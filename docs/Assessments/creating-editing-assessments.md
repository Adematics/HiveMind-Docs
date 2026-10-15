---
title: Creating & Editing Assessments
hidden: false
---

Build an assessment in minutes with the guided helper, or hand-pick every question yourself. This guide covers the builder, putting questions in order, the question bank, per-question analytics, and the assessments Hive composes for you automatically.

## 1. Create with the helper

From **Assessments**, click **New Assessment**. The guided builder has three steps (**Role/Skills Selection**, **Assessment Configuration**, and **Review & Confirm**):

1. **Choose a Role**: search for the role you're hiring for (e.g. Frontend Developer), then **Select Relevant Skills** from the suggested skill pills.
2. **Configure Your Assessment**: set the **Average Assessment Difficulty** (Easy / Medium / Hard) and pick your **Question Types**. Each type card shows how many matching questions are available. See [Assessment Types](/docs/assessment-types) for what each one measures.
3. **Review & Confirm**: Hivemind shows **Composing Questions...** while it generates an optimized set of 10 questions weighted to your difficulty. Review the list, swap anything you like, then click **Confirm and Create**.

{/* 📸 Screenshot: The three-step assessment builder on the Review & Confirm step showing the composed question list */}

Prefer full control? Click **Skip helper and create manually** at any step. Manual mode gives you an **Assessment Title** field, an **Add Questions** button, and a **Description** editor with a **Generate** button that writes candidate-facing instructions for you.

## 2. Add questions from the bank

The **Add Questions** button opens **Add Questions to Assessment**, a filterable picker over your question bank. Toggle **Include templates** to browse Hivemind's shared template questions alongside your own, select what you need, and click **Add Selected**.

## 3. Edit an existing assessment

Open any assessment via **Edit Assessment**. The editor shows the questions on the left and an **Overview** panel on the right that adds up the question count, duration, **Difficulty**, **Format** (question types) and **Skills**. From the header you can copy the assessment link, **Preview** it exactly as candidates will see it, and jump to **Applicants**.

- **Questions**: click **Add Questions** to pull more from the bank, or open a question's **⋯** (more actions) menu and choose **Remove**. Use the eye icon to preview a single question.
- **Title and Description**: click the title to rename the assessment, and edit the **Description** (what candidates read before they start). **Generate** rewrites it from the current questions, so regenerate after changing the set.

Question changes (adding, removing, reordering) save as you make them. The title and description save when you click **Save**; until then the header shows **Unsaved**. Difficulty and time limit recalculate automatically from the question set.

{/* 📸 Screenshot: The assessment editor with the question list, the Overview panel, and the header actions */}

### Put questions in order

Candidates answer the questions in the order shown in the editor, so you can open gently and build up:

1. Grab the handle on the left of a question and drag it to a new position, or
2. Open the question's **⋯** menu and choose **Move to top**, **Move up**, **Move down**, or **Move to bottom**. This works without a mouse, too.

The new order saves straight away. If it can't be saved, you'll see **Couldn't save the new order** and the question moves back to where it was. Candidates still get the freedom to jump around: the progress panel lets them open any question in any order. See [Assessment Types](/docs/assessment-types).

<Callout icon="💡" theme="info">
  An assessment nobody has arranged yet is ordered by question type: multiple choice first, then open ended, video, coding, real-time coding, and real-time open ended. Drag anything to override that.
</Callout>

<Callout icon="⚠️" theme="warn">
  Edits apply to everyone who takes the assessment from then on, even if candidates have already taken it, which makes earlier and later scores harder to compare. If a live assessment needs big changes, **Duplicate** it and attach the new version to your pipeline instead.
</Callout>

## 4. Manage the question bank

Click **Question Bank** on the assessments page to open **Questions**: every question you can reuse across assessments, with **Type**, **Difficulty**, **Duration**, **Skills**, **Roles**, and **Source** (**Custom** vs **Template**). Click **New Question** to create your own:

- **AI mode** (default): describe the question you want in **What question do you want to create?**, pick a type, and click **Create Question**. Review the generated question, assign skills, and save.
- **Manual mode**: write the **Question Title** and **Description**, set **Duration (min)**, **Difficulty**, and **Skill(s)**, then fill the **Question Configuration**. Multiple-choice questions take 2–4 **Answer Choices** with one marked as the **Correct Answer**; open-ended, video, and coding questions use an **Evaluation Rubric**, the point-weighted criteria the AI grades against.

{/* 📸 Screenshot: The Create Question dialog in AI mode with the prompt box and type selector */}

## 5. Check per-question analytics

From the question bank, open a question's **Question Analytics** to see **Total Usage**, **Total Candidates**, **Average Score**, and **Answer Rate**, plus a score distribution and recent answers. Retire questions that everyone aces (or no one finishes) to keep your assessments sharp.

## 6. Let Hive build it for you

When you create a pipeline with the Hive chat builder using the **Skills Prescreen** template, the **Composing assessment** step auto-builds a 10-question assessment from the role, skills, and seniority you chose, with no extra work needed. It lands in your library like any other assessment, so you can refine it afterwards. See [Quick Start](/docs/quick-start) and [Creating a Pipeline](/docs/creating-a-pipeline).

## What's next

- Attach your assessment to a stage in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- See what candidates experience in [The Candidate Experience](/docs/the-candidate-experience)
- Read the scores in [Reviewing Results](/docs/reviewing-results)
