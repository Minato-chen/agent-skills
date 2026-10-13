---
name: finish-code-work
description: Implement and verify scoped code changes while protecting existing work, isolating all temporary testing, and cleaning generated artifacts. Use for bug fixes, features, refactoring requests, code reviews, and open source contributions; project summaries and interview preparation belong to the separate notion-project-summary skill.
---

# Finish code work

## Scope and baseline

1. Determine whether the user requests explanation, review, planning, implementation, or release. Discussion alone produces a proposal, not edits. Once implementation is authorized, complete the requested outcome without repeatedly seeking confirmation for routine steps.
2. Read repository instructions, relevant code, requirements, and existing tests. Define acceptance criteria from the user's actual request; do not substitute an easier milestone for the requested result. Keep repository-specific commands and conventions in its AGENTS.md or equivalent.
3. Inspect the initial branch, tracked changes, untracked files, and relevant tool versions. Preserve all pre-existing work. Do not reset, stash, revert, delete, or overwrite user changes merely to obtain a clean tree.
4. Change only files necessary for the task. Avoid unrelated refactors, whole-repository formatting, dependency upgrades, lockfile churn, and generated-file changes. Do not add debug entry points, test buttons, fake data, or temporary instrumentation to production source for convenience.

## Isolate testing

1. Before running checks, identify where they write files and whether they start processes or modify persistent state. Create a unique task-owned temporary directory outside the working repository. Put ad hoc test scripts, fixtures, logs, screenshots, caches, coverage, and build outputs there; redirect tool outputs when supported.
2. If a tool requires repository-local outputs or temporary source changes, run it in an isolated copy or worktree outside the working repository. Include the current intended changes and needed pre-existing work, not merely HEAD. Keep dependencies and configuration suitable for the check, and do not copy secrets unnecessarily. Report any material difference between the isolated environment and the actual project.
3. Keep durable regression tests in the project's established test directory when they meaningfully protect changed behavior. Treat these as intentional deliverables, not disposable verification files. Follow existing embedded-test conventions only when appropriate and clearly include such changes in the final diff. Run tests with generated artifacts and mutable state isolated.
4. Use disposable test storage and services. Do not run destructive checks against real user data, production resources, or shared state. Do not edit ignore rules merely to hide test pollution or install dependencies globally for convenience.
5. Choose checks proportionate to the change. For UI work, inspect rendering and affected interactions; for engine projects, check project loading and relevant scenes; for libraries, exercise affected behavior and meaningful edge cases. Do not add tests that only mirror the implementation.
6. Separate new regressions, baseline failures, and environment limitations. Fix task-related failures and rerun affected checks; do not weaken tests or change unrelated code to manufacture a passing result. Never claim checks passed when they were not run.

## Cleanup and completion

1. Track temporary paths and processes as they are created. Use guaranteed cleanup such as try/finally or shell traps where possible. On success, failure, or early termination, stop only task-owned processes and remove only confirmed task-owned temporary artifacts. On resuming an interrupted task, check for leftover owned artifacts before creating more.
2. Preserve requested evidence as a named deliverable before deleting temporary outputs. Remove isolated copies or worktrees through the appropriate tool. Avoid broad deletion, repository-wide clean commands, or resetting tracked files as a cleanup shortcut.
3. Compare final status against the initial baseline. Inspect the full diff, untracked and ignored outputs, generated files, dependency changes, and debug remnants. The final tree should contain intended deliverables and the user's original work. Report any cleanup failure or remaining task-owned artifact with its exact location; do not claim cleanup succeeded otherwise.
4. Report what changed, why, observed verification, material limitations, and actual completion state. Keep small-task reports brief. If blocked, preserve useful progress and name the unresolved requirement.

## Open source and external actions

Read contribution rules and relevant maintainer discussion for upstream work. Prepare a reproducible issue/PR explanation and cite real discussion when relevant. Distinguish local changes, submitted PRs, approved PRs, merged changes, and releases. Drafting a reply is different from sending it; commits, pushes, messages, merges, and deployment follow the user's existing authorization and applicable environment rules.

Do not make Notion updates part of every code task. When project documentation or interview preparation is requested or already authorized, hand actual evidence to notion-project-summary; lack of Notion access does not invalidate completed code work.
