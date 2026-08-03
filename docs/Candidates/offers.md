---
title: Offers
hidden: false
---

When a candidate makes it to the end of your pipeline, Hivemind can generate their offer letter, route it through your team for approval, and collect a legally binding e-signature, with no printing and no third-party signing tool. This guide covers setting up the **Offer** step, the internal signing chain, and what candidates see.

## How offers work

Offers are driven by the **Offer** step in your pipeline. You configure it once (the letter template, the fields it collects, and who signs), and every candidate who reaches that step automatically gets their own offer. Your team fills in the details and signs first, in order; **the candidate always signs last**. There's no separate "send" button: the moment your last internal approver signs, the candidate is emailed their signing link.

## Set up the Offer step

Open the Offer step in your pipeline editor and work through its sections:

1. **Offer letter**: give it a **Name** (e.g. "Engineering Offer Letter").
2. **Offer fields**: the details the offer collects. **Position**, **Salary**, and **Start date** are always included; click **Add field** for extras, choosing a type: **Text**, **Number**, **Date**, **Amount**, or a pay rate like **Per hour** or **Per year**.
3. **Chain of approval**: click **Add approver** to add team members in signing order, optionally with a title like "Hiring Manager", and assign which fields each person fills. The **Candidate** row is always locked at the end.
4. **Letter template**: write the letter with placeholders such as `{candidate_name}`, `{company_name}`, `{salary}`, and `{start_date}` that fill in per candidate. Click **Preview** to see the rendered letter as a PDF.
5. **Send from**: pick which connected email account the signing link is sent from.

{/* 📸 Screenshot: The Offer step configuration showing Offer fields, Chain of approval, and the Letter template editor */}

## Your team fills and signs

When it's an approver's turn, a task lands in their Hivemind inbox: a live PDF preview of the letter on the left, and **Your fields** plus a **Sign** section on the right. From there they:

1. Fill in their assigned fields under **Your fields**.
2. Type or draw a signature.
3. Tick the consent boxes.
4. Click **Sign and pass to {next approver}**, or, if they're last, **Sign and send to {candidate}**.

Approvers can also **Send back** an offer to a previous signer with a note, **Decline** it, or **Withdraw** it entirely.

<Callout icon="⚠️" theme="warn">
  **Withdraw** stops everything: the candidate can no longer sign and the pipeline halts on the Offer step. It can't be undone, so use **Send back** if you just need a correction.
</Callout>

## What the candidate sees

The candidate receives "Your offer from {company} is ready to sign" with a **Review and sign** button. From there:

1. They verify their identity with a 6-digit code emailed to them.
2. They land on the signing page: the offer letter on the left, **Add your signature** on the right, with **Type** and **Draw** options.
3. They tick the consent boxes.
4. They click **Sign & finish**, or choose **Request changes** to open a negotiation, or **Decline**.

{/* 📸 Screenshot: The candidate signing page with the offer letter PDF and the signature panel */}

Once everyone has signed, the candidate gets a "Your signed offer" email and can **Download signed PDF** anytime.

<Callout icon="💡" theme="info">
  If a candidate clicks **Request changes**, you'll get a task showing their message and the terms they'd like to revisit. From there you can **Resend as-is**, **Edit & Reissue** a revised offer (which restarts the signing chain), or **Withdraw**.
</Callout>

## After signing

When the offer is fully executed, every approver is notified that the candidate signed and the pipeline advances automatically. The candidate's profile keeps the record on its **Offers** tab: status badges like **Awaiting candidate** or **Fully executed**, a signing timeline, and a **View & download** button for the signed copy. See [Candidate Profiles](/docs/candidate-profiles).

## What's next

- Add an Offer step to your flow in [Creating a Pipeline](/docs/creating-a-pipeline)
- Browse every step type in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Connect the mailbox offers send from in [Email Integration & Inbox](/docs/email-integration-inbox)
- See the applicant's full journey in [The Candidate Experience](/docs/the-candidate-experience)
