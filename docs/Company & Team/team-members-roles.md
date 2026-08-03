---
title: Team Members & Roles
hidden: false
---

Hiring is a team sport, and Hivemind lets everyone in, with exactly the access they need. Teammates live in **Settings → Team Members**, and what each person can do is governed by their role in **Settings → Roles**. This guide covers inviting people, managing them, and building roles of your own.

## 1. Invite a teammate

1. Open **Settings → Team Members** and click **Invite**.
2. Enter their **Email** and pick a **Role**. The dropdown lists **System Roles** and any **Custom Roles**, with **Recruiter** pre-selected as a sensible default. You can even pick **Create new role…** to build one on the spot.
3. Click **Invite**.

Your teammate receives an invitation email. The link takes them to a **Verify Invite** page where they enter their **Full Name** and set a password (8+ characters with at least one uppercase and one lowercase letter), then they're signed straight into your workspace. Until they accept, their card shows a pending status.

{/* 📸 Screenshot: the Invite Team Member dialog with the Email field and Role dropdown open */}

## 2. Manage members

The **Team Members** tab groups everyone by role, with the workspace **Owner** shown separately at the top. On each member's card you can:

- **Change their role**: pick a new system or custom role from the dropdown.
- **Manage pipeline access**: for roles that work inside pipelines, assign specific pipelines so each person only sees the searches they're part of. The Owner always has **Full Access**.
- **Delete the member**: removes them from the workspace (this can't be undone).

<Callout icon="💡" theme="info">
  There is exactly one **Owner** per workspace. The Owner role can't be reassigned, and the Owner can't be deleted or moved to another role.
</Callout>

## 3. System roles vs custom roles

Open **Settings → Roles**. Hivemind ships with seven ready-made **System Roles**: **Admin**, **Recruiter**, **Hiring Manager**, **Interviewer**, **Sourcer**, **Developer**, and **Viewer**. Each has a curated permission set and a member count so you can see who's on what. System roles can't be edited; they're a stable foundation.

When the presets don't fit (say you want a reviewer who can score assessments but never touch billing), create a **Custom Role**.

## 4. Build a custom role

1. In the **Roles** tab, click **New Role**.
2. Give it a **Name** (e.g. *Pipeline Reviewer*) and an optional **Description**.
3. Optionally use **Clone from** to start with a system role's permissions instead of a blank slate. (Owner can't be cloned; it's reserved.)
4. Tick permissions in the **Permissions** list. They're grouped by area (pipelines, candidates, billing, and so on), and each group has a select-everything option if you want to grant a whole area at once.
5. Click **Create role**.

Custom roles appear alongside system roles everywhere a role can be assigned. Edit or delete them anytime from the **Roles** tab.

{/* 📸 Screenshot: the role builder panel showing Name, Description, Clone from, and the grouped Permissions checklist */}

<Callout icon="⚠️" theme="warn">
  A role can only be deleted while no one is assigned to it. If members still hold the role, you'll get a "Role is in use" message. Move them to another role first, then delete.
</Callout>

## 5. What roles control

Permissions shape the whole app, not just Settings: tabs like **Workspace Settings**, **Roles**, and **Credits** only appear for roles allowed to manage them, and pages a role can't access simply don't show. If a teammate says something is "missing," check their role first. See [Settings Overview](/docs/settings-overview).

## What's next

- Finish workspace basics in [Account & Workspace Setup](/docs/account-workspace-setup)
- Put your team to work in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Assign interviewers to scheduling in [Calendar & Scheduling](/docs/calendar-scheduling)
