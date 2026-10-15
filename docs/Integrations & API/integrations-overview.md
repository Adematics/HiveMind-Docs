---
title: Integrations Overview
hidden: false
---

Hivemind connects to the tools you already hire with: your mailbox and calendar, video meetings, your ATS, your team chat, and the AI assistant you use every day. Every connection lives in one searchable directory: **Settings → Apps & Integrations**. This page tours what each app unlocks and how to connect, fix, or remove it.

{/* 📸 Screenshot: Settings → Apps & Integrations directory with the Connected / Need attention / Available counts, the search box, the category filter and the "In use" and "Available" bands */}

## 1. Find your way around the directory

- **Counts at the top**: how many apps are **Connected**, how many **Need attention**, and how many are **Available**.
- **Search apps...**: search by name or by what an app does (for example "gmail", "teams" or "mcp").
- **Category filter**: **All**, **Calendar & Meetings**, **Messaging**, **ATS**, **AI**, **Analytics** and **Developer**.
- **In use** and **Available**: apps you have connected sit above the ones you haven't. Each tile shows its status: **Connected** (sometimes with a count such as *2 accounts*), **Needs attention**, or **Not connected**.

Click any tile to open its settings in a side panel. That panel is where you connect, reconnect, change settings and disconnect.

<Callout icon="💡" theme="info">
  You only see the apps your role can act on. Company-wide apps (ATS, Slack, ClickUp, Twilio, OpenAI, Power BI) need permission to manage company integrations. See [Team Members & Roles](/docs/team-members-roles).
</Callout>

## 2. What each app enables

| Category | App | What it enables |
| --- | --- | --- |
| Calendar & Meetings | **Google** | Send outreach from Gmail and sync replies and bounces, check Google Calendar availability, and add Google Meet links to interviews. |
| Calendar & Meetings | **Zoom** | Host interviews on Zoom and track attendance afterwards to spot no-shows. |
| Calendar & Meetings | **Microsoft** | Outlook mailboxes, Microsoft Teams meeting links for interviews, and Teams channel notifications. See [Microsoft 365](/docs/microsoft-365). |
| Messaging | **LinkedIn** | Send connection requests, messages and InMails from [Outreach Campaigns](/docs/outreach-campaigns), and post jobs with [LinkedIn Job Posting](/docs/linkedin-job-posting). |
| Messaging | **WhatsApp** | Message candidates directly from your outreach campaigns. |
| Messaging | **Slack** | A private Slack channel for every active pipeline, plus direct messages for your own tasks. See [Slack & ClickUp](/docs/slack-and-clickup). |
| Messaging | **ClickUp** | A ClickUp channel for every live pipeline that carries the decisions waiting on a person. See [Slack & ClickUp](/docs/slack-and-clickup). |
| Messaging | **Twilio** | Call candidates from the browser using your own Twilio account and number. See [Calling Candidates](/docs/calling-candidates). |
| ATS | **Ashby** | Two-way sync: Ashby applicants land in your pipelines and Hivemind results go back to Ashby as notes. See [Ashby Sync](/docs/ashby-sync). |
| ATS | **Greenhouse** | Manage job applications through Greenhouse, connected with a Greenhouse API key. |
| ATS | **Ceipal**, **TempWorks** | You can save an API key now, but candidate and requisition sync is not live yet. |
| AI | **OpenAI** | Use your own OpenAI API key so AI evaluations stop consuming credits; OpenAI bills you directly. |
| Analytics | **Power BI** | Sync pipelines, candidates and assessments to a Microsoft Power BI workspace every night. |
| Developer | **Connected apps** | Let Claude, ChatGPT or any MCP client work with your workspace in chat. See [Hivemind MCP Server](/docs/hivemind-mcp-server). |
| Developer | **Hivemind API key** | Authenticate requests to the [Public API](/docs/public-api-getting-started). |
| Developer | **Outbound webhook** | Post candidate events to your own HTTPS endpoint. See [Webhooks](/docs/webhooks). |

## 3. Personal vs. company-wide connections

Integrations come in two scopes:

- **Personal**: each teammate links their own account. Calendars and meeting platforms (Google Calendar and Meet, Zoom, Teams meetings), LinkedIn and WhatsApp are personal. Personal connections are private: teammates can see that you can host a Google Meet, Zoom or Teams interview, but not your account details.
- **Company-wide**: one connection shared by the whole workspace, set up by someone who can manage company integrations. Slack, ClickUp, Teams channel notifications, Twilio, OpenAI, Power BI and the ATS apps are company-wide.

Mailboxes can be either. When you connect a Gmail or Outlook mailbox, **Who is this account for?** lets you choose **Personal** (only you can see and use it) or **Company** (shared with your whole team).

## 4. Connect an app

1. Open **Settings → Apps & Integrations** and click the app's tile.
2. In the side panel, follow the connect step for that app:
   - **Sign-in apps** (Google, Microsoft, Zoom, Slack, ClickUp, Power BI): click the connect button, for example **Connect Gmail**, **Connect Google Calendar**, **Connect Zoom** or **Connect Slack**, and approve access on the provider's page. You return to Hivemind with the app connected.
   - **Twilio**: click **Connect Twilio** and authorize your Twilio account, then in **Finish connecting Twilio** pick a **Caller number**, paste a Standard API key (**API Key SID** and **API Key Secret**) and click **Test & Connect**. Calls are billed to your Twilio account, not Hivemind credits.
   - **API key apps** (Ashby, Greenhouse, OpenAI): paste the key into the **API key** field and connect. Hivemind checks the key before saving it.
   - **LinkedIn and WhatsApp**: follow the guided connection flow in the panel.
3. Some apps need one more step after connecting, such as adding webhooks in Ashby or pasting a Teams workflow URL. The app's own page walks you through it.

<Callout icon="💡" theme="info">
  Connecting a mailbox is also available from **Settings → Email Services**. See [Email Integration & Inbox](/docs/email-integration-inbox).
</Callout>

## 5. Fix, manage or disconnect

When a connection stops working, its tile reads **Needs attention** (or **Reconnect needed**) and a banner at the top of the directory lists every affected connection with a **Fix** button that opens the right panel.

- **Reconnect** restores a connection whose access expired or was revoked.
- **Disconnect** removes the connection. Hivemind confirms first. Existing scheduled meetings are preserved, and a company-wide app becomes unavailable to your entire company until it is reconnected.
- **Remove a single capability** by clicking the **×** on its badge, for example to drop **Calendar** from a Google account while keeping Meet. Removing the last capability disconnects the account entirely.
- **Zoom attendance upgrade**: older Zoom connections may show **Attendance tracking unavailable**. Click **Reconnect** to grant the extra access Hivemind needs to detect interview no-shows.

<Callout icon="⚠️" theme="warn">
  Automations that depend on a broken connection (scheduling, outreach sends, ATS sync, channel updates) pause until you reconnect. Check this page first when something stops sending.
</Callout>

## What's next

- Set up your mailbox in [Email Integration & Inbox](/docs/email-integration-inbox)
- Book interviews with [Calendar & Scheduling](/docs/calendar-scheduling)
- Get hiring updates in your team chat with [Slack & ClickUp](/docs/slack-and-clickup)
- Sync with your ATS using [Ashby Sync](/docs/ashby-sync)
- Build your own integration with the [Public API](/docs/public-api-getting-started) and [Webhooks](/docs/webhooks)
