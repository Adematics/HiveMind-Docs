---
title: Integrations Overview
hidden: false
---

Hivemind connects to the tools you already hire with: your email, calendar, video conferencing, ATS, and messaging channels. Everything lives in one place: **Settings → Apps & Integrations**. This page tours what each provider unlocks and how to connect or disconnect it.

{/* 📸 Screenshot: Settings → Apps & Integrations page showing the API key, webhook, and integration cards */}

## 1. What each integration enables

| Provider | What it enables |
| --- | --- |
| **Google** | Send and read Gmail (outreach and reply tracking), sync **Google Calendar** for interview scheduling and free/busy checks, and host interviews on **Google Meet**. |
| **Microsoft** | Outlook send, calendar sync, and Teams meetings. In the interview setup picker, **Microsoft Teams** is currently marked **Coming soon**. |
| **Zoom** | Schedule and host interviews on Zoom, plus **Attendance** tracking to detect no-shows after a meeting ends. |
| **Ashby** | ATS integration: connect with an Ashby API key to sync candidates between systems. |
| **Greenhouse** | ATS integration: connect with a Greenhouse API key to manage job applications across both tools. |
| **OpenAI** | Bring your own OpenAI API key. Once connected, **credits are no longer deducted for AI evaluations**; usage bills to your own key instead. |
| **Twilio** | SMS to candidates. Connecting requires your Twilio **API key, secret and a caller number**. |
| **Zapier** | Push Hivemind pipeline data into thousands of other apps via the Hivemind app on Zapier. |
| **Stripe** | Powers payments for plans and credit purchases, managed from [Credits & Billing](/docs/credits-billing) rather than a connect card. |
| **LinkedIn & WhatsApp** | Messaging channels for [Outreach Campaigns](/docs/outreach-campaigns): send LinkedIn connection requests, messages, and InMails, or message candidates on WhatsApp. A connected LinkedIn account also unlocks [LinkedIn Job Posting](/docs/linkedin-job-posting): publish any Hivemind job to LinkedIn in one click. |

## 2. Personal vs. company-wide connections

Integrations come in two scopes:

- **Personal**: each teammate links their own account (Google email/calendar, Google Meet, Zoom, LinkedIn, and WhatsApp). Your connections appear under **My connected accounts** with badges showing what each account can do (for example **Calendar**, **Meet**, **Gmail**).
- **Company-wide**: one connection shared by the whole workspace (Twilio, OpenAI, Ashby, and Greenhouse). These cards are only visible to roles that can manage company integrations (Owner, Admin, and Developer). See [Team Members & Roles](/docs/team-members-roles).

## 3. Connect an integration

1. Open **Settings → Apps & Integrations**.
2. For OAuth providers, click the matching button (**Connect Google Calendar**, **Connect Google Meet**, or **Connect Zoom**) and approve the requested access on the provider's page. You'll return to Hivemind with the new account listed.
3. For API-key providers (Ashby, Greenhouse, OpenAI), paste the key into the card's **API Key** field and connect. Twilio additionally asks for the secret and caller number.
4. LinkedIn and WhatsApp have their own cards with a guided connection flow for linking your accounts.

<Callout icon="💡" theme="info">
  Connecting your mailbox for candidate email lives in a separate tab: **Settings → Email Services**. See [Email Integration & Inbox](/docs/email-integration-inbox).
</Callout>

{/* 📸 Screenshot: "My connected accounts" section with a Google card showing Calendar / Meet capability badges */}

## 4. Manage or disconnect

Each connected account is a card showing its status: **Active**, or an error state with a **Reconnect** button when access has expired or been revoked.

- **Disconnect** removes the whole connection. Hivemind confirms first; existing scheduled meetings are preserved, and company-wide integrations become unavailable to your entire company until reconnected.
- **Remove a single capability** by clicking the **×** on its badge, for example to drop **Calendar** from a Google account while keeping **Meet**. Removing the last capability disconnects the account entirely.
- **Zoom attendance upgrade**: older Zoom connections may show *Attendance tracking unavailable*. Click **Reconnect** on that prompt to grant the extra scope so Hivemind can detect interview no-shows.

<Callout icon="⚠️" theme="warn">
  If an integration shows **Reconnect needed** or **expired**, automations that depend on it (scheduling, outreach sends, ATS sync) pause until you reconnect. Check this page first when something stops sending.
</Callout>

## What's next

- Set up your mailbox in [Email Integration & Inbox](/docs/email-integration-inbox)
- Book interviews with [Calendar & Scheduling](/docs/calendar-scheduling)
- Message candidates at scale with [Outreach Campaigns](/docs/outreach-campaigns)
- Build your own integration with the [Public API](/docs/public-api-getting-started) and [Webhooks](/docs/webhooks)
