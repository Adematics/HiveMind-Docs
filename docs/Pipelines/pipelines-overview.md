---
title: Pipelines Overview
hidden: false
---

A pipeline is your hiring process turned into an automated workflow. You lay out the steps a candidate should go through (resume screening, assessments, phone calls, interviews, an offer), and Hivemind moves each applicant through them for you, only pausing where a human decision is needed.

## The visual builder

Every pipeline is built on a visual canvas. Steps appear as connected cards flowing from a **Start** circle down to an **End** circle, and you build your process by dragging steps in from the palette on the left, which is organized into **Communication**, **Automated Assessment**, **Interviews**, **Flow Control**, and **API** sections. Click any step to configure it, then click **Save** to store your changes.

{/* 📸 Screenshot: the pipeline editor canvas with the node palette on the left and a Start → Application Form → End flow on the canvas */}

The **Start** circle is where candidates enter: it carries the pipeline's **Application Link** badge, an **Outreach** button for linking sourcing campaigns, and a **Referral Link** badge. See the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference) for every step you can add.

<Callout icon="💡" theme="info">
  Once a pipeline has active candidates, the editor switches to a limited editing mode: you can still adjust each step's configuration, but structural changes (adding or removing steps) are disabled to protect candidates mid-process.
</Callout>

## Automatic candidate progression

When a candidate finishes a step, Hivemind immediately advances them along the flow. Automated steps (resume scoring, emails, SMS, branching, delays) run on their own, one after another. Steps that need something from the candidate (an assessment, an AI phone call, picking interview times) email the candidate a personal link and wait. Steps that need something from *you*, like **Candidate Review**, surface in your **Inbox** and pause the candidate until someone on your team decides.

Branching steps can route candidates down different paths, for example sending strong scorers straight to an interview. See [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline) for watching and steering candidates once they're in.

## Draft vs. active

On the **My Pipelines** page you can filter pipelines by **Active**, **Drafts**, **Closed**, and **All**. Status matters:

- **Draft**: the pipeline exists but can't accept applicants, and its application link isn't available yet. Drafts show a **Draft** badge and their status card reads *"Draft — complete setup and activate to accept applications."*
- **Active**: the pipeline is live and its public application link works.
- **Inactive**: a previously active pipeline that's been switched off. Visitors to its link see *"This pipeline is no longer active"* along with a link to your company's other open positions.

To go live, open the pipeline and choose **Activate** from its **Manage** menu. Hivemind first checks that every step is fully configured and that the job details (title, description, location, workplace type, job type) are filled in; otherwise you'll see **Cannot Activate** or **Incomplete Pipeline** messages pointing at anything missing. On success: *"Your pipeline is now live and accepting applications."*

{/* 📸 Screenshot: the My Pipelines page showing pipeline cards with a Draft badge, candidate counts, and the pipeline menu open */}

## The public application link

Every active pipeline has its own public application page where candidates apply with their name, email, phone number, resume, and LinkedIn profile. Grab the URL with the **Application Link** item in the pipeline menu; it copies the link to your clipboard so you can post it on job boards, your careers page, or anywhere else. Active pipelines can also use **Share to LinkedIn**.

<Callout icon="⚠️" theme="warn">
  The **Application Link** option only appears once a pipeline is out of draft. Activate first, then share.
</Callout>

Candidates who apply enter at the first step and progress automatically. Read [The Candidate Experience](/docs/the-candidate-experience) to see their side of it.

## What's next

- Build your first one in [Creating a Pipeline](/docs/creating-a-pipeline)
- Learn every building block in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Track applicants in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Fill your pipeline proactively with [Outreach Campaigns](/docs/outreach-campaigns)
