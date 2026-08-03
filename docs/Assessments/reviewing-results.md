---
title: Reviewing Results
hidden: false
---

The moment a candidate submits an assessment, Hivemind's AI grades every answer and assembles a full report — scores, written justifications, and behavioral integrity signals. Here's how to read it and how results move candidates through your pipeline.

## Open a candidate's report

Get to a report from any of these places:

- **Assessments → View Candidates** — the candidate list for one assessment, with **Score** and **Rank** columns (e.g. **Top 10%**). Click a candidate to open their report.
- The **candidate profile** — assessment results appear alongside everything else you know about them; see [Candidate Profiles](/docs/candidate-profiles).
- A **shareable link** — copy the report URL from the report header to share a read-only version with your hiring team.

If grading is still running you'll see **Evaluation in Progress** — results appear automatically once it finishes, so there's nothing to refresh or trigger.

{/* 📸 Screenshot: A candidate's assessment report showing the Overall Score ring and the Integrity Analysis card side by side */}

## The Overall Score

The report leads with an **Overall Score** out of 100 — a weighted average of every question — with a performance badge: **Excellent** (80+), **Good** (60+), **Average** (40+), or **Needs Improvement**. Below it, a percentile line compares the candidate with others in the same pipeline or with all company candidates who completed the assessment. Click **Performance Analytics** for a deeper breakdown, or **Edit Score** to override the overall number for a pipeline candidate.

## Questions & Answers

The **Questions & Answers** section breaks down every response:

- **Multiple choice** — marked **Correct Answer** or **Incorrect Answer**, showing the selected and correct options.
- **Open-ended** — the written **Response** with an **AI Score** and an **AI Grading Justification** explaining the mark against the rubric.
- **Video** — the **Video Response** plays right in the report, with its AI score and justification.
- **Coding** — the **Submitted Code** in a read-only editor with the language used; live coding also includes the **Conversation History** with the AI assistant, and a **View Session Recording** link when available.

Each scored question has its own **Edit Score** option — overridden scores are flagged with an **Edited** pill so your team knows a human adjusted them. Answers that couldn't be auto-graded are called out with the reason. For direct (non-pipeline) candidates, a **Retake Assessment** button lets you invite a fresh attempt.

## Integrity Analysis

Beside the score sits **Integrity Analysis** — behavioral pattern detection, summarized as a risk **Probability**, the number of questions **Flagged**, and a **Confidence** level. The badge ranges from **Standard Patterns** through **Minor Concerns** and **Review Recommended** up to **Requires Attention**. Click **Detailed Report** for per-question analysis of signals like **Tab Switches**, pasted content, **Description Copied**, **Choice Changes**, unusually fast answers, and video **Recording Attempts** — plus a recommendation for each. A **Session Recording** replay is available where captured.

<Callout icon="⚠️" theme="warn">
  Integrity signals detect suspicious behavior patterns — they are not proof of cheating, and there is no webcam surveillance involved. Treat **Review Recommended** and above as a cue to verify skills in a live conversation, not as an automatic rejection.
</Callout>

## How results drive stage progression

The overall score is stored on the candidate, and a decision node placed after the assessment stage branches on it — advance high scorers to an interview, reject below your threshold, or route mid-range candidates to manual review. You set those conditions yourself in the pipeline builder; there is no built-in pass mark. Manual score overrides count, so correcting a grade can change where a candidate goes next. See [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline).

<Callout icon="💡" theme="info">
  Cognitive test results show an overall score with **Reasoning**, **Memory**, and **Verbal** components and percentiles; personality reports include role-fit ratings, strengths, challenges, and **Evidence from Assessment** drawn from the candidate's own answers. See [Assessment Types](/docs/assessment-types).
</Callout>

## What's next

- Compare candidates side by side in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Move your finalists forward with [Offers](/docs/offers)
- Tune weak questions via [Creating & Editing Assessments](/docs/creating-editing-assessments)
