---
name: notion-project-summary
description: Create or update one Notion project page with evidence-based technical results, personal contributions, collaboration history, and interview preparation. Use for requested project summaries, contribution records, milestone documentation, portfolio material, and interview narratives; implementation and testing belong to the code-work workflow.
---

# Notion project summary

Keep technical records and interview preparation on one project page. Summarize ongoing or completed work honestly; do not implement code or perform unrelated changes to strengthen the narrative. Use the user's preferred language, defaulting to Chinese when appropriate. Scale effort to the milestone: small changes need a short targeted update, not a complete story or full-page rewrite. Apply checks internally and show only useful findings; do not repeatedly ask for already available context.

## Scope and page identity

1. Identify the project, requested scope, audience, milestone, and whether the user wants advice, a draft, or a saved update. Discussion alone does not authorize Notion writes. Proceed with writes already authorized by the request or established workflow without asking again for routine steps.
2. Locate the existing page by stable identity, preferring repository/product URL or a known page ID over a similar title. If several candidates remain, prepare the content and clarify the destination before writing. Create a new project page only when no matching page exists and the intended parent and authorization are clear.
3. Read the current page and relevant supporting records. Ensure the affected sections and their nested content have been read completely, following pagination when needed; do not assume a partial response is the whole page. Read broader content only as necessary to preserve structure and avoid duplicates.
4. Use available Notion capabilities and their current schemas; the skill supplies no credentials or permissions. If access or destination is unavailable, prepare a ready-to-paste update and state what was not saved. Do not change connection settings, database schemas, sharing, publish status, or send notifications merely to summarize a project.

## Evidence and attribution

1. Inspect relevant changes, issues, PRs, releases, test evidence, and discussion. Separate verified facts, user-provided statements, inference, and unknowns. User statements may be recorded without presenting them as independently verified. Never invent tests, outputs, impact, collaboration, dates, or source coverage.
2. Distinguish project-wide capability from personal responsibility and contribution. Do not attribute the whole product, collaborators' work, or all AI-generated implementation to the user without support. Describe the user's actual design, investigation, implementation, review, integration, and validation responsibilities when known; mark unclear ownership rather than guessing.
3. Distinguish activity from outcome and expected benefit from observed effect. Explain the concrete behavior improved. Do not invent performance, adoption, revenue, or percentage gains; meaningful qualitative results are acceptable. Give quantitative claims their baseline, measurement conditions, and source when available.
4. Verify submitted, approved, merged, released, and deployed states separately. Current status does not establish when a transition happened; last-edited timestamps are not completion dates. Resolve conflicting sources using relevant authoritative evidence or report the conflict instead of selecting the optimistic version.
5. Record actual constraints, decisions, alternatives considered, feedback, responses, and informative failed attempts. Do not reconstruct an impressive decision history from final code. Label newly generated alternatives or lessons as retrospective analysis rather than contemporaneous choices.
6. Put source links near material claims without attaching citations to every sentence. Report important inaccessible evidence or coverage limits. Include only necessary project information; omit credentials, unrelated private conversations, and collaborators' personal circumstances. Do not expose private content to external searches or broaden existing access.

## Maintain one project record

Use these sections for an initial full summary; adapt to existing headings instead of creating duplicate structures:

1. **项目概况** — repository/product link, goal, personal role, current state, and supported milestone dates.
2. **问题与实现** — original problem, evidence, approach, personal contribution, actual decisions, and tradeoffs.
3. **验证与结果** — checks actually observed, manual evidence, PR/release links, limitations, and supported impact.
4. **团队协作** — actual participants or roles, feedback, responses, resulting changes, unresolved differences, and follow-up. Link discussion; describe solo work honestly.
5. **面试表达** — concise spoken account, technical depth, and a small set of evidence-based project-specific follow-up questions.
6. **后续事项** — review, maintenance, blockers, and next steps; distinguish proposed actions from commitments.

Keep the main sections current and a brief dated history of meaningful milestones, decisions, or status transitions. Update only affected content; do not append another full summary on every run. Preserve useful history and unrelated edits. If a fact was wrong, correct the current summary and record a material correction when needed, rather than preserving a misleading statement as truth. Use stable project/event identifiers or source links to recognize an already recorded update; the same milestone should not create duplicate paragraphs or history entries.

## Interview expression

1. Default to a brief spoken account of the problem, personal responsibility, key action, and actual result. Use STAR as an organizing aid, not a mandatory four-heading template. Keep language natural and support every claim with the technical record.
2. Add relevant depth: why the approach was chosen, real alternatives and constraints, validation, limitations, and lessons learned. Include a few likely project-specific follow-ups with evidence-based answers; do not generate a generic question bank or fabricate experience to answer it.
3. An unmerged PR can demonstrate investigation, implementation, and response to review. State its real submission and feedback status; do not imply upstream acceptance, release, or user impact. Include unfinished work honestly rather than excluding it automatically.
4. Tailor emphasis to a known target role and requested speaking language. Without one, use a general technical account rather than inventing a job target. Do not create multiple language versions or lengthy scripts unless useful or requested. When technical facts or status change, synchronize the corresponding interview claims without duplicating the whole technical explanation.

## Incremental writing and verification

1. Before writing, identify the target page and affected blocks/properties. Use scoped edits; do not replace the entire page to update one section. Recheck affected content for changes since it was read, using supported version guards when available; integrate concurrent edits rather than overwriting a stale snapshot.
2. If an operation times out or returns an uncertain result, inspect the target before retrying. Determine whether all, part, or none of the intended update was saved, and retry only missing changes. Do not create a second page or duplicate blocks merely because the response was lost.
3. Check consistency of sources, dates, contribution attribution, result claims, and completion states across the technical and interview sections. After writing, read back the changed content and inspect enough neighboring structure to confirm the intended update and preservation of prior material.
4. Report the page link and concise changes when saving is verified. If writing fails, report the known partial state; if readback fails after a write, say the save is unconfirmed rather than claiming either success or definite failure. Retain a usable draft for recovery. Summarizing a project does not authorize modifying tasks, PRs, collaborators' records, or sending messages.
