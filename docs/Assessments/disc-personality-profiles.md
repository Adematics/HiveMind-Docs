---
title: DISC Personality Profiles
hidden: false
---

A DISC profile tells you how a candidate prefers to work: how directly they push, how much they lean on other people, how they handle pace and change, and how closely they stick to rules and detail. It is a behavioural profile, not an ability test, and it is best read alongside the assessments that measure whether someone can do the job.

Hivemind runs DISC as a **Personality** step inside a pipeline. The candidate answers **28 forced-choice blocks**, picking what is most and least like them in each one, and the profile is scored the moment they submit.

## 1. Add it to a pipeline

Drag a **Personality** node onto the pipeline canvas from the **Automated Assessment** section of the palette, then set its variant to **DISC**. Left on the default, the node runs Hivemind's original work-style questionnaire instead, so the variant is the setting that matters here.

Like the other assessment steps, the node emails the candidate their own link and holds the pipeline until they respond. **Smart Follow-Up Reminders** work the same way as elsewhere: up to three nudges by email, SMS, or both.

{/* 📸 Screenshot: the Personality node configuration panel with the DISC variant selected */}

## 2. What the candidate sees

Twenty-eight blocks, each with a short set of statements. For every block the candidate picks the one **most** like them and the one **least** like them. There are no right answers and nothing is timed to pressure them.

The scoring key never reaches the candidate's browser: the D, I, S and C mapping is stripped from the items before they are served, so the test cannot be reverse engineered from the page.

## 3. Read the profile

The result opens on the candidate's record with a **style code** such as `DC`, made from the candidate's primary and secondary dimensions, and a style name that goes with it, such as **Trailblazer**, **Connector**, **Anchor** or **Analyst**.

The four dimensions are:

| Dimension | Reads as |
| --- | --- |
| **D — Dominance** | Drives at results, takes charge, comfortable with confrontation. |
| **I — Influence** | Persuades and energises, works through people and enthusiasm. |
| **S — Steadiness** | Steady pace, dependable, values stability and cooperation. |
| **C — Conscientiousness** | Accuracy, standards, structure, evidence before action. |

Two sets of numbers come with it. **Claimed** is built from the "most like me" picks, which is how the candidate describes themselves. The other is built from the "least like me" picks, which is what they rule out. Alongside them, **intensity** is the gap between the top two dimensions: a wide gap means a pronounced style, a narrow one means the candidate sits between two.

<Callout icon="⚠️" theme="warn">
  The dimension scores are shares of this candidate's own profile and add up to 100 across the four dimensions. They are **not** percentiles against other people. A candidate scoring 40 on D is not "in the 40th percentile for dominance", and two candidates' D scores cannot be meaningfully ranked against each other. Forced-choice answers cannot support that comparison.
</Callout>

## 4. Check the quality flags

Every profile carries a quality read, so you know how much weight to put on it. Watch for:

- **Incomplete**: the candidate left blocks unanswered.
- **Low consistency**: paraphrased items that should have matched did not.
- **Rushed**: answered fast enough that the answers may not be considered.
- **Flat profile**: no dimension separated from the others, so there is no real style to report.

A profile with no usable answers reports no primary dimension at all rather than guessing one.

<Callout icon="💡" theme="info">
  Scoring is arithmetic over the candidate's own picks. No model is involved anywhere in the scoring path, so the same answers always produce the same profile.
</Callout>

## 5. What it costs

A DISC profile is billed from your credit balance like the other assessment steps. Check the current rate against your balance in [Credits & Billing](/docs/credits-billing) before you add it to a high-volume pipeline.

## What's next

- Put the step in context in [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Compare it with the ability tests in [Assessment Types](/docs/assessment-types)
- See where results land in [Reviewing Results](/docs/reviewing-results)
