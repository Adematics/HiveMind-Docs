---
title: Ashby Sync
hidden: false
---

Running two systems usually means doing the work twice. Connect Ashby once and the two stay in step: applicants and their resumes arrive in the Hivemind pipeline you route them to, and what Hivemind learns about them goes back to Ashby as notes on the candidate.

Here is what the sync does:

| Direction | What happens |
| --- | --- |
| Ashby → Hivemind | New applications on a routed Ashby job create the candidate in Hivemind and start their pipeline at the first step. |
| Hivemind → Ashby | Results are written onto the Ashby candidate as notes: assessment scores, cognitive test and personality results, resume scores, and AI interview outcomes. |
| Ashby → Hivemind | When Ashby hires or rejects (archives) a candidate, Hivemind records the outcome and stops their pipeline: no further steps, emails or credits. An assessment they already have open can still be handed in, and it is still scored. |
| Hivemind → Ashby (optional) | Move candidates forward to the matching Ashby stage as they progress in Hivemind. Off until you turn it on. |
| New Ashby jobs (optional) | Hivemind builds a pipeline for each new Ashby job, as a draft or switched on. Off until you turn it on. |

Ashby is a company-wide connection. You need permission to manage company integrations to set it up; see [Team Members & Roles](/docs/team-members-roles).

## 1. Connect Ashby

1. In Ashby, go to **Admin**, then **API keys**, and create a key with read access to jobs, candidates, applications and interview plans.
2. In Hivemind, open **Settings → Apps & Integrations** and click **Ashby** under **ATS**.
3. Paste the key into **API key** and click **Connect Ashby**. Hivemind checks the key and confirms how many jobs it can see.

{/* 📸 Screenshot: the Ashby panel's Setup tab with the API key, Webhooks and Job routing steps */}

Once connected, the Ashby panel has two tabs: **Setup** and **Automation**. A status line at the top tells you how healthy the sync is, for example **In sync**, **No events yet**, or **Partial** when a required event has never arrived.

## 2. Add the webhooks in Ashby

Ashby tells Hivemind about new applications and stage changes through webhooks. On the **Setup** tab, open **Webhooks**:

1. Copy the **Webhook URL** and **Signing secret**. Every webhook uses this same URL and secret.
2. In Ashby, add a webhook for each event listed under **Required events**:
   - **applicationSubmit**: creates the Hivemind candidate and starts the pipeline.
   - **candidateStageChange**: keeps each candidate's Ashby stage in sync, and stops their pipeline when they are rejected or hired.
3. Optionally add the events under **Optional events**, for example **applicationUpdate** (catches archives and edits), **candidateDelete** (stops Hivemind emailing someone you deleted in Ashby), **candidateMerge**, and **jobCreate**, **jobUpdate** and **jobPostingPublish** if you want Hivemind to build pipelines for new jobs.

Each event shows **Received** with a time once it has arrived. The step turns green when every required event has come through.

<Callout icon="⚠️" theme="warn">
  If an application webhook is missed, a daily check with Ashby adds the applicant anyway. A missed stage change, rejection or hire is not recovered, so keep the required events arriving: without **candidateStageChange**, a rejection or hire in Ashby won't stop the Hivemind pipeline.
</Callout>

## 3. Route Ashby jobs to pipelines

Candidates only arrive for jobs that are routed to a pipeline.

1. Open the pipeline in Hivemind and go to **Settings**, then the **Ashby** tab.
2. Under **Ashby jobs feeding this pipeline**, tick the jobs that should send applicants here. Use the search box or **Open only** to narrow the list.
3. Save. New applicants on those jobs enter at the pipeline's first step.

A job feeds one pipeline at a time, so selecting a job that already feeds another pipeline moves it here. The **Job routing** step in the Ashby panel lists every job and the pipeline it feeds.

<Callout icon="💡" theme="info">
  A pipeline that is switched off turns away applicants from its Ashby jobs, and switching it on later does not go back for them. Keep routed pipelines active.
</Callout>

## 4. Optional: move candidates in Ashby too

On the **Automation** tab, under **When a candidate moves forward in Hivemind**, turn on **Move them in Ashby too**. When a candidate clears a step in Hivemind, they move to the Ashby stage that step was built from, so your Ashby funnel shows where people actually are.

- Only forward: Hivemind never moves anyone back a stage.
- It never touches an application your team has already hired or archived.
- It applies to pipelines Hivemind generated from an Ashby job, since those know which Ashby stage each step came from.
- If a stage has its own Ashby automations, moving someone into it runs them, so check any auto-emails on the stages your pipeline covers.

Hivemind asks you to confirm before turning it on. You can turn it off at any time, but moves already made stay made.

## 5. Optional: build pipelines for new Ashby jobs

On the **Automation** tab, **When a job is created in Ashby** decides what Hivemind does with a brand new job:

| Option | What happens |
| --- | --- |
| **Do nothing** | New Ashby jobs are ignored. You build pipelines yourself. |
| **Draft a pipeline** | Hivemind builds a pipeline linked to the job and leaves it off for you to review. Nobody is contacted until you turn it on. |
| **Build and switch it on** | A pipeline whose every step can run on its own starts immediately. Anything needing a person (an interview, a phone round, a skills assessment or an offer) is drafted instead. |

You can also limit it to **Only jobs with these words in the title** (leave it empty to cover every new job) and choose the **Pipeline shape**:

- **Match my interview plan**: each job gets a pipeline built from its own Ashby interview plan, stage by stage. A job with no readable plan gets a resume screen, then an interview.
- **Straight to interview**: a resume screen, then an interview.
- **Phone pre-screen**: a resume screen, a screening call, then an interview.
- **Skills assessment**: a resume screen, a scored assessment, a review, then an interview.

The setting covers jobs created in Ashby after you save it; jobs that already exist are left alone. Pipelines built this way carry a mark showing they were generated from an Ashby job.

<Callout icon="⚠️" theme="warn">
  **Build and switch it on** puts applicants into a generated pipeline before anyone has read it. Applicants get real emails (and SMS) and credits are spent from the moment it starts, and if a step is wrong, the message has already gone out. Messages already sent cannot be recalled. Every fixed shape ends in an interview, so only **Match my interview plan** can produce pipelines that go live on their own.
</Callout>

<Callout icon="💡" theme="info">
  Drafts lose people too: a pipeline still switched off turns away applicants to its job, and switching it on later does not go back for them. Open each new draft and turn it on as soon as you are happy with it.
</Callout>

## Disconnect Ashby

On the **Setup** tab, click **Disconnect Ashby**. This stops Ashby sync for your whole company and removes all job routing. Candidates already in Hivemind stay where they are. Reconnecting creates a new webhook URL and secret, so the webhooks in Ashby have to be added again.

If Ashby rejects the stored key later, the panel shows **Key rejected** and asks for a **New API key**.

## What's next

- Build the pipelines your jobs route into with [Creating a Pipeline](/docs/creating-a-pipeline)
- See applicants arrive in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- See every app in the [Integrations Overview](/docs/integrations-overview)
