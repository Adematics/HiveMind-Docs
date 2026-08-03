---
title: Managing Candidates in a Pipeline
hidden: false
---

Once a pipeline is live, candidates flow through it on their own — your job is to watch progress, clear review checkpoints, and occasionally move someone by hand. This page covers the candidates view and the tools you have for steering individual applicants.

## 1. Open the candidates view

From any pipeline, open the **Manage** menu and choose **Applicants**. You'll land on the pipeline's candidates table, showing every applicant with columns like **Name**, **Email**, **Phone**, **Resume** (with a **View Resume** link), **Score**, **Status**, **Current Node**, **Last Active**, and **Date Created**. More columns — **Skills**, **Hired**, **Referral Tag**, **Node Status**, **Review Status** — can be toggled on via the **View** button's **View Settings** panel.

{/* 📸 Screenshot: a pipeline's candidates table with Status chips and Current Node badges visible */}

Each candidate's **Status** chip tells you where things stand: **Ongoing** (moving through the pipeline), **Completed** (reached the end), or **Pending Credits** (paused until your workspace has credits — see [Credits & Billing](/docs/credits-billing)). Use the search box and column filters to narrow the list, and click a candidate's name to open their details panel — or jump to their full record in [Candidate Profiles](/docs/candidate-profiles).

## 2. How candidates get in

There's no manual "add candidate" button — candidates enter a pipeline in two ways:

- **The application link.** Anyone who applies through the pipeline's public application page enters at the first step. Copy it with the **Application Link** menu item.
- **Linked outreach campaigns.** Campaigns connected to the pipeline via the **Outreach** button on the Start node feed the people they engage into the pipeline. See [Outreach Campaigns](/docs/outreach-campaigns).

## 3. Move a candidate: skip ahead or rewind

Sometimes automation isn't the right call — a referral shouldn't retake a test, or someone deserves a second shot at an assessment. Click the candidate's **Current Node** badge in the table to open the **Manage Progress** dialog, which lists the pipeline's steps as a timeline with the candidate's **Current** position marked. Select a target step, and the action becomes:

- **Skip Ahead** — jumps the candidate forward. The **Confirm Skip** dialog warns that all intermediate steps will be skipped and the candidate won't complete those assessments.
- **Rewind** — moves the candidate back. The **Confirm Rewind** dialog shows exactly which responses will be permanently deleted, and warns the candidate will need to redo all subsequent assessments.

{/* 📸 Screenshot: the Manage Progress dialog with the step timeline and the Skip Ahead button */}

<Callout icon="⚠️" theme="warn">
  Rewinding deletes the candidate's responses for every step after the target — **this action cannot be undone**. Review the preview in the confirmation dialog before clicking **Confirm Rewind**.
</Callout>

Only assessment-type steps (skills tests, personality, IQ, AI phone calls) are valid targets — automated steps like emails or delays don't appear in the timeline.

## 4. Clear manual review checkpoints

Candidates sitting at a **Candidate Review** step (or awaiting an interview verdict) wait for a human decision. These show up in three places:

- **Your Inbox** — as tasks like *"Review: {name}"* or *"Video Interview Review: {name}"*, filterable under **Candidate Review**.
- **The candidate's profile** — an **Awaiting manual review** card.
- **The pipeline editor** — click the review node to see everyone *awaiting review* at that step.

Wherever you find them, the decision is the same two buttons: **Approve** advances the candidate to the next step; **Disapprove** ends their journey. You can check their scores and responses via the **Details** link before deciding. The **Review Status** column tracks outcomes as **Approved**, **Disapproved**, or **Pending**.

<Callout icon="💡" theme="info">
  Get review tasks on the go — manual review notifications also reach the [mobile app](/docs/notifications-mobile-app), so checkpoints never bottleneck your pipeline.
</Callout>

## 5. Export to CSV

Click **Export** in the table toolbar. The **Export data** dialog shows how many candidates and columns you're about to download — it exports every row matching your current filters and search (not just the visible page), using the columns you have shown. Click **Export** to download the CSV.

You can also select candidates in the table to **Send Email** in bulk or **Delete** them.

## What's next

- Dig into an individual applicant in [Candidate Profiles](/docs/candidate-profiles)
- See what candidates experience at each step in [The Candidate Experience](/docs/the-candidate-experience)
- Review test results in [Reviewing Results](/docs/reviewing-results)
- Close your finalists with [Offers](/docs/offers)
