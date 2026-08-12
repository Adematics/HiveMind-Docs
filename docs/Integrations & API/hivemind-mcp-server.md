---
title: Hivemind MCP Server
hidden: false
---

The Hivemind MCP server puts your hiring data inside the AI assistant your team already uses: Claude, ChatGPT, Microsoft Copilot, or any client that speaks the [Model Context Protocol](https://modelcontextprotocol.io). Ask "who's still in screening for the backend role?" in plain language and the answer comes back grounded in your live pipelines, candidates, and assessment results.

The server is live at `https://mcp.hivemind.hr` and exposes **25 tools**. Sessions are **read-only**: your assistant can look anything up, and it can never change anything in your account.

<Callout icon="🔒" theme="info">
  Authentication is per request, using your Hivemind API key. Everything the assistant sees is scoped to that key's company.
</Callout>

## 1. Get an API key

In Hivemind, go to **Settings → Apps & Integrations** and generate or copy the API key. It looks like `hk_live_…`.

**One active key per company.** Regenerating revokes the previous key, which breaks every client already using it, so reuse the same key across your MCP clients rather than minting a second one.

{/* 📸 Screenshot: Settings → Apps & Integrations showing the API key card */}

## 2. Connect from Claude Code (CLI)

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

## 3. Connect from Claude Desktop

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

<Callout icon="⚠️" theme="warn">
  For now, the Hivemind MCP server can't be added on the claude.ai website itself; use Claude Code or Claude Desktop. Support for connecting it directly on claude.ai is planned for a future release, and this page will be updated when it lands.
</Callout>

## 4. Verify it works

Both clients should list **25 tools**. The quickest end-to-end check is to ask:

> List my Hivemind pipelines.

If your pipelines come back, authentication and company resolution are both working. To check the server itself:

```bash
curl -fsS https://mcp.hivemind.hr/healthz   # -> ok (unauthenticated)
```

A `401` on any other route is correct: every MCP route is auth-gated; only `/healthz` is open.

## 5. What you can ask

The 25 tools cover pipelines, candidates, and assessment results. Some starters:

- *Who's still in screening for the Backend Engineer pipeline?*
- *How is the senior pipeline converting stage to stage?*
- *Which candidates scored above 80 on the coding assessment?*
- *Compare the top three candidates in the design pipeline.*

## What's next

- Get your key set up in [Integrations Overview](/docs/integrations-overview)
- Automate the other direction with [Webhooks](/docs/webhooks)
- Prefer raw HTTP? See [Public API: Getting Started](/docs/public-api-getting-started)
