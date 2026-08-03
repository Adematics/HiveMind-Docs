---
title: Assessment Types
hidden: false
---

Hivemind offers six question types you can mix inside any assessment, plus two standalone tests, the cognitive (IQ) test and the personality test, that run as their own pipeline stages. Here's what each one measures, what candidates experience, and when to reach for which.

## Question types in the assessment builder

When you build an assessment, the **Question Types** step lets you combine any of these:

- **Open Ended**: "Let participants express detailed thoughts and ideas in writing." Candidates type into a text box (up to 3,000 characters by default), and AI grades the answer against the question's rubric. Great for judgment, communication, and role-specific scenarios.

- **Open Ended Video**: "Capture rich responses with video submissions." Candidates answer on camera in a single take of up to two minutes. The question prompt stays hidden until they press record, and no retakes are allowed, so you see a genuinely spontaneous answer. Use it to gauge communication style and presence before a live interview.

- **Multiple Choice**: "Test knowledge with predefined answer options." Single- or multi-select, graded instantly: full marks for the right choice, zero otherwise. Ideal for factual knowledge screens at scale.

- **Coding**: "Evaluate programming ability with code tasks." Candidates work in a full coding workspace with a professional editor, a terminal to run their code, and a language picker (JavaScript, TypeScript, Python, Java, Go, SQL, and many more; HTML questions get a live preview instead). A **Ready to Start?** dialog shows the time limit before the challenge begins.

- **Real-Time Coding**: "Live coding for real-time evaluation." The same coding workspace, plus a live AI assistant the candidate can talk or type to while solving the task. It mirrors modern pair-programming, so it's the best test of how someone actually works with AI tools.

- **Real-Time Open Ended**: "Dynamic real-time written responses." A live AI interview: the candidate converses by voice or text with **Hive**, Hivemind's AI interviewer, and the transcript is graded. Use it when you want interview-style depth without scheduling a call. See [AI Voice Interviews](/docs/ai-voice-interviews) for the phone-based equivalent.

{/* 📸 Screenshot: The Question Types selection cards in the assessment builder */}

<Callout icon="💡" theme="info">
  Candidates always see an overview screen first (question count, total minutes, and a **Question Breakdown** by type) before clicking **Start Assessment**. Progress saves automatically, and they can move between questions freely. More in [The Candidate Experience](/docs/the-candidate-experience).
</Callout>

## Cognitive Assessment (IQ Test)

Added to a pipeline as its own stage, the **Cognitive Assessment** is based on published neuroscience research and runs six short subtests in a fixed order: **Verbal Reasoning**, **Mental Rotation**, **Visual Memory**, **Anagrams**, **Spatial Centroid**, and **Exposure Memory**. Only the two memory subtests are timed per trial, and progress is saved so candidates can resume if interrupted.

You get an overall IQ-style score (average = 100) with three component scores (**Reasoning**, **Memory**, and **Verbal**), each with a percentile. Use it for roles where raw problem-solving matters more than a specific skill stack.

## Personality Test (Work Style Assessment)

Candidates see this as a **Work Style Assessment**: a 15–20 minute interactive conversation with the AI interviewer covering **Work Environment Preferences**, **Learning & Problem-Solving**, **Decision Making Style**, and **Work Style Flexibility**. There are no right or wrong answers, and candidates never see a score or a type.

On your side, the report maps the conversation to a personality profile with role-fit ratings (**strong fit** / **fit** / **not fit**), strengths, potential challenges, and evidence from the candidate's own answers. Details in [Reviewing Results](/docs/reviewing-results).

<Callout icon="⚠️" theme="warn">
  Use the personality and cognitive tests as one signal among several: pair them with a skills assessment and an interview rather than screening on them alone.
</Callout>

## What's next

- Build one in [Creating & Editing Assessments](/docs/creating-editing-assessments)
- Understand scoring in [Reviewing Results](/docs/reviewing-results)
- Place tests in your flow with the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
