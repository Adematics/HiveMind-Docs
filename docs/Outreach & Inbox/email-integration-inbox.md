---
title: Email Integration & Inbox
hidden: false
---

Connecting a mailbox lets Hivemind send and receive email on your behalf: automated pipeline messages, outreach sequences, and your own replies all go out through your real address, and candidate responses flow back into your **Inbox** automatically. This guide covers connecting Gmail or a custom mail server, and working with conversations once mail starts arriving.

<Callout icon="⚠️" theme="warn">
  Without a connected mailbox, automated candidate emails, outreach email steps, and inbound reply tracking won't run. Connect one before your pipelines or campaigns go live.
</Callout>

## 1. Connect an email account

1. Open **Settings → Email Services** to reach the **Email Accounts** page.
2. Click **Add Account**.
3. Choose who the account is for: **Personal** (only you can see and use it) or **Company** (shared with your whole team).
4. Pick a provider:
   - **Google**: for Gmail and Google Workspace. You're redirected to Google to sign in and approve access; one approval covers both sending and reading replies, so reply and bounce tracking work immediately.
   - **SMTP**: for any other provider. In the **Connect Email Account** dialog, enter your **Email Address** and **Password**, your **SMTP Server**, and a **Username**, and choose whether to **Use TLS Encryption**. Turn on **Inbox Sync (IMAP)** and fill in the **IMAP Server** and **Port** (usually 993) so replies sync automatically. Hivemind verifies the connection step by step and confirms with **Account connected successfully**.

{/* 📸 Screenshot: the Add Email Account dialog showing the Google and SMTP options */}

## 2. Manage your accounts

Each connected account appears as a card with status pills: Google accounts show **Connected**, while SMTP accounts show **SMTP Verified** (sending works) and **IMAP Enabled** (replies sync). You can connect multiple accounts and flip **Set as default** on the one Hivemind should use for automated emails. Use the card menu to **Edit Settings** or **Remove** an account, and **Test Email Accounts** at the top of the page to run a **Verify Connection** check anytime.

{/* 📸 Screenshot: the Email Accounts page with a connected account card and its status pills */}

## 3. Sending and receiving

Outgoing mail (pipeline automations, [outreach campaign](/docs/outreach-campaigns) steps, and replies you write) is sent through your connected account, so candidates see your address, not a generic one. Inbound works automatically: Gmail accounts sync replies in real time, and IMAP accounts are checked on a regular schedule. Hivemind matches each reply to the conversation it belongs to and files it in your Inbox.

## 4. Working in the Inbox

Your **Inbox** is a unified list of everything needing attention: new emails alongside candidate reviews, chat replies, and other tasks. Use the **Filters** button to narrow by **Status**, **Read** state, or **Date range**, filter by pipeline, or pick task types such as **New Email**, **Message Reply**, or **Candidate Review**. Unread items show a red dot.

New replies appear as **New email from [sender]**. Open one to read the full thread; if the sender matches a candidate, a **View Profile** button jumps to their [candidate profile](/docs/candidate-profiles), and email history also appears on the profile itself. To respond, click **Reply to [name]**, write your message, and hit **Send**; it goes out from the mailbox the conversation belongs to.

Each outgoing message carries a delivery status (**Sent**, **Delivered**, **Opened**, **Clicked**, **Replied**, or **Bounced**), and the **Activity** panel shows the full event timeline.

{/* 📸 Screenshot: the Inbox with a New Email task open and the reply composer visible */}

<Callout icon="💡" theme="info">
  In-app chat messages from candidates land in the same Inbox as **Message Reply** tasks, so you can answer email and chat from one place.
</Callout>

## 5. Bounce tracking

When a message can't be delivered, a **Bounce** item appears in your Inbox showing the failed recipient and the original subject. Opening it shows a **Delivery failed** banner with the details, so you can correct the address or try another channel before the candidate goes cold.

## What's next

- Launch your first sequence in [Outreach Campaigns](/docs/outreach-campaigns)
- Connect calendars and more in [Account & Workspace Setup](/docs/account-workspace-setup)
- Control who can manage email accounts in [Team Members & Roles](/docs/team-members-roles)
