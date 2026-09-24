---
name: finish-code-work
description: Work on code projects and open source contributions with scoped changes, honest verification, collaboration tracking, and one Notion project page containing technical records and interview preparation. Use for coding tasks, PRs, releases, and completed project milestones.
---

# Finish code work

## Scope and implementation

1. Read repository instructions, relevant code, issue or request, and existing tests. Identify a useful milestone and its acceptance criteria. Follow upstream conventions for contributions.
2. Make focused changes. Preserve unrelated work and avoid unrelated refactors. Explain consequential design choices and compatibility implications.
3. Add or update tests when behavior changes and tests meaningfully guard against regression. Run relevant checks. Inspect the final diff, status, generated files, and potential secrets. Never claim a check passed if it was not run.
4. For open source work, read contribution rules and maintainer discussion. Prepare a reproducible explanation, link the issue where appropriate, respond to review with concrete changes, and distinguish submitted, approved, merged, and released states.
5. Report what changed, why, verification evidence, limitations, and the next action. Do not treat a drafted patch or unsubmitted PR as a completed external contribution.

Put project-specific commands, architecture, and conventions in that repository's AGENTS.md or equivalent; follow those instructions when present.

## Milestone and Notion record

At a meaningful completed milestone (for example a submitted PR, merged PR, published extension, released plugin, or finished feature), update the **existing single Notion page for that project**. Do not create separate technical and job-interview documents. Find the correct page by project identity and links; avoid duplicates. If no page exists, create one project page in the user's intended location only when that location is clear. Never pretend an unavailable Notion connection succeeded: prepare the content and report the blocker.

Keep these sections together on that page, updating relevant parts and preserving useful prior history:

1. **项目概况** — repository/product link, role, goal, current state, milestone dates.
2. **问题与实现** — original problem, evidence, approach, personal contribution, key decisions and tradeoffs.
3. **验证与结果** — commands and outcomes actually observed, manual checks, PR/release links, feedback and measurable impact if supported. Separate submitted, merged, and released states.
4. **团队协作** — people or roles involved, issue/PR discussion, feedback received, response, changes made, unresolved differences, and follow-up. Cite actual discussion; do not invent teamwork or shared ownership for a solo project.
5. **面试表达** — a concise spoken account covering background, personal responsibility, technical challenge, decisions, results, and collaboration; likely follow-up questions with evidence-based answers. Tailor emphasis to the target role if known. Mark unverified impact and unfinished work honestly.
6. **后续事项** — outstanding review, maintenance, and next steps.

Verify external facts from the current repository, PR, release, and discussion before changing status. Add source links and dates. For later milestones, revise the same page and append a brief dated update so earlier states remain understandable. Avoid repetitive prose between the technical and interview sections.

If the task ends before a meaningful milestone, give a concise progress report; do not label it complete or force a Notion entry. If Notion access or destination is unavailable, provide a ready-to-paste update and identify the page or destination needed. Never claim it was saved.
