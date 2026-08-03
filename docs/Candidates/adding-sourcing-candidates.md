---
title: Adding & Sourcing Candidates
hidden: false
---

Candidates enter Hivemind through your pipeline's public application page — whether they found the link on a job board, your careers site, or an outreach email you sent them. This guide covers the inbound route, proactive sourcing through Outreach, and the developer option for everything else.

## The application link — the front door

Every pipeline has its own public application page. Once a pipeline is out of draft, copy the link from two places:

- The pipeline's actions menu — choose **Application Link**, and you'll see a **"Link copied"** confirmation.
- The pipeline page title — click the share icon labeled **Copy application link**.

Active pipelines also get a **Share to LinkedIn** option in the same menu for one-click posting.

Post the link anywhere — job boards, your careers page, social, email signatures. Everyone who completes the form becomes a candidate at your pipeline's first stage and starts moving through it automatically. For what the form looks like on their side, see [The Candidate Experience](/docs/the-candidate-experience).

{/* 📸 Screenshot: The pipeline actions menu open, with Application Link and Share to LinkedIn visible */}

<Callout icon="⚠️" theme="warn">
  New applications are only accepted while the pipeline is **Active**. Draft pipelines don't expose a link at all, and a deactivated pipeline shows visitors "This pipeline is no longer active" — though candidates already mid-process can still finish their steps.
</Callout>

<Callout icon="💡" theme="info">
  There's intentionally no "Add candidate" button or CSV upload into a pipeline. Every candidate goes through the application form, so each one arrives with the same structured data and starts at the same first stage — no half-filled records. To bring in people you found yourself, use Outreach below.
</Callout>

## Sourcing proactively with Outreach

When you'd rather go find talent than wait for it, open **Outreach**. It has three tabs — **Search**, **Campaigns**, and **Contacts** — and four ways to build a prospect list:

- **People Search** — the default **Search** tab asks "who are you looking for?" Describe your ideal hire in plain language (e.g. "Senior React engineer in San Francisco, 5+ years experience") or stack precise filters: **Job title**, **Seniority**, **Skill**, **Location**, **Industry**, **Company**, **Company size**, **Company type**, and **Experience**. Select results and click **Add to campaign**. Full guide: [Sourcing with People Search](/docs/sourcing-with-people-search).
- **Add Manually** — enter one prospect at a time: **Name** and **Email** (required), plus optional phone, LinkedIn URL, and notes.
- **Import CSV** — upload a spreadsheet of prospects (CSV, up to 10MB). Hivemind auto-detects your headers in a **Column Mapping** step where you match columns to **Name**, **Email**, **Phone**, **Notes**, or **LinkedIn**, previews the first rows, and flags invalid emails. Email is required — rows without one are skipped. Finish with **Import**.
- **From Contacts** — reuse people already saved in your **Contacts** library.

{/* 📸 Screenshot: The Outreach Search tab with the natural-language search box and filter chips (Job title, Seniority, Skill, Location…) */}

## Turning prospects into candidates

Prospects become candidates when they apply — and your campaign makes that seamless. In your campaign's settings, open the **Linked Pipeline** tab and pick a pipeline: "When a recipient applies through this campaign, they will be automatically added to the linked pipeline for further processing."

Your outreach emails can include the pipeline's application link; when a prospect clicks it and submits the form, they land in the linked pipeline as a tracked candidate — you'll see which campaign sourced them. A reply alone doesn't convert anyone; the application does. See [Outreach Campaigns](/docs/outreach-campaigns) for sequencing and follow-ups.

## For developers: the API

Have candidates in another system? Your team can push them in programmatically with the public API, using an API key generated in **Settings**. See [Public API: Getting Started](/docs/public-api-getting-started).

## What's next

- Find great people fast with [Sourcing with People Search](/docs/sourcing-with-people-search)
- Build the email sequence in [Outreach Campaigns](/docs/outreach-campaigns)
- Watch arrivals in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Review anyone's record in [Candidate Profiles](/docs/candidate-profiles)
