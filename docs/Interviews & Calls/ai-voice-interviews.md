---
title: AI Voice Interviews
hidden: false
---

Hivemind can run first-round phone screens for you. Drop a **Voice Call** stage into a pipeline and an AI interviewer phones each candidate, holds a natural conversation based on your prompt, then hands you back a recording, a transcript, a summary, and a score: no calendars, no scheduling, no recruiter on the line.

## 1. Add a Voice Call stage

In the pipeline editor, add a **Voice Call** node and open its settings:

- **Node Name**: how the stage appears in your pipeline.
- **Preset**: start from **Screening (Joe)** or **Screening (Sally)** for a ready-made phone screen, or pick **Customizable** to write your own from scratch.
- **First Message**: the opening line the AI speaks when the candidate picks up.
- **Prompt**: the interview brief: what to ask, what to probe, how to evaluate. Use the **Name**, **Company**, **Position**, and **Job Description** variables to personalize every call automatically.
- **Voice**: choose **Cordial Joe** or **Laidback Sally**.

{/* 📸 Screenshot: The Voice Call node settings with a preset, first message, and prompt filled in */}

<Callout icon="💡" theme="info">
  Not sure how it will sound? Under **Try a sample call to test the configuration**, enter your own phone number and click **Start Sample Call**, and the AI will ring you and run the interview exactly as a candidate would hear it.
</Callout>

## 2. How candidates get the call

There's nothing for the candidate to install or join. When they reach the Voice Call stage, their application page shows a **Phone Call Interview** step: they enter their phone number and click **Start Phone Interview**. Their phone rings within moments and the AI interviewer takes it from there. It's a real phone call, not a browser session.

If the call doesn't come through, the candidate can click **Didn't get a phone call? Try again** after a short cooldown, for up to four attempts in total.

<Callout icon="⚠️" theme="warn">
  Voice interviews consume credits based on call length, so make sure your workspace has balance before activating the stage. See [Credits & Billing](/docs/credits-billing).
</Callout>

## 3. Review the results

Once the call ends, Hivemind processes it automatically. Open the candidate's profile and check the **Calls** tab (the entry is labeled **AI voice call**), or open their report from the pipeline. You'll find:

- **Recording**: the full audio, playable in the browser or downloadable.
- **Transcript**: the complete conversation, with a **Copy** button.
- **Summary**: an AI-written recap of how the interview went.
- **Score**: an overall result out of 100.

{/* 📸 Screenshot: A candidate's AI voice call detail showing the recording player, Summary tab, and score */}

The AI's evaluation can also drive your pipeline automatically: follow the Voice Call stage with a **Choice** node to route strong performers forward and screen out the rest. See the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference).

## 4. Prefer a human? Use Manual Phone Call

The **Manual Phone Call** node schedules recorded phone screens that *you* conduct. It has three tabs:

- **Main Config**: name the stage, pick a phone number, and set your **Company's working hours**. This node uses your own Twilio account: if you haven't linked one, you'll see **Twilio Account Not Connected** with a **Connect Twilio Account** button.
- **Scheduler**: candidates who reach the stage appear here; click **Schedule** to book a time. Both sides get an email with a calendar invite.
- **Awaiting Review**: after each call, listen back and click **Approve** or **Decline** to decide who moves on.

At the scheduled time:

1. Open the call from your email link.
2. Enter **Your Phone Number**.
3. Click **Start Conference Call**.

Hivemind dials you and the candidate into the same call, and records and transcribes it just like an AI interview.

## What's next

- Browse recordings and transcripts across your workspace in the [Calls Log](/docs/calls-log)
- Combine phone screens with tests in [Assessments Overview](/docs/assessments-overview)
- Book live interviews with [Calendar & Scheduling](/docs/calendar-scheduling)
