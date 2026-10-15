---
title: Pipelines Overview
hidden: false
---

A pipeline is your hiring process turned into an automated workflow. You lay out the steps a candidate should go through (resume screening, assessments, phone calls, interviews, an offer), and Hivemind moves each applicant through them for you, only pausing where a human decision is needed.

## The visual builder

Every pipeline is built on a visual canvas. Steps appear as connected cards flowing down from a **Start** card, and you build your process by dragging steps in from the palette on the left, which is organized into **Communication**, **Automated Assessment**, **Interviews**, **Reviews**, **Flow Control**, and **Integrations** sections. Drop a step on a **Drag a step here** slot, click any step to configure it, then click **Save** in the header to store your changes.

{/* 📸 Screenshot: the pipeline editor canvas with the node palette on the left and a Start → Application Form flow on the canvas */}

The **Start** card is where candidates enter: it has rows for the pipeline's **Application link** (click to copy), **Outreach** for linking sourcing campaigns, and **Referral link**. See the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference) for every step you can add.

<Callout icon="💡" theme="info">
  Once a pipeline has active candidates, the editor switches to **Limited Edit Mode**: you can still adjust each step's configuration, but structural changes (adding or removing steps) are disabled to protect candidates mid-process.
</Callout>

## Automatic candidate progression

When a candidate finishes a step, Hivemind immediately advances them along the flow. Automated steps (resume screening, emails, SMS, branching, delays) run on their own, one after another. Steps that need something from the candidate (an assessment, an AI phone call, picking interview times) email the candidate a personal link and wait. Steps that need something from *you*, like **Candidate Review**, surface in your **Inbox** and pause the candidate until someone on your team decides.

Branching steps can route candidates down different paths, for example sending strong scorers straight to an interview. See [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline) for watching and steering candidates once they're in.

## The My Pipelines table

The **Inbound** section of the sidebar lists your pipelines; click **View all** there to open the full **My Pipelines** page. It's a table built for working across many roles at once:

- **Status tabs**: **Active** (the default), **Drafts**, **Closed**, and **All**.
- **Columns**: **Pipeline**, **Status**, **Role**, **Candidates**, **In Progress**, **Hired**, **Location**, and **Created**. **Job Type**, **Workplace**, and **Updated** are hidden by default; switch them on from the view settings.
- **Search, filter, and sort**: search by pipeline name or role, filter on columns like job type or workplace, and sort by any sortable column.
- **Dashboard shortcut**: hover a pipeline's name and click **Dashboard** to open its analytics.

{/* 📸 Screenshot: the My Pipelines table with the Active / Drafts / Closed / All tabs, candidate counts, and a row's actions menu open */}

Select a single row (or right-click it) to get its actions: **View Dashboard**, **Edit Pipeline**, **Applicants**, **Application Link** (once out of draft), **Activate** or **Deactivate**, **Duplicate**, and **Delete**. Select several rows to **Delete** them in bulk.

- **Duplicate** asks for a new **Pipeline Name** and creates a copy of the job details and every step as a new draft.
- **Delete** permanently removes the pipeline and its configuration. Pipelines that already have candidates can't be deleted; they're skipped, and you're pointed to their candidates instead.
- **Deactivate** asks you to confirm first, since it stops new candidates from applying.

The same actions (plus **Share to LinkedIn** on active pipelines) live in the **Manage** menu inside each pipeline.

## Draft vs. active

Status matters:

- **Draft**: the pipeline exists but can't accept applicants, and its application link isn't available yet.
- **Active**: the pipeline is live and its public application link works.
- **Closed**: a previously active pipeline that's been deactivated. Visitors to its application link see *"This pipeline is no longer active"* along with a link to your company's open positions. Candidates already mid-process can still finish their steps.

To go live, open the pipeline and click **Activate** in its header. Hivemind first checks that every step is fully configured and that the job details (title, description, location, workplace type, job type) are filled in; otherwise it highlights the steps that need attention or shows an **Incomplete Pipeline** message pointing at the missing details. On success: *"Your pipeline is now live and accepting applications."* Choosing **Activate** from the table on a draft or closed pipeline takes you into the pipeline to finish the same check.

## The public application link

Every active pipeline has its own public application page where candidates apply with the form you configured. Grab the URL with the **Application Link** item in the pipeline menu, the **Application link** row on the Start card, or the share icon next to the pipeline's name; each copies the link to your clipboard so you can post it on job boards, your careers page, or anywhere else. Active pipelines also appear on your [company page](/docs/your-company-page), each with its own job page, and can use **Share to LinkedIn**.

<Callout icon="⚠️" theme="warn">
  The **Application Link** option only appears once a pipeline is out of draft. Activate first, then share.
</Callout>

Candidates who apply enter at the first step and progress automatically. Read [The Candidate Experience](/docs/the-candidate-experience) to see their side of it.

## What's next

- Post your first role end to end with [How to Post a Job](/docs/post-a-job)
- Build your first one in [Creating a Pipeline](/docs/creating-a-pipeline)
- Learn every building block in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Track applicants in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Fill your pipeline proactively with [Outreach Campaigns](/docs/outreach-campaigns)
