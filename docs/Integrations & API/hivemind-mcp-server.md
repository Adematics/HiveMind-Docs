---
title: Hivemind MCP Server
hidden: false
---

The Hivemind MCP server puts your hiring data inside the AI assistant your team already uses: Claude, ChatGPT, Microsoft Copilot, or any client that speaks the [Model Context Protocol](https://modelcontextprotocol.io). Ask "who's still in screening for the backend role?" in plain language and the answer comes back grounded in your live pipelines, candidates, and assessment results.

The server is live at `https://mcp.hivemind.hr` and exposes **38 tools**. Most of them read: pipelines, candidates, assessments, questions, and outreach campaigns. Some of them build, and those follow a two-step pattern, so nothing an assistant produces goes live on its own.

<Callout icon="🔒" theme="info">
  Everything the assistant sees is scoped to one company: whichever company the connection was authorized for. Connect with **Sign in with Hivemind** below and you can review and revoke that access at any time from Settings.
</Callout>

## Building tools stage first, then commit

Tools that create a pipeline, an assessment or an outreach campaign write a **staged draft**, not a live object. A separate `commit_` tool promotes it. In between you can list it, edit it, screenshot it to see what it will look like, or delete it and start over.

That means an assistant cannot activate a pipeline or send a campaign in one step. Ask for a pipeline and you get a draft to approve.

## 1. Connect with one click

In Claude, add a **custom connector** pointing at `https://mcp.hivemind.hr`. Claude discovers the rest: you are sent to Hivemind, you sign in if you are not already, and a consent screen names the app asking for access. Approve it and the connection is live. There is no key to copy and nothing to paste.

The consent screen shows a **verified** badge for apps Hivemind can vouch for, which today means Claude. An app without that badge is showing you a name it chose for itself, so read it with suspicion before approving.

{/* 📸 Screenshot: the Hivemind consent screen showing the verified Claude badge */}

### Review and revoke access

Connected apps are listed under **Settings → Apps & Integrations**. Each one can be revoked there, which takes effect immediately and cannot be undone from the app's side. Revoking is the right move when a laptop goes missing or a teammate leaves.

<Callout icon="💡" theme="info">
  Connections are per user. Revoking yours does not disturb a colleague's, and a colleague's connection sees the same company data yours does, under their own permissions.
</Callout>

## 2. Or connect with an API key

An API key is still the right choice for a script, a server, or a client that does not speak OAuth. Sections 3 and 4 below use this route.

In Hivemind, go to **Settings → Apps & Integrations** and generate or copy the API key. It looks like `hk_live_…`.

**One active key per company.** Regenerating revokes the previous key, which breaks every client already using it, so reuse the same key across your MCP clients rather than minting a second one.

{/* 📸 Screenshot: Settings → Apps & Integrations showing the API key card */}

## 3. Connect from Claude Code (CLI) with a key

Claude Code speaks HTTP natively, so it's one command:

```bash
claude mcp add hivemind --transport http https://mcp.hivemind.hr \
  --header "Authorization: Bearer hk_live_YOUR_KEY_HERE"
```

Verify it connected:

```bash
claude mcp get hivemind     # URL, headers, connection status
claude mcp list             # health-check every configured server
```

Expect `Status: ✔ Connected`.

## 4. Connect from Claude Desktop with a key

Claude Desktop is configured through its JSON config file, and it accepts stdio servers only, so the connection is bridged with `mcp-remote` (requires Node.js on PATH).

| OS | Config file |
| --- | --- |
| macOS | `~/Library/Application Support/Claude/claude_desktop_config.json` |
| Windows | `%APPDATA%\Claude\claude_desktop_config.json` |
| Linux | `~/.config/Claude/claude_desktop_config.json` |

Merge this entry under `mcpServers` (add it alongside any servers already there; don't replace the file):

```json
{
  "mcpServers": {
    "hivemind-mcp-remote": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.hivemind.hr",
        "--header",
        "Authorization: Bearer hk_live_YOUR_KEY_HERE"
      ]
    }
  }
}
```

Prefer not to edit JSON by hand? Run the command for your OS below; each one does the merge for you (it only touches the `hivemind-mcp-remote` entry and creates the file if it doesn't exist).

**macOS / Linux** (needs `jq`: `brew install jq` on macOS, `sudo apt install jq` on Linux)

First set the config path for your OS (run only the line that matches):

```bash
# macOS
CONFIG="$HOME/Library/Application Support/Claude/claude_desktop_config.json"
# Linux
CONFIG="$HOME/.config/Claude/claude_desktop_config.json"
```

Then run the merge; it's identical on both:

```bash
mkdir -p "$(dirname "$CONFIG")" && [ -s "$CONFIG" ] || echo '{}' > "$CONFIG"
jq '.mcpServers["hivemind-mcp-remote"] = {
  "command": "npx",
  "args": ["-y", "mcp-remote", "https://mcp.hivemind.hr",
           "--header", "Authorization: Bearer hk_live_YOUR_KEY_HERE"]
}' "$CONFIG" > "$CONFIG.tmp" && mv "$CONFIG.tmp" "$CONFIG"
```

**Windows** (PowerShell, nothing extra needed)

```powershell
$path = "$env:APPDATA\Claude\claude_desktop_config.json"
if (!(Test-Path $path) -or !(Get-Content $path -Raw).Trim()) {
  New-Item -ItemType File -Path $path -Force | Out-Null
  Set-Content $path '{}'
}
$cfg = Get-Content $path -Raw | ConvertFrom-Json
if (!$cfg.PSObject.Properties['mcpServers']) {
  $cfg | Add-Member -NotePropertyName mcpServers -NotePropertyValue ([pscustomobject]@{})
}
$server = [pscustomobject]@{
  command = "npx"
  args = @("-y","mcp-remote","https://mcp.hivemind.hr","--header","Authorization: Bearer hk_live_YOUR_KEY_HERE")
}
$cfg.mcpServers | Add-Member -NotePropertyName "hivemind-mcp-remote" -NotePropertyValue $server -Force
$cfg | ConvertTo-Json -Depth 10 | Set-Content $path
```

Then **fully quit and reopen Claude Desktop**; it only reads the config at startup. The server appears under the tools (🔨) icon in the composer.

<Callout icon="💡" theme="info">
  The `mcp-remote` bridge above is only needed for the API key route. If you connect with **Sign in with Hivemind**, add `https://mcp.hivemind.hr` as a custom connector instead and skip the config file entirely, on claude.ai and in Claude Desktop alike.
</Callout>

## 5. Verify it works

Both clients should list **38 tools**. The quickest end-to-end check is to ask:

> List my Hivemind pipelines.

If your pipelines come back, authentication and company resolution are both working. To check the server itself:

```bash
curl -fsS https://mcp.hivemind.hr/healthz   # -> ok (unauthenticated)
```

A `401` on any other route is correct: every MCP route is auth-gated; only `/healthz` is open.

## 6. What you can ask

The tools cover pipelines, candidates, assessments, questions, and outreach. Some starters:

Reading:

- *Who's still in screening for the Backend Engineer pipeline?*
- *How is the senior pipeline converting stage to stage?*
- *Which candidates scored above 80 on the coding assessment?*
- *Compare the top three candidates in the design pipeline.*

Building, which stages a draft for you to approve:

- *Draft a pipeline for a senior backend engineer with a resume screen and a coding assessment.*
- *Put together a React and TypeScript assessment at medium difficulty.*
- *Start an outreach campaign for the designers I sourced last week and add them as recipients.*

<Callout icon="⚠️" theme="warn">
  Check a staged draft before committing it. Ask the assistant to screenshot it, or open it in Hivemind. `commit_` is the point of no return, and it is the one step worth doing with your own eyes on the result.
</Callout>

## What's next

- Get your key set up in [Integrations Overview](/docs/integrations-overview)
- Automate the other direction with [Webhooks](/docs/webhooks)
- Prefer raw HTTP? See [Public API: Getting Started](/docs/public-api-getting-started)
