---
title: Calendar & Scheduling
hidden: false
---

The **Calendar** page is where interview scheduling comes together: your Google Calendar events, your teammates' busy times, and every interview candidates book, all on one grid. Set your availability once, and Hivemind offers candidates only the times that actually work for you.

## 1. Connect your accounts

Open **Calendar** from the sidebar and switch to the **Connections** tab. You'll see two sections under **Connected Accounts**:

- **Calendar sync**: click **Connect Google Calendar** to sync your availability and surface your events on the in-app calendar. Once connected, the **Sync** button in the header pulls in your latest events.
- **Meeting platforms**: click **Connect Google Meet** or **Connect Zoom** so interviews you own get a meeting link on your account. Microsoft Teams is marked **Coming soon**.

{/* 📸 Screenshot: The Connections tab showing the Calendar sync and Meeting platforms cards */}

<Callout icon="💡" theme="info">
  Google Calendar and Google Meet are separate connections: linking your calendar doesn't automatically enable Meet. You can use the same Google account for both, and Zoom works on its own with no calendar required. Each interviewer hosts meetings on their own connected account, so every teammate who runs interviews should connect a platform here.
</Callout>

## 2. Set your availability

Click the **Availability** button in the calendar header:

1. Turn on **Available for interviews**. First-time setup gives you default hours of Mon–Fri, 9:00–5:00.
2. Pick your timezone and adjust the **Weekly Hours** grid: toggle days on or off, add extra time ranges with **Add**, or use **Copy** to apply one day's hours to another.
3. Optionally set a **Buffer between meetings** and a **Minimum advance notice** so bookings can't land back-to-back or at the last minute.
4. Click **Save**.

Candidates can only book you inside these hours, minus anything already on your connected calendar. Turning **Available for interviews** off pauses new bookings without losing your hours.

<Callout icon="⚠️" theme="warn">
  If your status shows **Availability not set**, candidates can't book interviews with you, and interviewers without availability can't be selected for interview stages. Set your hours before activating a pipeline with interviews.
</Callout>

## 3. Work the calendar

The **My calendar** tab shows **Month**, **Week**, and **Day** views. Use the mini calendar to jump between dates, the **Pipeline** filter to show one pipeline's interviews (or **All Events**), and the **Other calendars** list to overlay teammates: their events appear as private **Busy** blocks.

{/* 📸 Screenshot: Week view with a booked interview event and a teammate's Busy overlay */}

- **Block time**: click and drag an empty slot to open the **Block Time** dialog, then give it a title, adjust the times, and hit **Create Event**.
- **Open an event**: click it to see the time, participants, description, a **Join Meeting** link, and **Open in Google Calendar**. From here you can **Reschedule** or **Delete** events you organize; deleting a synced event removes it from Google Calendar too.

## 4. Reschedule by dragging

Interview bookings (the events tied to a candidate) can simply be dragged to a new slot. A confirmation asks **Reschedule this interview?** showing the old and new times; click **Reschedule & notify** and the candidate is emailed the new time while the calendar invite updates for everyone. Only the meeting organizer can reschedule, and past time slots are blocked.

## 5. How candidates book

Interview stages in your pipelines offer two **Booking Mode** options:

- **Candidate Book**: the candidate sees your team's open slots on a **Book Your Interview** page, picks a time, and clicks **Confirm Booking**. They get an **Interview Booked!** confirmation and the meeting link by email, and they can reschedule themselves later.

The booking page has a **Timezone** picker, set to the candidate's own timezone when the page loads. Every slot on the page is shown in whichever timezone is selected, so a candidate in another country reads times in theirs and never has to convert your working hours by hand. Changing the picker re-labels the slots; it does not change which slots are on offer, because those still come from your availability.
- **Company Book**: the candidate submits their availability, and you pick the time from the pipeline's **Scheduler** tab using the **Schedule** button next to each candidate.

See [Pipeline Nodes Reference](/docs/pipeline-nodes-reference) for configuring interview stages.

## What's next

- Build an interview stage into a pipeline in [Creating a Pipeline](/docs/creating-a-pipeline)
- See what booking looks like from the candidate's side in [The Candidate Experience](/docs/the-candidate-experience)
- Let AI handle first-round screens with [AI Voice Interviews](/docs/ai-voice-interviews)
