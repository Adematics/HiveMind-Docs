---
title: Credits & Billing
hidden: false
---

Credits are Hivemind's single currency for everything the platform does on your behalf: AI resume screening, assessment evaluation, voice interviews, outreach messages, and candidate sourcing. Instead of juggling separate meters, one balance powers it all. Manage everything from **Settings → Credits**, where you'll see your **Current Credits** balance, your **Current Subscription**, and two tabs: **Buy Credits** and **Transaction History**.

{/* 📸 Screenshot: Credits tab showing the Current Credits card, Current Subscription card, and the Buy Credits and Transaction History tabs */}

New accounts start on the free plan. Accounts created with an email and password include **300 free credits**, enough to try Hivemind's AI features on a few candidates before you top up.

## What consumes credits

Credits are deducted automatically as candidates move through your pipelines and as you use AI features:

- **AI resume screening**: 10 credits per candidate
- **Assessment evaluation**: 300 credits per candidate
- **AI voice interview**: 1,500 credits for a 10-minute call, adjusted at 150 credits per minute (shorter calls are partially refunded, longer calls cost more)
- **Personality test**: 80 credits per candidate
- **IQ test**: 80 credits per candidate
- **Pipeline emails**: 1 credit each; **SMS**: 100 credits each
- **Outreach campaign steps**: 1 credit per email or LinkedIn profile visit, 3 per WhatsApp message, 5 per SMS, LinkedIn invite, or LinkedIn message, and 10 per InMail
- **People Search**: 30 credits per profile returned (you're only charged for results actually found)

<Callout icon="💡" theme="info">
  If you connect your own OpenAI key under **Settings → Apps & Integrations**, AI evaluation stages (like resume screening) run on your key and skip the credit charge. Calls, emails, SMS, and tests are always billed in credits.
</Callout>

## Subscriptions

If your workspace has a subscription, the **Current Subscription** card shows the plan, its monthly price, how many credits it adds each month, its status, and the date it renews. Without one, the card reads **No active subscription**. Plans aren't purchased from this tab. To start or change a subscription, talk to the Hivemind team: see [Contact & Support](/docs/contact-support).

## Buying credits directly

No subscription required: the **Buy Credits** tab sells one-off top-ups at $10 per 1,000 credits. Pick one of the **Credit Packages** (1,000, 5,000, 10,000, 25,000, or 50,000 credits) and click **Buy Now**, or enter a **Custom Amount** (minimum 1,000, in steps of 1,000) and click **Buy**. Either way you'll complete payment through Stripe checkout, and the credits land in your balance right after.

## Transaction history

The **Transaction History** tab is your audit trail: every purchase, subscription refill, usage charge, and refund, with **Amount**, **Type**, **Date**, and **Status** columns. Click a row to expand the full details, handy for seeing exactly which pipeline stage or search consumed credits.

{/* 📸 Screenshot: Transaction History tab with a row expanded showing usage details */}

## When credits run out

Hivemind never charges you into the negative; actions that need credits simply pause:

- A candidate about to enter a paid stage stays at their current stage; the move is rolled back and no charge is made. Top up and move them forward again from the pipeline.
- Voice calls won't start, outreach campaigns won't launch, and People Search is blocked until you add credits.

<Callout icon="⚠️" theme="warn">
  Running dry mid-hire can stall active candidates without an obvious error on their side. Keep an eye on the **Current Credits** card. Only roles with billing permission can see this tab, so make sure someone on the team owns it.
</Callout>

## What's next

- See which pipeline stages use AI in the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- Learn how voice interviews work in [AI Voice Interviews](/docs/ai-voice-interviews)
- Estimate campaign costs in [Outreach Campaigns](/docs/outreach-campaigns)
- Find candidates with [Sourcing with People Search](/docs/sourcing-with-people-search)
