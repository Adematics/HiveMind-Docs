---
title: Outreach Campaigns
hidden: false
---

Outreach campaigns let you reach candidates who haven't applied yet. You build a multi-step sequence (emails, text messages, LinkedIn touches, WhatsApp), add recipients, set a sending schedule, and launch. Hivemind then sends each step automatically, spaces sends out to protect your accounts, and tracks who replies and who applies.

<Callout icon="💡" theme="info">
  Email steps send from a mailbox you've connected in **Settings → Email Services**. Connect one before launching. See [Email Integration & Inbox](/docs/email-integration-inbox).
</Callout>

## 1. Create a campaign

1. Open **Outreach** and switch to the **Campaigns** tab.
2. Click **New Campaign**. Hivemind creates a draft called **Untitled Campaign** and opens it.
3. Click the name to rename it.

Drafts walk you through a three-step wizard: **Recipients**, **Sequence**, and **Launch**.

{/* 📸 Screenshot: Campaigns tab with the New Campaign button and campaign list */}

## 2. Add recipients

On the **Recipients** step you can add people four ways:

- **Add Manually**: enter a **Name** and **Email**, plus optional **Phone**, **LinkedIn URL**, and **Notes**.
- **Import CSV**: drag and drop a CSV (up to 10 MB). Match your columns to **Name**, **Email**, **Phone**, **Notes**, or **LinkedIn** in the **Column Mapping** section, check the preview, then click **Import**. Rows without a valid email are skipped.
- **From Contacts**: the **Browse Contacts** dialog picks people from your contact library; anyone already in the campaign is marked **In campaign**.
- **Search**: describe who you're looking for and add matches straight from [People Search](/docs/sourcing-with-people-search).

{/* 📸 Screenshot: the Import CSV dialog showing column mapping and preview */}

## 3. Build the sequence

The **Sequence** step is a visual flow from **Start** to **End**. Click the **+** on any connector to **Add Step**: **Email**, **SMS**, **LinkedIn Invite**, **LinkedIn Message**, **LinkedIn InMail**, **LinkedIn Visit**, or **WhatsApp**. Every step after the first gets a **Wait** delay you can set in days or weeks.

For email steps, pick a starter template (like **Professional Introduction** or **Gentle Reminder**) or choose **Write Custom**, then fill in the **Subject Line** and **Email Body**. You can insert variables such as first name and an application link. SMS and WhatsApp steps only go to recipients who have a phone number on file, and LinkedIn InMail requires a Premium, Recruiter, or Sales Navigator sending account.

{/* 📸 Screenshot: the sequence builder with an email step and the Add Step menu open */}

## 4. Configure settings and schedule

Click **Settings** to open **Campaign Settings**:

- **General**: the campaign name and the **Email Account**, **LinkedIn Account**, and **WhatsApp Account** used for sending.
- **Schedule**: **Send spacing** between sends, the **Sending window**, **Timezone**, and **Active days**, with a **Delivery preview** of the rollout. By default campaigns send on weekdays, 9:00–17:00, ten minutes apart.
- **Pipeline**: a **Linked Pipeline**. Recipients who apply through the campaign are automatically added to it. See [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline).

<Callout icon="⚠️" theme="warn">
  If your message uses the application link variable, you must link a pipeline. Otherwise launch is blocked with **Missing pipeline connection**.
</Callout>

## 5. Launch

The **Launch** step shows your recipients next to a **Sequence Preview** and lists anything left to fix (for example **No email account connected**). Click **Launch to N recipients**, review the schedule and rollout plan in the **Launch Campaign** dialog, and confirm.

Campaigns move through **Draft**, **Active**, **Paused**, and **Completed**. On a live campaign, the **Manage** menu offers **Pause Campaign**, **Resume Campaign**, and **Send to New Recipients** for people added later.

## 6. Track progress

The campaign header shows delivery progress with **Sent**, **Replied**, **Applied**, and **Pending** counts (plus **Bounced** and **Opted Out** when relevant). Each recipient moves from **Pending** to **Sent**, then to **Replied** when they respond or **Applied** when they apply; replied, applied, bounced, and opted-out recipients stop receiving further steps. Row actions let you **Edit** a recipient, **Send Now** to skip the wait, or **Remove Prospect**.

## What's next

- Find new prospects with [Sourcing with People Search](/docs/sourcing-with-people-search)
- Connect your mailbox in [Email Integration & Inbox](/docs/email-integration-inbox)
- Build the pipeline applicants land in: [Creating a Pipeline](/docs/creating-a-pipeline)
