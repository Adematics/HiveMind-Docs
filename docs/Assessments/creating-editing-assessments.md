---
title: Creating & Editing Assessments
hidden: false
---

Build an assessment in minutes with the guided helper, or hand-pick every question yourself. This guide covers the builder, the question bank, per-question analytics, and the assessments Hive composes for you automatically.

## 1. Create with the helper

From **Assessments**, click **New Assessment**. The guided builder walks three steps — **Role/Skills Selection**, **Assessment Configuration**, and **Review & Confirm**:

1. **Choose a Role** — search for the role you're hiring (e.g. Frontend Developer), then **Select Relevant Skills** from the suggested skill pills.
2. **Configure Your Assessment** — set the **Average Assessment Difficulty** (Easy / Medium / Hard) and pick your **Question Types**. Each type card shows how many matching questions are available — see [Assessment Types](/docs/assessment-types) for what each one measures.
3. **Review & Confirm** — Hivemind shows **Composing Questions...** while it generates an optimized set of 10 questions weighted to your difficulty. Review the list, swap anything you like, then click **Confirm and Create**.

{/* 📸 Screenshot: The three-step assessment builder on the Review & Confirm step showing the composed question list */}

Prefer full control? Click **Skip helper and create manually** at any step. Manual mode gives you an **Assessment Title** field, an **Add Questions** button, and a **Description** editor with a **Generate** button that writes candidate-facing instructions for you.

## 2. Add questions from the bank

The **Add Questions** button opens **Add Questions to Assessment** — a filterable picker over your question bank. Toggle **Include templates** to browse Hivemind's shared template questions alongside your own, select what you need, and click **Add Selected**.

## 3. Edit an existing assessment

Open any assessment via **Edit Assessment**. You can rename it inline, add or remove questions, regenerate or edit the **Description**, copy the shareable link, **Preview** it exactly as candidates will see it, and jump to **View Applicants**. Difficulty and time limit recalculate automatically from the question set.

<Callout icon="⚠️" theme="warn">
  Edits apply immediately, even if candidates have already taken the assessment — which makes earlier and later scores harder to compare. If a live assessment needs big changes, **Duplicate** it and attach the new version to your pipeline instead.
</Callout>

## 4. Manage the question bank

Click **Question Bank** on the assessments page to open **Questions** — every question you can reuse across assessments, with **Type**, **Difficulty**, **Duration**, **Skills**, **Roles**, and **Source** (**Custom** vs **Template**). Click **New Question** to create your own:

- **AI mode** (default) — describe the question you want in **What question do you want to create?**, pick a type, and click **Create Question**. Review the generated question, assign skills, and save.
- **Manual mode** — write the **Question Title** and **Description**, set **Duration (min)**, **Difficulty**, and **Skill(s)**, then fill the **Question Configuration**. Multiple-choice questions take 2–4 **Answer Choices** with one marked as the **Correct Answer**; open-ended, video, and coding questions use an **Evaluation Rubric** — the point-weighted criteria the AI grades against.

{/* 📸 Screenshot: The Create Question dialog in AI mode with the prompt box and type selector */}

## 5. Check per-question analytics

From the question bank, open a question's **Question Analytics** to see **Total Usage**, **Total Candidates**, **Average Score**, and **Answer Rate**, plus a score distribution and recent answers. Retire questions that everyone aces (or no one finishes) to keep your assessments sharp.

## 6. Let Hive build it for you

When you create a pipeline with the Hive chat builder using the **Skills Prescreen** template, the **Composing assessment** step auto-builds a 10-question assessment from the role, skills, and seniority you chose — no extra work needed. It lands in your library like any other assessment, so you can refine it afterwards. See [Quick Start](/docs/quick-start) and [Creating a Pipeline](/docs/creating-a-pipeline).

## What's next

- Attach your assessment to a stage in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- See what candidates experience in [The Candidate Experience](/docs/the-candidate-experience)
- Read the scores in [Reviewing Results](/docs/reviewing-results)
