---
title: Sourcing with People Search
hidden: false
---

People Search is Hivemind's built-in sourcing tool. Instead of stacking filters by hand, you describe who you're looking for in plain language, and Hivemind turns your description into search criteria, finds matching professionals with contact details already included, and explains why each one fits. From there, adding prospects to an [outreach campaign](/docs/outreach-campaigns) takes one click.

## 1. Start a search

Open **Outreach**; the **Search** tab is the default view. You'll see the prompt **"Hey, who are you looking for?"** with a search box. Type a description like *Senior React engineer in San Francisco, 5+ years experience*. As you type, pills light up for each thing Hivemind recognizes: **Job Title**, **Location**, **Seniority**, **Industry**, **Company Size**, and **Skills**. Your **Recent searches** are listed below so you can re-run them.

{/* 📸 Screenshot: the People Search start screen with the search box and detection pills */}

## 2. Review your search

Before anything runs, a **Review your search** dialog shows the criteria Hivemind parsed, grouped by category (job title, seniority, skills, location, industry, experience, company, and more). Each criterion has a role you can change:

- **Required**: the candidate must match.
- **Nice to have**: boosts ranking but never excludes anyone.
- **Excluded**: the candidate must not match.

Use **Add filter** to add criteria yourself (including **Job title**, **Skill**, **Location**, **Industry**, **Company**, **Seniority**, **Company size**, **Company type**, and minimum years of **Experience**), or remove any chip you don't want. You need at least one **Required** filter before the **Search** button activates.

{/* 📸 Screenshot: the Review your search dialog with criteria chips and the role dropdown */}

## 3. Read the results

Results appear as a ranked list with a counter like **1,234 matches · showing 10**. Each row shows the person's name, current title and company, location, years of experience, and their email, phone, and LinkedIn where available. A match badge like **4/5** counts how many of your criteria are confirmed from the profile, and each criterion chip is marked green (confirmed), red (doesn't match), or neutral (partial).

Expand a row for the full picture:

- **Why they fit**: an AI-written fit summary that leads with the person's strongest signal and flags the most important gap.
- **Experience**: their employment timeline.
- **Skills**: with your searched skills highlighted.

{/* 📸 Screenshot: an expanded search result showing the Why they fit summary */}

<Callout icon="💡" theme="info">
  Searches cost credits per profile returned. Each search brings back up to 10 profiles, and you're only charged for results actually found. If your balance is too low, the search fails with an **Insufficient credits** message. See [Credits & Billing](/docs/credits-billing).
</Callout>

## 4. Add prospects to a campaign

Tick the checkbox on any rows you like (or **Select all**). A bar appears showing how many are selected; click **Add to campaign**:

- From the main Search tab, Hivemind creates a new draft campaign named after your selection and opens it, ready for a sequence.
- If you searched from inside an existing campaign (via **Add prospects**), the people are added to that campaign instead.

Only prospects with an email address can be added; the button shows the reachable count when some selections have no email.

## 5. Your contact library

Every profile a search returns is automatically saved to the **Contacts** tab, so you never lose a good find. From there you can select saved contacts and click **Create Campaign** to start outreach later, or pull them into an existing campaign with **From Contacts**.

<Callout icon="⚠️" theme="warn">
  If you clear every filter, Hivemind asks you to **keep at least one filter**: very broad searches are blocked so you don't spend credits on unusable results.
</Callout>

## What's next

- Build the sequence those prospects will receive: [Outreach Campaigns](/docs/outreach-campaigns)
- Connect a mailbox so email steps can send: [Email Integration & Inbox](/docs/email-integration-inbox)
- Track who applies in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
