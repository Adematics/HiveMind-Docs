---
title: Pipeline Nodes Reference
hidden: false
---

Every step in a pipeline is a node you drag onto the canvas from the palette on the left of the editor. The palette groups nodes into **Communication**, **Automated Assessment**, **Interviews**, **Reviews**, **Flow Control**, and **Integrations**. Each step type has its own icon, shown the same way in the palette and on the canvas. This page covers all of them, plus the built-in steps every pipeline has. For how the editor itself works, see the [Pipelines Overview](/docs/pipelines-overview).

{/* 📸 Screenshot: the node palette sidebar showing all six sections with their draggable node cards */}

## Built-in steps

Every pipeline begins with a **Start** card. It's where candidates enter, and it has three rows: **Application link** (click to copy the public link), **Outreach** for linking [outreach campaigns](/docs/outreach-campaigns), and **Referral link**, which opens the referral settings. Empty **Drag a step here** slots show where the next step can go. When a candidate finishes the last step on their path, they're marked as completed.

Right after Start sits the **Application Form**, the form applicants fill in on your public application page. By default it collects name, email, **Phone Number**, a resume upload, and **LinkedIn Profile**, and you can customize its fields.

## Communication

| Node | What it does |
|---|---|
| **Email** | Sends a customized email to the candidate, with placeholders like first name, last name, and company name. |
| **SMS** | Sends a personalized text message to the candidate's phone. |

Use these to confirm receipt of an application, share prep material before an interview, or deliver good (or bad) news between stages. Key settings: the **Subject** (email only) and **Message**, plus which connected mailbox sends the email. Insert placeholders with the **Variables** picker beside each field, or press **Ctrl+/** (**⌘/** on Mac) while typing. Its **Custom** group holds your company's message variables (set under **Settings → Workspace Settings → Message Variables**), and a variable can carry a fallback after a pipe, like `{city|your area}`, for when there's nothing to fill in. See [Outreach Campaigns](/docs/outreach-campaigns) for more on variables.

## Automated Assessment

These steps evaluate candidates without you lifting a finger. Most of them email the candidate a personal link and wait for a response before advancing.

| Node | What it does | When to use it |
|---|---|---|
| **Personality Test** | A **Work Style Interview** (a conversational AI interview on collaboration, decision-making, and work style) or a **DISC Profile** questionnaire. | Understanding team fit and working preferences. |
| **Skills Assessment** | Sends one of your [assessments](/docs/assessments-overview), with technical challenges or custom topics. | Verifying the abilities the role actually requires. |
| **Resume Screening** | AI analyzes and scores the candidate's resume against your job description. | As the first filter on almost every pipeline. |
| **IQ Test** | A timed cognitive ability test covering verbal, numerical, logical, and spatial reasoning. | Roles needing analytical thinking and quick learning. |
| **AI Phone Screen** | An AI voice agent calls the candidate and conducts a conversational interview. | Prescreening at scale. See [AI Voice Interviews](/docs/ai-voice-interviews). |

Key settings: **Resume Screening** scores each resume out of 100 against its **Evaluation criteria** (typically your job description). It can also screen on **true/false resume facts** you define (for example, *"5+ years of backend experience"*); branch on those answers with a **Choice** step and candidates route down different paths automatically, so the pipeline does the first pass for you. **Personality Test** asks you to choose a variant once the step is added: the **Work Style Interview** (15–20 minutes, needs a microphone) or the **DISC Profile**, a 28-question forced-choice profile (6–8 minutes, any device) scored the moment the candidate submits (see [DISC Personality Profiles](/docs/disc-personality-profiles)). **AI Phone Screen** lets you set the opening message, the conversation prompt, and the voice. **Skills Assessment** links to an assessment you've built (a coding-focused variant appears as **Coding Assessment** on the canvas). The assessment and call steps all include **Smart follow-up reminders**: up to three automatic nudges after a set number of days, sent by **Email**, **SMS**, or **Email & SMS**.

## Interviews

| Node | What it does |
|---|---|
| **Video Interview** | Collects the candidate's availability, matches it against your team's working hours, and schedules a live video interview. |
| **Phone Interview** | Collects availability the same way, for a phone call your team makes at the scheduled time. |

Key settings for **Video Interview**: the **Meeting platform** (**Google Meet**, **Zoom**, or **Microsoft Teams**), the **Interviewer Pool**, **Meeting Owner**, and **Other Interviewers**, working hours and **Timezone**, and an **Evaluation Rubric** for the review afterward. Each interviewer hosts on their own connected account; teammates connect their platforms under **Calendar → Connections**, and only people who have the chosen platform connected can be picked. **Phone Interview** adds the **Twilio phone number** the call comes from. Both pause the pipeline until the interview is held and reviewed. See [Calendar & Scheduling](/docs/calendar-scheduling).

## Reviews

Both of these hold the candidate until a person signs off.

| Node | What it does | When to use it |
|---|---|---|
| **Candidate Review** | Pauses the candidate until someone on your team clicks **Approve** or **Disapprove**. | A human checkpoint before expensive or final stages. |
| **Offer Letter** | Sends a generated offer for multi-party signing (internal approvers plus the candidate) and auto-advances when fully signed. | Closing the hire. See [Offers](/docs/offers). |

**Offer Letter** has three built-in terms on every offer (**Position**, **Salary**, and **Start date**), and you can add your own fields and internal signers.

## Flow Control

| Node | What it does | When to use it |
|---|---|---|
| **Choice** | Branches candidates down different paths based on conditions (scores, responses, other data). | Routing strong scorers ahead and others to rejection. |
| **Randomization** | Randomly distributes candidates across up to four paths, with a weight per path. | A/B testing different processes or messaging. |
| **Wait** | Pauses the candidate for a delay you set in hours. | Spacing out communications or giving breathing room. |

**Choice** works through **Branches**: candidates are checked against each branch in order and take the first one they match. A new Choice starts with one branch called **Meets criteria**; rename it, click **Add condition** under **Send candidates where**, and choose whether a candidate must match **All** or **Any** of the conditions. Click **Add a branch** for more (up to four). An **Everyone else** branch is always there and can't be removed: anyone who matches none of the branches above ends up on it. On the canvas, each branch's name appears as a colored label on the step it leads to, and **Everyone else** is always red. **Randomization** paths hold regular process nodes only (no nested branching or waits).

## Integrations

| Node | What it does |
|---|---|
| **Webhook** | Waits for data from an external service, then matches it to the candidate and records the results. |
| **API Call** | Sends a custom HTTP request: method, URL, headers, parameters, and body are all yours to define. |

Use these to plug in outside tools: an external testing platform, your HRIS, or anything with an API. Details in [Webhooks](/docs/webhooks) and [Integrations Overview](/docs/integrations-overview). A **Zapier** step may also appear in older pipelines for Zapier-based hand-offs.

<Callout icon="💡" theme="info">
  Not sure where to start? A strong default is **Resume Screening → Skills Assessment → Candidate Review → Video Interview → Offer Letter**. That's essentially what the [Hive templates](/docs/creating-a-pipeline) build for you.
</Callout>

<Callout icon="⚠️" theme="warn">
  Every node must be fully configured before you can activate the pipeline; empty or incomplete nodes block activation with a validation error.
</Callout>

## What's next

- Assemble these blocks in [Creating a Pipeline](/docs/creating-a-pipeline)
- Build the tests behind the Skills Assessment step in [Assessments Overview](/docs/assessments-overview)
- Handle review checkpoints in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Configure AI calls in [AI Voice Interviews](/docs/ai-voice-interviews)
- Read a behavioural profile in [DISC Personality Profiles](/docs/disc-personality-profiles)
