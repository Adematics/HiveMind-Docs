---
title: Creating a Pipeline
hidden: false
---

There are two ways to build a pipeline: let **Hive**, the AI chat builder, assemble one from a few quick answers, or fill in the **Manual** form and design the steps yourself. Both live on the same page: go to **My Pipelines** and click **New Pipeline**, then pick a tab at the top of the create screen.

## 1. Build with Hive (the AI chat builder)

**Hive** is the default tab. It opens a chat that starts with *"Let's create a new pipeline. Pick a starting point below:"* and walks you through everything:

1. **Pick a starting point.** Choose a template: **Simple Pipeline** (Resume Screen → Interview), **Phone Prescreen** (Resume Screen → Phone Call → Interview), or **Skills Prescreen** (Resume Screen → Assessment → Review → Interview). If you've built pipelines before, a **Start from your pipelines** section lets you reuse one. You can also click **Skip for now** to continue with the simple template.
2. **Select the role.** Search for the position you're hiring for (e.g. Frontend Developer).
3. **Pick the required skills.** Hive suggests skills for the role; select at least one and click **Continue**.
4. **Choose a seniority level**: **Intern**, **Junior**, **Mid Level**, **Senior**, **Lead**, or **Principal**.
5. **Set up the interview step.** Pick your **Interviewers** from your team and a **Meeting Platform** (**Google Meet**, or **Zoom** if Zoom is connected), created on the host interviewer's connected account. Your timezone is picked up automatically.
6. **Add more details, or not.** Choose **Add More Details** to specify a **Location**, **Contract Type** (Full-Time, Part-Time, Contract, Volunteer, Internship, Other), **Work Type** (Remote, Hybrid, In-Office), and any notes, or choose **Create Pipeline Now** to skip straight ahead. These are the same job-type and workplace options the Manual form uses.
7. **Review the summary**: template, role, skills, seniority, work preferences, interview setup, and notes. Then click **Create Pipeline**.

{/* 📸 Screenshot: the Hive chat showing the three template cards (Simple Pipeline, Phone Prescreen, Skills Prescreen) */}

Hive then gets to work. You'll watch it move through **Generating job description**, **Composing assessment**, **Configuring pipeline nodes**, and **Finalizing**. When it's done you'll see *"Pipeline created."* with links to **View Pipeline** and, if your template included one, **View Assessment**.

<Callout icon="💡" theme="info">
  Hive-built pipelines are created **already active**, so the public application link works immediately. Review the generated steps and [assessment](/docs/creating-editing-assessments) before you share the link widely.
</Callout>

## 2. Build manually

The **Manual** tab is a single form for the job itself. Only two fields are required to create the pipeline:

- **Job Title** (required): the role candidates will see, e.g. *Backend Engineer*.
- **Seniority**: optional, from **Intern** to **Principal**. When set, it's added to the front of the job title (Senior + Backend Engineer becomes *Senior Backend Engineer*).
- **Pipeline name** (required): your internal name for the pipeline, e.g. *Backend Hiring Q3*. It must be unique in your workspace.
- **Workplace Type**: **Remote**, **Hybrid**, or **In-Office**.
- **Location**: for Hybrid and In-Office roles, pick a **City** and **Country**. For Remote roles this becomes a **Region** picker (Worldwide, EMEA, Americas, APAC, and more).
- **Job Type**: **Full-Time**, **Part-Time**, **Contract**, **Volunteer**, **Internship**, or **Other**.
- **Description**: the job description, in an editor that supports formatting.

{/* 📸 Screenshot: the Manual tab showing Job Title, Seniority, Pipeline name, Workplace Type, Location, Job Type, and the Description editor */}

### Draft the description with AI

You don't have to write the description from an empty box. Once a job title is filled in, click **Draft with AI** above the editor. A small panel opens where you can add optional notes (team, mission, must-have tools, salary range), then click **Generate**. Hivemind writes a description from the job title, seniority, location, and work setup you've entered, and puts it in the editor for you to edit like any other text.

If the editor already has text, the button reads **Regenerate with AI** instead. Regenerating writes a fresh draft from the job details and **replaces** what's in the editor, so copy anything you want to keep first.

### Preview the posting

Click **Preview posting** to see the job the way a candidate will read it: title, company, location, workplace and job type, and the description. You can click **Create Pipeline** straight from the preview.

At the bottom of the form, a short note tells you whether the pipeline is ready to go live, or which details (location, workplace type, job type, description) it still needs before it can be activated. Missing details never block creation; they only block activation.

{/* 📸 Screenshot: the Preview posting dialog showing the job as a candidate sees it */}

Click **Create Pipeline**. Hivemind attaches a default flow (Start → Application Form) and you land directly in the visual editor, where you drag in steps from the palette and connect them. See the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference) for what each one does.

## 3. Edit job details later

The same fields live in every existing pipeline's settings. Open the pipeline and click **Settings** in the header, then the **General** tab. You get the same **Job Title**, **Seniority**, **Pipeline name**, **Workplace Type**, **Location**, **Job Type**, and **Description** fields, the same **Draft with AI** button, and **Preview posting**. Click **Save Changes** when you're done.

On an active pipeline, every job detail must stay filled in: if one is empty, saving shows **Missing Fields** and names exactly what's missing.

The **Settings** dialog also has **Members**, **Webhook**, **Ashby**, **Greenhouse**, and **Referral** tabs.

## 4. Activate it

Manually created pipelines start as **drafts**, which can't accept applicants. When your flow is ready, click **Activate** in the pipeline header. Hivemind validates the pipeline first:

- Every step must be fully configured. Otherwise you'll see a message like *"2 steps need attention"*, and the broken steps are marked in red on the canvas. Open one to fix its settings.
- The job details must be complete. Otherwise you'll see **Incomplete Pipeline** (*"Please fill in all job details in Settings before activating."*) and the settings open so you can fill them in.

Once it passes, you'll get **Pipeline Activated**: *"Your pipeline is now live and accepting applications."* The **Application Link** item appears in the **Manage** menu so you can copy and share the public application page. If you have a LinkedIn account connected, Hivemind also offers to share the new job to LinkedIn (see [LinkedIn Job Posting](/docs/linkedin-job-posting)).

<Callout icon="⚠️" theme="warn">
  Connect a mailbox in **Settings → Email Services** before activating, since automated candidate emails can't send without one. See [Email Integration & Inbox](/docs/email-integration-inbox).
</Callout>

## What's next

- Follow the whole flow end to end in [How to Post a Job](/docs/post-a-job)
- Understand every step type in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Watch applicants arrive in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Fine-tune generated tests in [Creating & Editing Assessments](/docs/creating-editing-assessments)
- See what applicants experience in [The Candidate Experience](/docs/the-candidate-experience)
