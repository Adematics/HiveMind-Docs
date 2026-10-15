---
title: Dashboards Overview
hidden: false
---

Dashboards turn everything already in your account into boards you can read at a glance: how each pipeline is converting, which candidates are moving, how interviews and assessments are going, and where your credits went. Open **Dashboards** in the sidebar to get there. If you don't see it, your role doesn't include viewing analytics dashboards; ask a workspace admin (see [Team Members & Roles](/docs/team-members-roles)).

There are two kinds of board, and the difference matters:

- **Core boards** are built in and always current. Hivemind hydrates them live every time you open one, so there is nothing to set up and nothing to keep up to date.
- **Saved boards** are yours. You start them, name them, arrange the cards, and come back to them.

{/* 📸 Screenshot: the Dashboards index showing the core-board rail and saved boards */}

## 1. Start with a core board

Six core boards ship with every account, listed under **Core dashboards** in the left rail (your own boards follow under **Your dashboards**):

| Board | What it answers |
| --- | --- |
| **Overview** | How is hiring going overall right now? |
| **Pipelines** | Where are candidates converting, and where are they stalling? |
| **Candidates** | Who is in play, and how did they get there? |
| **Interviews** | What is scheduled, held, and still waiting on a review? |
| **Assessments** | How are candidates performing on what you send them? |
| **Credits** | Where is the balance going? |

Core boards are read-only as they stand. Change anything on one and Hivemind forks your version into a saved board rather than overwriting the built-in, so you can always get back to the original. Use **Save a copy** to do that deliberately. **Refresh** re-pulls the numbers without dropping the filters you have set.

## 2. Filter what you are looking at

Every board with live data has two controls at the top: a searchable **pipeline picker** (set to **All pipelines** by default) and a **time range**.

- **Pipeline**: type a few letters under **Search pipelines…** and pick one. Widgets about candidates, interviews and assessments narrow to that pipeline. Widgets about the pipelines themselves (for example, a comparison across pipelines) stay as they are, because narrowing them to one pipeline would tell you nothing.
- **Time range**: choose a rolling window (**Today**, **Last 7 days**, **Last 30 days**, **Last 90 days**, **Last 12 months**) or a calendar one (**This week**, **This month**, **This quarter**, **All time**). **Default range** clears the range again. Every live widget re-reads against the window you pick.

The board title follows the range, so a board never claims to show thirty days while displaying ninety.

<Callout icon="💡" theme="info">
  Some widgets hold fixed values rather than a live query, so the filters cannot re-run them. When none of a board's widgets can be filtered, the controls are disabled and the header reads **Fixed data: ask Hive to change the range**. A chart that hit the 5,000-record limit shows **Partial: most recent 5,000 records** underneath; narrow the time range or pick a pipeline for exact figures.
</Callout>

## 3. Create your own board

Click **New dashboard** on the Dashboards index. Under **Start from**, choose:

- **Blank**: an empty board. Ask Hive what you want to see and it builds the widgets for you.
- **One of the core boards**: a populated copy of that board, with its current numbers, that you can change into what you actually want. Each tile shows how many widgets the board has.

Give it a **Name** (picking a core board fills in a name like *Pipelines (copy)*; leave it empty for **Untitled dashboard**) and click **Create dashboard**. The board opens ready to edit and is saved as a draft.

{/* 📸 Screenshot: the New dashboard dialog with Blank and the core boards as starting points */}

### Arrange the cards

Cards sit on a twelve-column grid:

- Drag a card to move it, and drag its corner to resize in either direction.
- Cards snap to whole columns and pack together, so a board cannot end up with holes in it.
- KPI cards compress to compact chips, so a row of numbers stays a row of numbers.
- Click a card's title to rename it. Each card can also **Refresh data**, **Export as PNG**, **Export as CSV**, toggle half or full width, or be removed.

Click the board's title to rename it, and **Save** to keep your changes. Press the fullscreen control to fill the screen with a single board, and **Esc** to come back.

{/* 📸 Screenshot: the board editor with a card mid-resize on the twelve-column grid */}

### Drafts, publishing and sharing

The Dashboards index (**Your dashboards**) lists your boards in two groups, with a summary of the widgets on each:

- **Drafts**: boards you are still working on, including the ones Hive builds for you. Click **Publish** to make one live.
- **Published**: live boards with a public share link. Click **Share** to copy the link; anyone with it can view the board without signing in. Inside a published board, **Copy share link** does the same.

<Callout icon="⚠️" theme="warn">
  A published board's link works for anyone who has it, with no sign-in. Check what a board shows before you share its link outside your company.
</Callout>

## 4. Ask Hive instead of building by hand

Hive is the chat dock that sits alongside your boards: open it with the **Open Hive** button in the bottom-right corner, or with **Ask Hive** on an empty board. Describe the board you want and it builds it; ask for a change while a board is open and the change lands on that board in place, with no overlay to dismiss and no copy to reconcile.

Openers that work well:

- *Give me a hiring overview for the last 30 days*
- *Compare my pipelines by applications and scores*
- *Who moved stages this week?*

Hive knows which board you are looking at, so follow-ups can be short: *now split that by pipeline*, *make it the last quarter instead*.

<Callout icon="⚠️" theme="warn">
  A request that is not about the board you have open forks a new draft instead of overwriting your work. If a board you expected to change did not, look for a new draft on the Dashboards index.
</Callout>

## What's next

- Understand the numbers behind the pipeline boards in [Pipelines Overview](/docs/pipelines-overview)
- See how assessment scores are produced in [Reviewing Results](/docs/reviewing-results)
- Track spend in [Credits & Billing](/docs/credits-billing)
