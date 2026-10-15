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
- **Import CSV**: drag and drop a CSV (up to 10 MB). Under **Contact details**, pick which column holds each of **Name**, **Email**, **Phone**, **LinkedIn**, and **Notes** (only email is required). Every other column is listed under **Variables**: leave it on and it becomes a per-lead variable you can write into your messages, or switch it to **Not imported**. Check the preview, then click **Import**. Rows without a valid email are skipped, and re-importing someone already in the campaign replaces their details and variable values.
- **From Contacts**: the **Browse Contacts** dialog picks people from your contact library; anyone already in the campaign is marked **In campaign**.
- **Search**: describe who you're looking for and add matches straight from [People Search](/docs/sourcing-with-people-search).

{/* 📸 Screenshot: the Import CSV dialog showing column mapping and preview */}

## 3. Build the sequence

The **Sequence** step is a visual flow from **Start** to **End**. Click the **+** on any connector to **Add Step**: **Email**, **SMS**, **LinkedIn Invite**, **LinkedIn Message**, **LinkedIn InMail**, **LinkedIn Visit**, or **WhatsApp**. Every step after the first gets a **Wait** delay you can set in days or weeks.

For email steps, pick a starter template (like **Professional Introduction** or **Gentle Reminder**) or choose **Write Custom**, then fill in the **Subject Line** and **Email Body**. Click **Variables** in any message field to insert personalization such as the recipient's first name, the application link, or your own company variables (see below). SMS and WhatsApp steps only go to recipients who have a phone number on file, and LinkedIn InMail requires a Premium, Recruiter, or Sales Navigator sending account.

{/* 📸 Screenshot: the sequence builder with an email step and the Add Step menu open */}

### Personalize with variables

Variables are placeholders in curly braces, like `{first_name}`, that Hivemind fills in for each recipient when the message sends. The **Variables** picker (or **Ctrl+/**, **⌘/** on Mac, while you're typing) lists three kinds:

- **Built-in variables**: details Hivemind already knows, such as the recipient's name and the application link.
- **Per lead**: one for each extra column you brought in with **Import CSV**, named after the column header. A column of portfolio links or referrer names can go straight into the message.
- **Custom**: your company's message variables, values you define once (a booking link, an office address, a signature line) and reuse in every campaign, in pipeline emails and texts, and in emails you write to a candidate. Changing the value updates every message that uses it. Create them right from the picker with **New variable**, or manage them in **Settings → Workspace Settings → Message Variables**.

To cover recipients with nothing to fill in, give a variable a fallback after a pipe: `{city|your area}` sends "your area" when a lead has no city. In the picker, click the arrow next to a variable to set its fallback before inserting it.

<Callout icon="💡" theme="info">
  Creating or editing company variables needs outreach or workspace edit access. Everyone else sees them read-only but can still insert them.
</Callout>

## 4. Configure settings and schedule

Click **Settings** to open **Campaign Settings**:

- **General**: the campaign name and the **Email Account**, **LinkedIn Account**, and **WhatsApp Account** used for sending.
- **Schedule**: **Send spacing** between sends, the **Sending window**, **Timezone**, and **Active days**, with a **Delivery preview** of the rollout. By default campaigns send on weekdays, 9:00–17:00, ten minutes apart.
- **Pipeline**: a **Linked Pipeline**. Recipients who apply through the campaign are automatically added to it. See [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline).

<Callout icon="⚠️" theme="warn">
  If your message uses the application link variable, you must link a pipeline. Otherwise launch is blocked with **Missing pipeline connection**.
</Callout>

## 5. Launch

The **Launch** step shows your recipients next to a **Sequence Preview** and lists anything left to fix (for example **No email account connected**). It also checks every variable you used: a token that isn't a real variable (usually a typo like `{frist_name}`) blocks the launch, because it would otherwise go out as literal text. Separately, Hivemind tells you how many leads have no value for each per-lead variable you used without a fallback. That warning doesn't block launch; those leads get empty text unless you add a fallback. Click **Launch to N recipients**, review the schedule and rollout plan in the **Launch Campaign** dialog, and confirm.

Campaigns move through **Draft**, **Active**, **Paused**, and **Completed**. On a live campaign, the **Manage** menu offers **Pause Campaign**, **Resume Campaign**, and **Send to New Recipients** for people added later.

## 6. Track progress

The campaign header shows delivery progress with **Sent**, **Replied**, **Applied**, and **Pending** counts (plus **Bounced** and **Opted Out** when relevant). Each recipient moves from **Pending** to **Sent**, then to **Replied** when they respond or **Applied** when they apply; replied, applied, bounced, and opted-out recipients stop receiving further steps. Row actions let you **Edit** a recipient, **Send Now** to skip the wait, or **Remove Prospect**.

## What's next

- Find new prospects with [Sourcing with People Search](/docs/sourcing-with-people-search)
- Connect your mailbox in [Email Integration & Inbox](/docs/email-integration-inbox)
- Build the pipeline applicants land in: [Creating a Pipeline](/docs/creating-a-pipeline)
