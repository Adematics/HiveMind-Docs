---
title: Managing Candidates in a Pipeline
hidden: false
---

Once a pipeline is live, candidates flow through it on their own. Your job is to watch progress, clear review checkpoints, and occasionally move someone by hand. This page covers the applicants table, adding candidates yourself, and the tools you have for steering individual applicants.

## 1. Open the applicants table

From any pipeline, open the **Manage** menu and choose **Applicants**. You'll land on the pipeline's candidates table, showing every applicant with columns like **Name**, **Email**, **Phone Number**, **Resume** (with a **View Resume** link), **Score**, **Status**, **Current Node**, **Last Active**, **Date Created**, and **Outcome**. More columns (**Skills**, **Hired**, **Referral Tag**, **Node Status**, **Candidate Review Status**) can be toggled on via the **View** button's **View Settings** panel. The pipeline header also has **Add candidate**, **Inbox**, and the **Manage** menu.

{/* 📸 Screenshot: a pipeline's candidates table with Status chips and Current Node badges visible */}

Each candidate's **Status** chip tells you where things stand: **Ongoing** (moving through the pipeline), **Completed** (their path through the pipeline has ended), or **Pending Credits** (paused until your workspace has credits; see [Credits & Billing](/docs/credits-billing)). **Outcome** is separate from status and records the result: **Passed**, **Rejected**, **Withdrawn**, or **Hired**. Hover it to see who set it (Hivemind, a teammate, or a connected ATS) and why.

A badge next to a candidate's name shows how they got in when it wasn't through the application form: **Manual** (added by your team), **Copied** (copied from another pipeline), or the integration that sent them, such as **Ashby**, **Greenhouse**, **Webhook**, or **API**. Use the search box and column filters to narrow the list, and click a candidate's name to open their details panel, or jump to their full record in [Candidate Profiles](/docs/candidate-profiles).

## 2. How candidates get in

Candidates enter a pipeline in a few ways:

- **The application link.** Anyone who applies through the pipeline's public application page enters at the first step. Copy it with the **Application Link** menu item.
- **Linked outreach campaigns.** Campaigns connected to the pipeline via the **Outreach** row on the Start card feed the people they engage into the pipeline. See [Outreach Campaigns](/docs/outreach-campaigns).
- **You add them.** Put someone in at any stage without asking them to apply, or copy an existing candidate in from another pipeline. See below.

### Add a candidate at any stage

Use this for a referral you've already spoken to, someone who applied by email, or anyone you want to drop straight into a later step.

1. Click **Add candidate** in the pipeline header (or on the **Candidates** page, where you'll pick the pipeline first). Only active pipelines accept new candidates; drafts and closed pipelines are shown but can't be picked.
2. **Details**: fill in the pipeline's application form fields. The resume is optional: leave it empty and a placeholder resume is generated so the record isn't missing one.
3. **Entry stage**: pick the step they enter at. Each step says what happens the moment they land:
   - **Runs the pipeline from the top**: they enter as if they had just applied.
   - **Runs immediately**: the step fires for real (an Email step sends that email, Resume Screening scores the resume).
   - **Waits for the candidate**: they sit there until they complete the step, such as an assessment or interview booking.
   - **Waits for you**: they're parked until your team acts, as at a Candidate Review.
   - **Waits for an external call**: they're parked until a webhook moves them on.
4. Click **Add to pipeline**.

No email is sent on entry by itself; only the steps they enter at and after do what they normally do.

{/* 📸 Screenshot: the Add candidate dialog on the Entry stage step, with the stage list and behaviour labels */}

<Callout icon="⚠️" theme="warn">
  A stage marked **Runs immediately** really runs. Dropping someone on an email or SMS step sends that message as soon as you click **Add to pipeline**.
</Callout>

### Copy a candidate to another pipeline

To consider someone for a second role, select their row (or right-click it) in any candidates table and choose **Copy to another pipeline**. Pick the target pipeline, review the details, and choose the entry stage the same way as above, then click **Copy to pipeline**.

The original application stays exactly where it was. The copy reuses their resume, and where the new pipeline's form asks for something the original application didn't, a **From original** picker lets you pull an answer across from their original application, or you can type one in.

## 3. Move a candidate: skip ahead or rewind

Sometimes automation isn't the right call: a referral shouldn't retake a test, or someone deserves a second shot at an assessment. Click the candidate's **Current Node** badge in the table to open the **Manage Progress** dialog, which lists the pipeline's steps as a timeline with the candidate's **Current** position marked. Select a target step, and the action becomes:

- **Skip Ahead**: jumps the candidate forward. The **Confirm Skip** dialog warns that all intermediate steps will be skipped and the candidate won't complete those assessments.
- **Rewind**: moves the candidate back. The **Confirm Rewind** dialog shows exactly which responses will be permanently deleted, and warns the candidate will need to redo all subsequent assessments.

{/* 📸 Screenshot: the Manage Progress dialog with the step timeline and the Skip Ahead button */}

<Callout icon="⚠️" theme="warn">
  Rewinding deletes the candidate's responses for every step after the target. **This action cannot be undone.** Review the preview in the confirmation dialog before clicking **Confirm Rewind**.
</Callout>

Only assessment-type steps (skills tests, personality, IQ, AI phone calls) are valid targets; automated steps like emails or delays don't appear in the timeline.

## 4. Clear manual review checkpoints

Candidates sitting at a **Candidate Review** step (or awaiting an interview verdict) wait for a human decision. These show up in three places:

- **Your Inbox**: as tasks like *"Review: {name}"* or *"Video Interview Review: {name}"*, filterable under **Candidate Review**.
- **The candidate's profile**: an **Awaiting manual review** card.
- **The pipeline editor**: click the review node to see everyone *awaiting review* at that step.

Wherever you find them, the decision is the same two buttons: **Approve** advances the candidate to the next step; **Disapprove** ends their journey. You can check their scores and responses via the **Details** link before deciding. The **Candidate Review Status** column tracks outcomes as **Approved**, **Disapproved**, or **Pending**.

<Callout icon="💡" theme="info">
  Get review tasks on the go: manual review notifications also reach the [mobile app](/docs/notifications-mobile-app), so checkpoints never bottleneck your pipeline.
</Callout>

## 5. Export to CSV

Click **Export** in the table toolbar. The **Export data** dialog shows how many candidates and columns you're about to download. It exports every row matching your current filters and search (not just the visible page), using the columns you have shown. Click **Export** to download the CSV.

Select one candidate (or right-click a row) for **Send Email**, **Add to list**, **Copy to another pipeline**, and **Delete**. Select several to **Send Email**, **Add to list**, or **Delete** in bulk. Lists are covered in [Candidate Lists](/docs/candidate-lists).

## What's next

- Dig into an individual applicant in [Candidate Profiles](/docs/candidate-profiles)
- See what candidates experience at each step in [The Candidate Experience](/docs/the-candidate-experience)
- Review test results in [Reviewing Results](/docs/reviewing-results)
- Close your finalists with [Offers](/docs/offers)
