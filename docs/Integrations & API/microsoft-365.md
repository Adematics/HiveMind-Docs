---
title: Microsoft 365
hidden: false
---

If your team runs on Microsoft 365, one **Microsoft** app in **Settings → Apps & Integrations** covers three things: Outlook mailboxes for sending and receiving candidate email, Microsoft Teams links for interviews, and a Teams channel that receives pipeline activity and team tasks.

{/* 📸 Screenshot: the Microsoft side panel showing the Outlook mailboxes, Teams meetings and Teams channel notifications sections */}

## 1. Outlook mailboxes

Connect an Outlook or Microsoft 365 mailbox to send outreach and pipeline email from your real address, and to sync replies and bounces back into Hivemind.

1. Open **Settings → Apps & Integrations** and click the **Microsoft** tile.
2. Under **Outlook mailboxes**, choose **Who is this account for?**: **Personal** (only you can see and use it) or **Company** (shared with your whole team).
3. Click **Connect Outlook** (or **Connect another mailbox** if you already have one) and sign in with Microsoft.

You can also connect Outlook from **Settings → Email Services** by choosing **Microsoft** (*Outlook & Microsoft 365*) in **Add Email Account**. See [Email Integration & Inbox](/docs/email-integration-inbox) for working with the inbox once mail starts arriving.

To remove a mailbox, click **Disconnect** next to it. Sending and inbound reply and bounce sync stop for that mailbox; if the same Microsoft account also hosts your Teams meetings, those stay connected.

<Callout icon="💡" theme="info">
  Microsoft doesn't let Hivemind revoke its access from inside the app. After disconnecting, also remove Hivemind at myapps.microsoft.com if you want the grant withdrawn on Microsoft's side.
</Callout>

### When a Microsoft admin has to approve

Many Microsoft 365 organizations don't let individual users grant mailbox access to a new app. If yours is one of them, Hivemind shows **Admin approval required** when you try to connect. You have two options:

- **I'm an admin, approve now**: if you are a Microsoft admin in your organization, approve it yourself.
- **Copy approval link for your IT admin**: send the link to someone who is.

Approval is a one-time step for your organization and covers Outlook, Teams and Power BI alike. Once it is approved, start the connection again.

## 2. Teams meetings

Under **Teams meetings**, click **Connect Teams meetings** to add a Microsoft Teams link to interviews you schedule. Once connected, **Microsoft Teams** becomes available as a meeting platform in your interview steps, alongside Google Meet and Zoom. See [Calendar & Scheduling](/docs/calendar-scheduling) for setting it up on an interview.

## 3. Teams channel notifications

Post pipeline activity and team tasks to one Teams channel for the whole company. Hivemind batches what happened into a single card about once a minute rather than posting a message per event.

The card covers:

- **Pipeline activity**: new applicants, candidates who moved stage, finished, or need attention.
- **Team tasks**: candidates waiting for a review, interviews to schedule, phone calls ready to start, and new email in a shared (company) mailbox. Mail details stay in Hivemind: the card only says something arrived and links to the inbox. Tasks assigned to one person, and mail in personal mailboxes, never reach the channel.

To connect it, you need permission to manage company integrations:

1. In Teams, open the channel and select **More options (...) > Workflows**.
2. Choose the **Send webhook alerts to a channel** template.
3. Pick the team and channel, then save the workflow.
4. Copy the webhook URL. In Hivemind, open the **Microsoft** tile and paste it into **Webhook URL** under **Teams channel notifications**.
5. Click **Connect Teams notifications**. Hivemind posts a welcome message to check the URL before saving it.

<Callout icon="⚠️" theme="warn">
  Teams Workflows can't post to private channels, and messages appear as posted by Workflows. If the person who created the workflow leaves, or the workflow is turned off or deleted, the section shows that Teams stopped accepting messages: click **Disconnect Teams notifications** and connect again with a new URL.
</Callout>

Disconnecting stops Hivemind posting to the channel. Messages already there are left in place.

## 4. Power BI

The **Power BI** tile (under **Analytics**) uses a Microsoft account too. Someone who can manage company integrations clicks **Connect Power BI** once for the whole company, and Hivemind syncs pipelines, candidates and assessments into a Power BI workspace every night. Share that workspace with teammates inside Power BI to give them access. The connected account needs a Power BI Pro (or PPU/Fabric) license; without one the tile shows **Pro license required**.

## What's next

- Work with incoming mail in [Email Integration & Inbox](/docs/email-integration-inbox)
- Set up interview steps in [Calendar & Scheduling](/docs/calendar-scheduling)
- Prefer Slack or ClickUp? See [Slack & ClickUp](/docs/slack-and-clickup)
- See every app in the [Integrations Overview](/docs/integrations-overview)
