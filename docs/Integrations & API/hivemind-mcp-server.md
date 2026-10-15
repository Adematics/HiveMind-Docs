---
title: Hivemind MCP Server
hidden: false
---

The Hivemind MCP server puts your hiring data inside the AI assistant your team already uses: Claude, ChatGPT, or any app that supports the [Model Context Protocol](https://modelcontextprotocol.io). Ask "who's still in screening for the backend role?" or "rank everyone we have by years of Postgres" in plain language, and the answer comes back grounded in your live pipelines, candidates, and assessment results, with a link to every candidate it names.

The server lives at `https://mcp.hivemind.hr` and is listed in the official MCP Registry as `hr.hivemind/mcp`. It exposes **56 tools**. Most of them read; the ones that build or change things ask you first, and nothing an assistant drafts goes live on its own.

<Callout icon="🔒" theme="info">
  Every connection belongs to one person and one company. The assistant sees only the company you signed in to, and it can only do what your role in Hivemind allows.
</Callout>

## 1. Connect your assistant

Hivemind connects by signing in. There is no API key to copy and nothing to paste.

1. In your assistant, add a **custom connector** (some apps call it an **MCP server** or **Integration**). Choose the option for a remote server, not a local command.
2. Use `https://mcp.hivemind.hr` as the server URL, with no trailing slash.
3. Your assistant sends you to Hivemind. Sign in if you aren't already, check the workspace shown is the right one, and choose **Allow**.

The tools appear straight away. In **Claude** (claude.ai or Claude Desktop) this is **Settings → Connectors → Add custom connector**. In **Claude Code** it is one command, and Claude Code runs the sign-in for you:

```bash
claude mcp add --transport http hivemind https://mcp.hivemind.hr
```

Hivemind has the same steps in the app: open **Settings → Apps & Integrations**, click **Connected apps** and choose **How to connect**.

{/* 📸 Screenshot: the Hivemind consent screen showing the Verified badge and the Allow button */}

The consent screen shows a **Verified** badge for apps Hivemind can vouch for: Claude, ChatGPT and ClickUp today. Any other app shows **Unverified**: it still connects, but the name is one the app chose for itself, so read it with suspicion before approving.

<Callout icon="⚠️" theme="warn">
  API keys no longer work with the MCP server. If you set up Hivemind earlier with an `hk_live_` key (for example through `mcp-remote` in Claude Desktop's config file), remove that entry and connect with the steps above. The API key is still the right way in for the [Public API](/docs/public-api-getting-started).
</Callout>

## 2. Review and revoke access

Your connected apps are listed under **Settings → Apps & Integrations → Connected apps**, each with when it connected and whether it is verified. Click **Disconnect** to revoke one: it loses access and cannot reconnect unless you allow it again. If it is in the middle of something, that can take up to an hour to stop completely. Anything it already created stays where it is.

Connections are per person. Disconnecting yours does not affect a colleague's.

## 3. What it can do

The 56 tools fall into these groups:

| Group | Tools | What you can ask for |
| --- | --- | --- |
| **Candidates** | 8 | Search everyone in the company by resume content, skills, location, scores and stage; read full evidence for up to 10 candidates; compare 2 to 10 side by side; rank a pool; funnel counts for one pipeline or the whole company. |
| **Candidate lists** | 6 | Find your saved lists, see who is on one, save a shortlist, take people off a list, rename a list, or delete one. |
| **Pipelines** | 9 | List and read pipelines; draft a new pipeline, preview it, and save it; edit a draft. |
| **Assessments** | 7 | List assessments; draft a new one from your question bank (or new questions you agree to), preview it, and save it. |
| **Outreach campaigns** | 15 | Draft a campaign and its steps, add recipients from a pasted list, from candidates or from a saved list, check what still blocks launch, and link a campaign to a pipeline. |
| **Message variables** | 5 | See which variables a campaign's leads carry, and manage your company-wide variables. |
| **Reference and lookups** | 6 | Roles and skills, question bank search, the email senders and interviewers you can use, and reference material the assistant reads before building. |

Some things worth knowing:

- **Company-wide answers.** Counts work across every pipeline, so "how many applications came in last month?" doesn't need a pipeline name. Answers bounded by dates show today's date beside the window, so "last month" is never ambiguous.
- **Ranking.** The assistant can rank one pipeline's candidates by the total score, the resume score, a step type such as the assessment, or one specific step, and tells you who has no score yet instead of quietly dropping them. It can also rank a pipeline, a saved list, or every candidate in the company by **months of experience with a skill** from their resume, narrowed by status, stage, hired, or application date. People who list the skill without a duration count as unknown, never as zero.
- **Compare and shortlist.** Ask it to compare candidates and it lines them up on shared skills, scores and questions. Happy with the result? Ask it to save the shortlist and it lands under **Candidate Lists** in Hivemind for the rest of the team.
- **Outreach from people you already have.** Add candidates or a saved list straight to a campaign instead of exporting a spreadsheet. People who opted out of your emails are never added, and the assistant tells you who was skipped for having no email.
- **Honest limits.** Some requests are beyond what search can do today: matching on meaning rather than words, judging fit against a job description across your database, or searching interview transcripts. The assistant says so first, then offers the closest search it can run, labelled as an approximation.
- **Links you can check.** Every candidate it names comes with a link to their profile in Hivemind. The link only opens for people signed in to your company.

Some apps also show ready-made starting points from Hivemind, such as **build_pipeline**, **create_assessment** and **review_candidates**.

## 4. Safety: drafts, previews, and confirmations

**Building stages first, then commits.** Asking for a pipeline, an assessment or an outreach campaign creates a **staged draft**, not a live object. The assistant gives you a preview link and a screenshot, lists the defaults it chose, and asks whether to save it. Edits keep the same draft and the same link. Only when you say to save does it commit, and pipelines are saved as drafts unless you ask otherwise.

**Going live stays with you.** Activating a pipeline and launching a campaign are done by you in the Hivemind app, never by the assistant.

**It asks before anything final.** The assistant needs your explicit go-ahead, in the conversation, before it saves a draft, saves a shortlist, removes people from a list, deletes a list, removes campaign recipients, or overwrites a lead's variables. Deleting a list never deletes the candidates on it, and removing someone from a list removes them from nothing else.

<Callout icon="⚠️" theme="warn">
  Check a staged draft before you tell the assistant to save it. Open the preview link or ask for a screenshot: saving is the step worth doing with your own eyes on the result.
</Callout>

## 5. Role-aware answers

The assistant follows your role in Hivemind, using the same rules as the app. It only offers the tools your role allows, so how many of the 56 tools you see depends on your role. A teammate who can't create pipelines in the app can't create them through the assistant either, and when you ask for something outside your role it tells you plainly that it isn't available to you rather than looking for another way round.

Roles are checked live: changing someone's role, or deactivating them, reaches the assistant within a minute. See [Team Members & Roles](/docs/team-members-roles).

## 6. Usage limits

Limits are per company, shared by everyone's connections:

- **120 tool calls per minute** in total.
- The tools that read whole candidate records (candidate search, the skill vocabulary, full candidate details, and comparisons) also have their own budget of **30 calls per minute** and **2,000 per day**.

If a limit is reached, the assistant is told how long to wait and backs off.

## 7. Check it works

The quickest end-to-end check is to ask your assistant:

> List my Hivemind pipelines.

If your pipelines come back, sign-in and company access are both working. To check the server itself:

```bash
curl -fsS https://mcp.hivemind.hr/healthz   # -> ok (no sign-in needed)
```

Every other route needs a signed-in connection, so a `401` there is expected.

## What's next

- See every connection in the [Integrations Overview](/docs/integrations-overview)
- Automate the other direction with [Webhooks](/docs/webhooks)
- Prefer raw HTTP? See [Public API: Getting Started](/docs/public-api-getting-started)
