---
title: FAQ / Common Issues
hidden: false
---

Quick answers to the questions our support team hears most. If yours isn't here, reach out. See [Contact & Support](/docs/contact-support).

## Why isn't my application link working?

If candidates see **"This pipeline is no longer active"**, the pipeline is still a draft or has been closed. New pipelines always start as drafts and can't accept applicants. Open the pipeline and click **Activate** to take its application link live. See [Quick Start](/docs/quick-start).

## Why aren't emails going out to candidates?

Almost always: no mailbox is connected. Hivemind sends candidate emails through *your* email account, so open **Settings → Email Services**, click **Add Account**, and connect **Google** (Gmail & Google Workspace), **Microsoft** (Outlook & Microsoft 365), or any provider via **SMTP**. Then use **Test Email Accounts** to confirm sending works. Details in [Email Integration & Inbox](/docs/email-integration-inbox).

## My Outlook account says "Admin approval required." What do I do?

Your Microsoft 365 organization only lets an admin approve mail access for outside apps. If you're a Microsoft admin, click **I'm an admin, approve now**. Otherwise click **Copy approval link for your IT admin** and send it to them. Once they've approved it, go back to **Settings → Email Services** and connect the account again. See [Email Integration & Inbox](/docs/email-integration-inbox).

## What are credits, and what happens when I run out?

Credits power Hivemind's AI actions: assessment evaluation, AI voice interviews, outreach sends, people search, and pipeline automation. Email signups start with **300 free credits**. At zero, those actions stop with an "Insufficient credits" message (candidates can't be advanced through AI stages, calls won't place, campaigns won't launch) until you top up or upgrade in **Settings → Credits**. See [Credits & Billing](/docs/credits-billing).

## Can I import candidates from a CSV?

Not directly into a pipeline. CSV import exists for **outreach campaigns**: import a spreadsheet of prospects, then invite them to apply through an [outreach campaign](/docs/outreach-campaigns). Extra columns in the file become per-lead variables you can use in your messages. To put one specific person into a pipeline, use **Add candidate** in the pipeline's header instead. You *can* export a pipeline's candidates to CSV anytime.

## How do candidates get into my pipeline?

Four ways: they apply through the pipeline's public application link, they find the role on [your company page](/docs/your-company-page), you source them proactively with [People Search](/docs/sourcing-with-people-search) and [outreach campaigns](/docs/outreach-campaigns), or you add them yourself with **Add candidate** in the pipeline's header and choose the stage they start at. More in [Adding & Sourcing Candidates](/docs/adding-sourcing-candidates).

## How do I change my password?

Go to **Settings → Account Settings → Change Password**. You'll need your current password to set a new one.

## A teammate says a page or Settings tab is missing. Why?

Their role doesn't have permission for it. Tabs like **Workspace Settings**, **Roles**, and **Credits** only appear for roles allowed to manage them. An Owner or Admin can change their role, or build a custom role with exactly the right access. See [Team Members & Roles](/docs/team-members-roles).

## My company page doesn't show the design I built. Why?

You haven't published it yet. Until you click **Publish** in the page builder, visitors see a simple default layout; drafts are never shown live. If you've published before, the toolbar shows **Unpublished changes** when your latest edits aren't live yet. Publish, then refresh the live page. See [Your Company Page](/docs/your-company-page).

## I left the career page builder and my changes are gone. Can I get them back?

Probably. The builder only saves to your workspace when you click **Save** (or **Publish**), but it keeps unsaved work on your device. Reopen **Settings → Career Page** on the same browser and click **Restore** on the notice at the top.

## Where do I change our logo or cover image on the career page?

In **Settings → Workspace Settings**, not in the page builder. The logo, cover, and company name there feed your career page, the candidate portal, and the rest of Hivemind. The **Show cover on candidate portal** switch lives there too and applies as soon as you save.

## Why does my message show a placeholder like `{first_name}` instead of a real value?

Either the variable doesn't exist (often a typo) or the recipient has no value for it. Outreach campaigns catch the first case before launch: a token that isn't a real variable blocks the launch. For blank values, add a fallback after a pipe, like `{city|your area}`. Company-wide values such as a booking link live in **Settings → Workspace Settings → Message Variables**. See [Outreach Campaigns](/docs/outreach-campaigns#personalize-with-variables).

## I changed the accent colour. Why doesn't my teammate see it?

The **Appearance** settings (theme and accent colour) are personal and saved in your browser, so each person picks their own. Your public career page's accent colour is separate and set in the page builder's **Page settings**.

## Why isn't a job showing on my company page?

The **Open Positions** section only lists **active** pipelines; drafts and closed pipelines never appear. If you've turned off auto-pull and are hand-picking pipelines, check that the missing one is selected.

## Why can't I edit or delete a role?

**System roles** (Admin, Recruiter, Hiring Manager, and friends) can't be edited; clone one into a custom role instead. A custom role can only be deleted once no members are assigned to it; reassign them first.

## Can candidates see their scores and pipeline stage?

That's up to you. **Settings → Workspace Settings** has switches for **Show Pipeline in Candidate View**, **Show Assessment Score**, **Show Resumatic Summary (Public Reports)**, and **Show Cheating Analysis (Public Reports)**. Turn any of them off to keep that information internal.

<Callout icon="💡" theme="info">
  Interviews not scheduling? Check that **Google Calendar** (and **Google Meet** or **Zoom**) are connected in the **Calendar** page's **Connections** tab. Scheduling pulls availability from your connected calendar. See [Calendar & Scheduling](/docs/calendar-scheduling).
</Callout>

## What's next

- Still stuck? [Contact & Support](/docs/contact-support)
- Set up the essentials in [Account & Workspace Setup](/docs/account-workspace-setup)
- Learn the building blocks in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
