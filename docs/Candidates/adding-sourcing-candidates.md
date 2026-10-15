---
title: Adding & Sourcing Candidates
hidden: false
---

Candidates enter Hivemind through your pipeline's public application page, whether they found the link on a job board, your careers site, or an outreach email you sent them. This guide covers the inbound route, adding people yourself, proactive sourcing through Outreach, and the developer option for everything else.

## The application link: the front door

Every pipeline has its own public application page. Once a pipeline is out of draft, copy the link from any of these places:

- The pipeline's actions menu: choose **Application Link**, and you'll see a **"Link copied"** confirmation.
- The pipeline page title: click the share icon labeled **Copy application link**.
- The **Start** card in the pipeline editor: click the **Application link** row.

Active pipelines also get a **Share to LinkedIn** option in the pipeline page's **Manage** menu and in the pipeline's sidebar menu. See [LinkedIn Job Posting](/docs/linkedin-job-posting).

Post the link anywhere: job boards, social, email signatures. Active pipelines also appear on your [company page](/docs/your-company-page), where each role has its own job page with an **Apply now** button that leads to the same form. Everyone who completes the form becomes a candidate at your pipeline's first stage and starts moving through it automatically. For what the form looks like on their side, see [The Candidate Experience](/docs/the-candidate-experience).

{/* 📸 Screenshot: The pipeline actions menu open, with Application Link and Share to LinkedIn visible */}

<Callout icon="⚠️" theme="warn">
  New applications are only accepted while the pipeline is **Active**. Draft pipelines don't expose a link at all, and a deactivated pipeline shows visitors "This pipeline is no longer active", though candidates already mid-process can still finish their steps.
</Callout>

## Adding a candidate yourself

Not everyone needs to apply. For a referral you've already spoken to or someone who emailed their resume, click **Add candidate** in a pipeline's header (or on the **Candidates** page), fill in their details, and pick the stage they should enter at. To consider an existing candidate for another role, use **Copy to another pipeline** on their row. Both are covered step by step in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline#add-a-candidate-at-any-stage).

<Callout icon="💡" theme="info">
  There's no CSV upload into a pipeline. To bring in a larger group of people you found yourself, import them into Outreach (below) and invite them to apply.
</Callout>

## Sourcing proactively with Outreach

When you'd rather go find talent than wait for it, open **Outreach**. It has three tabs (**Search**, **Campaigns**, and **Contacts**) and four ways to build a prospect list:

- **People Search**: the default **Search** tab asks "who are you looking for?" Describe your ideal hire in plain language (e.g. "Senior React engineer in San Francisco, 5+ years experience") or stack precise filters: **Job title**, **Seniority**, **Skill**, **Location**, **Industry**, **Company**, **Company size**, **Company type**, and **Experience**. Select results and click **Add to campaign**. Full guide: [Sourcing with People Search](/docs/sourcing-with-people-search).
- **Add Manually**: enter one prospect at a time: **Name** and **Email** (required), plus optional phone, LinkedIn URL, and notes.
- **Import CSV**: upload a spreadsheet of prospects (CSV, up to 10 MB). Under **Contact details**, Hivemind auto-detects which column holds each contact field (**Name**, **Email**, **Phone**, **Notes**, **LinkedIn**); an email column is required. Under **Variables**, every other column can be imported as a per-lead variable for your messages or left as **Not imported**. A **Preview** shows the first rows and flags invalid emails. Finish with **Import**. See [Outreach Campaigns](/docs/outreach-campaigns) for using variables.
- **From Contacts**: reuse people already saved in your **Contacts** library.

{/* 📸 Screenshot: The Outreach Search tab with the natural-language search box and filter chips (Job title, Seniority, Skill, Location…) */}

## Turning prospects into candidates

Prospects become candidates when they apply, and your campaign makes that seamless. In your campaign's settings, open the **Linked Pipeline** tab and pick a pipeline: "When a recipient applies through this campaign, they will be automatically added to the linked pipeline for further processing."

Your outreach emails can include the pipeline's application link; when a prospect clicks it and submits the form, they land in the linked pipeline as a tracked candidate, and you'll see which campaign sourced them. A reply alone doesn't convert anyone; the application does. See [Outreach Campaigns](/docs/outreach-campaigns) for sequencing and follow-ups.

## For developers: the API

Have candidates in another system? Your team can push them in programmatically with the public API, using an API key generated in **Settings**. See [Public API: Getting Started](/docs/public-api-getting-started).

## What's next

- Find great people fast with [Sourcing with People Search](/docs/sourcing-with-people-search)
- Build the email sequence in [Outreach Campaigns](/docs/outreach-campaigns)
- Watch arrivals in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Review anyone's record in [Candidate Profiles](/docs/candidate-profiles)
