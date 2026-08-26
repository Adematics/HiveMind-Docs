---
title: Pipeline Nodes Reference
hidden: false
---

Every step in a pipeline is a node you drag onto the canvas from the palette on the left of the editor. The palette groups nodes into **Communication**, **Automated Assessment**, **Interviews**, **Flow Control**, and **API**. This page covers all of them, plus the built-in steps every pipeline has. For how the editor itself works, see the [Pipelines Overview](/docs/pipelines-overview).

{/* 📸 Screenshot: the node palette sidebar showing all five sections with their draggable node cards */}

## Built-in steps

Every pipeline begins with a **Start** circle and ends with an **End** circle. **Start** is where candidates enter: it carries the **Application Link** badge (click to copy the public link), the **Outreach** button for linking [outreach campaigns](/docs/outreach-campaigns), and a **Referral Link** badge. Reaching **End** marks the candidate as completed.

Right after Start sits the **Application Form**, the form applicants fill in on your public application page. By default it collects name, email, **Phone Number**, a resume upload, and **LinkedIn Profile**, and you can customize its fields.

## Communication

| Node | What it does |
|---|---|
| **Email** | Sends a customized email to the candidate, with placeholders like first name, last name, and company name. |
| **SMS** | Sends a personalized text message to the candidate's phone. |

Use these to confirm receipt of an application, share prep material before an interview, or deliver good (or bad) news between stages. Key settings: the **Subject** (email only) and **Message**, plus which connected mailbox sends the email.

## Automated Assessment

These steps evaluate candidates without you lifting a finger. Most of them email the candidate a personal link and wait for a response before advancing.

| Node | What it does | When to use it |
|---|---|---|
| **Resume Scoring** | AI analyzes and scores the candidate's resume against your job description. | As the first filter on almost every pipeline. |
| **AI Phone Call** | An AI voice agent calls the candidate and conducts a conversational interview. | Prescreening at scale. See [AI Voice Interviews](/docs/ai-voice-interviews). |
| **IQ** | A timed cognitive ability test covering verbal, numerical, logical, and spatial reasoning. | Roles needing analytical thinking and quick learning. |
| **Personality** | A work-style questionnaire on collaboration, decision-making, and flexibility, or a full **DISC** profile. | Understanding team fit and working preferences. |
| **Skills** | Sends one of your [assessments](/docs/assessments-overview), with technical challenges or custom topics. | Verifying the abilities the role actually requires. |

Key settings: **Resume Scoring** needs the **Job Description** to score against. It can also screen on **true/false resume facts** you define (for example, *"5+ years of backend experience"*); pair those answers with a **Flow** step and candidates route down different branches automatically, so the pipeline does the first pass for you. **Personality** runs the original work-style questionnaire by default, and switching its variant to **DISC** runs a 28-block forced-choice profile instead, scored the moment the candidate submits (see [DISC Personality Profiles](/docs/disc-personality-profiles)). **AI Phone Call** lets you set the opening message, the conversation prompt, and the voice. **Skills** links to an assessment you've built (a coding-focused variant appears as **Coding Assessment** on the canvas). The assessment and call steps all include **Smart Follow-Up Reminders**: up to three automatic nudges after a set number of days, sent by **Email**, **SMS**, or **Both (Email & SMS)**.

## Interviews

| Node | What it does |
|---|---|
| **Video** | Collects the candidate's availability, matches it against your team's working hours, and schedules a live video interview. |
| **Phone** | Collects availability the same way, for a phone call your team makes at the scheduled time. |

Key settings for **Video**: meeting duration, the interviewers to invite, working hours and timezone, the meeting platform (created on the host's Google or Zoom account), and a scoring rubric for the review afterward. **Phone** adds the number the call will come from. Both pause the pipeline until the interview is held and reviewed. See [Calendar & Scheduling](/docs/calendar-scheduling).

## Flow Control

| Node | What it does | When to use it |
|---|---|---|
| **Candidate Review** | Pauses the candidate until someone on your team clicks **Approve** or **Disapprove**. | A human checkpoint before expensive or final stages. |
| **Offer Letter** | Sends a generated offer for multi-party signing (internal approvers plus the candidate) and auto-advances when fully signed. | Closing the hire. See [Offers](/docs/offers). |
| **Flow** | Branches candidates down different paths based on conditions (scores, responses, other data), with a pass path and a fail path. | Routing strong scorers ahead and others to rejection. |
| **Randomize** | Randomly distributes candidates across up to four paths, with a weight per path. | A/B testing different processes or messaging. |
| **Wait** | Pauses the candidate for a delay you set in hours. | Spacing out communications or giving breathing room. |

**Offer Letter** has three built-in terms on every offer (**Position**, **Salary**, and **Start date**), and you can add your own fields and internal signers. **Flow** conditions can be grouped with AND/OR logic. **Randomize** paths hold regular process nodes only (no nested branching or waits).

## API

| Node | What it does |
|---|---|
| **Webhook** | Waits for data from an external service, then matches it to the candidate and records the results. |
| **API Call** | Sends a custom HTTP request: method, URL, headers, parameters, and body are all yours to define. |

Use these to plug in outside tools: an external testing platform, your HRIS, or anything with an API. Details in [Webhooks](/docs/webhooks) and [Integrations Overview](/docs/integrations-overview). A **Zapier** step may also appear in older pipelines for Zapier-based hand-offs.

<Callout icon="💡" theme="info">
  Not sure where to start? A strong default is **Resume Scoring → Skills → Candidate Review → Video → Offer Letter**. That's essentially what the [Hive templates](/docs/creating-a-pipeline) build for you.
</Callout>

<Callout icon="⚠️" theme="warn">
  Every node must be fully configured before you can activate the pipeline; empty or incomplete nodes block activation with a validation error.
</Callout>

## What's next

- Assemble these blocks in [Creating a Pipeline](/docs/creating-a-pipeline)
- Build the tests behind the Skills step in [Assessments Overview](/docs/assessments-overview)
- Handle review checkpoints in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Configure AI calls in [AI Voice Interviews](/docs/ai-voice-interviews)
- Read a behavioural profile in [DISC Personality Profiles](/docs/disc-personality-profiles)
