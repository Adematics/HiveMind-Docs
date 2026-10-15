---
title: Slack & ClickUp
hidden: false
---

Hiring decisions get discussed where your team already talks. Connect Slack or ClickUp once for the whole company and Hivemind keeps a channel for each live pipeline up to date on its own, so nobody has to copy updates out of the app by hand.

Both are company-wide connections. You need permission to manage company integrations to connect or disconnect them; see [Team Members & Roles](/docs/team-members-roles).

{/* 📸 Screenshot: a Hivemind pipeline channel in Slack showing a grouped activity digest */}

## Slack

### What you get

- **A private channel per active pipeline.** Each active pipeline gets its own private Slack channel named after it. Teammates whose Slack email matches their Hivemind account are invited automatically; anyone without a matching Slack account is skipped.
- **Grouped updates, not noise.** Activity is collected into one digest a minute: who applied, who moved stage, who finished, and who needs attention.
- **Direct messages for your own tasks.** Each person gets a DM from Hivemind for work that is theirs: a candidate to review, an interview to schedule, a phone call ready to start, a mention in a comment, a reply in a conversation, or a new inbound email. Every DM links straight to the right place in Hivemind.

When a pipeline is switched off, its channel is archived. Switch the pipeline back on and the same channel is unarchived, so its history stays in one place.

### Connect Slack

1. Open **Settings → Apps & Integrations** and click **Slack** under **Messaging**.
2. Click **Connect Slack** and approve access for your Slack workspace.
3. That's it. Channels are created for every pipeline that is already active, and for each pipeline you activate from now on.

### Disconnect Slack

Open the Slack panel and click **Disconnect**. This stops all notifications and pipeline channel digests. The pipeline channels are archived, and the channels and their messages stay in Slack. If you reconnect later, Hivemind picks up the same channels again instead of creating duplicates.

If the Hivemind app was removed from your workspace, the panel shows **Reconnect Slack** instead of **Connect Slack**.

## ClickUp

### What you get

When a pipeline is activated, Hivemind creates a channel for it in ClickUp Chat. Rather than every bit of activity, the channel carries only the moments that need a person:

- a candidate waiting for a review (flagged if they were a no-show)
- an offer that needs signing
- an interview to book
- an offer the candidate came back on with requested changes, or declined

Each message links straight to the task in Hivemind. When the task is resolved, the message updates itself to show the outcome (**Approved**, **Rejected**, **Skipped** or **Resolved**), so the channel reads as a record of what was decided rather than a list of stale requests. Where a task belongs to someone whose email matches a member of your ClickUp workspace, the message is assigned to them.

### Before you connect

- **Use a dedicated ClickUp account.** ClickUp channels belong to whoever authorized them, so a connection made with a personal account stops working if that person ever leaves.
- **ClickUp Chat must be available on your ClickUp plan**, since the channels live there.
- **Channels are public in your ClickUp Workspace.** Members of your ClickUp workspace can find and follow them.

### Connect ClickUp

1. Open **Settings → Apps & Integrations** and click **ClickUp** under **Messaging**.
2. Click **Connect ClickUp** and approve access for your ClickUp Workspace.
3. Channels are created for pipelines that are already live, and for each pipeline you activate from now on. The panel shows the account it is **Connected as** and the **Workspace**.

### Disconnect ClickUp

Click **Disconnect** in the ClickUp panel. Pipelines activated from now on stop getting a channel; channels that already exist are left in place. ClickUp has no way for Hivemind to revoke its own access, so also remove the Hivemind app in ClickUp to withdraw access there.

<Callout icon="💡" theme="info">
  Prefer Microsoft Teams? A Teams channel can receive pipeline activity and team tasks too. See [Microsoft 365](/docs/microsoft-365).
</Callout>

## What's next

- See every app in the [Integrations Overview](/docs/integrations-overview)
- Set up the review steps these channels report on in [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Control in-app and mobile alerts in [Notifications & Mobile App](/docs/notifications-mobile-app)
