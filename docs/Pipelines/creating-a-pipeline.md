---
title: Creating a Pipeline
hidden: false
---

There are two ways to build a pipeline: let **Hive**, the AI chat builder, assemble one from a few quick answers, or start from a blank canvas with the **Manual** form. Both live on the same page: go to **My Pipelines** and click **New Pipeline**, then pick a tab at the top of the **Create Pipeline** screen.

## 1. Build with Hive (the AI chat builder)

**Hive** is the default tab. It opens a chat that starts with *"Let's create a new pipeline. Pick a starting point below:"* and walks you through everything:

1. **Pick a starting point.** Choose a template: **Simple Pipeline** (Resume Screen → Interview), **Phone Prescreen** (Resume Screen → Phone Call → Interview), or **Skills Prescreen** (Resume Screen → Assessment → Review → Interview). If you've built pipelines before, a **Start from your pipelines** section lets you reuse one. You can also click **Skip for now** to continue with the simple template.
2. **Select the role.** Search for the position you're hiring for (e.g. Frontend Developer).
3. **Pick the required skills.** Hive suggests skills for the role; select at least one and click **Continue**.
4. **Choose a seniority level**: **Intern**, **Junior**, **Mid Level**, **Senior**, **Lead**, or **Principal**.
5. **Set up the interview step.** Pick your **Interviewers** from your team and a **Meeting Platform**, **Google Meet** or **Zoom**, created on the host interviewer's connected account. Your timezone is picked up automatically.
6. **Add more details, or not.** Choose **Add More Details** to specify a **Location**, **Contract Type** (Full-time, Part-time, Contract, Freelance), **Work Type** (Remote, On-site, Hybrid), and any notes, or choose **Create Pipeline Now** to skip straight ahead.
7. **Review the summary**: template, role, skills, seniority, work preferences, interview setup, and notes. Then click **Create Pipeline**.

{/* 📸 Screenshot: the Hive chat showing the three template cards (Simple Pipeline, Phone Prescreen, Skills Prescreen) */}

Hive then gets to work. You'll watch it move through **Generating job description**, **Composing assessment**, **Configuring pipeline nodes**, and **Finalizing**. When it's done you'll see *"Pipeline created."* with links to **View Pipeline** and, if your template included one, **View Assessment**.

<Callout icon="💡" theme="info">
  Hive-built pipelines are created **already active**, so the public application link works immediately. Review the generated steps and [assessment](/docs/creating-editing-assessments) before you share the link widely.
</Callout>

## 2. Build manually

The **Manual** tab is a short form that creates an empty pipeline for you to design yourself:

- **Pipeline Basics**: a **Pipeline Name** (required), plus **Job Title**, **Location**, **Workplace Type** (Hybrid, Remote, In-Office), and **Job Type** (Full-Time, Part-Time, Contract, Volunteer, Internship, Other).
- **Job Description**: write your own, or click **Generate** to get a polished starting point built from the job details above.

{/* 📸 Screenshot: the Manual tab with the Pipeline Basics form and Generate button */}

A default node flow is attached automatically and can be customized after the pipeline is created. Click **Create Pipeline** and you land directly in the visual editor, where you can drag in steps from the palette and connect them. See the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference) for what each one does.

## 3. Activate it

Manually created pipelines start as **drafts**, which can't accept applicants. When your flow is ready, open the **Manage** menu and click **Activate**. Hivemind validates the pipeline first:

- Every step must be fully configured; otherwise you'll see **Cannot Activate**: *"Please fix all validation errors before activating."*
- The job details must be complete; otherwise you'll see **Incomplete Pipeline** and be taken to **Settings** to fill them in.

Once it passes, you'll get *"Pipeline Activated — Your pipeline is now live and accepting applications,"* and the **Application Link** menu item appears so you can copy and share the public application page.

<Callout icon="⚠️" theme="warn">
  Connect a mailbox in **Settings → Email Services** before activating, since automated candidate emails can't send without one. See [Email Integration & Inbox](/docs/email-integration-inbox).
</Callout>

## What's next

- Understand every step type in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Watch applicants arrive in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Fine-tune generated tests in [Creating & Editing Assessments](/docs/creating-editing-assessments)
- See what applicants experience in [The Candidate Experience](/docs/the-candidate-experience)
