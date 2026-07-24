# Purpose

This document explains how AI agents should collaborate on this repository.

The repository's engineering standards, coding practices, and contribution
guidelines are defined in `CONTRIBUTING.md`. Unless explicitly instructed
otherwise, follow those guidelines.

This document contains only guidance that is specific to AI collaborators.

---

# Collaboration

Be a collaborator, not an autopilot.

Before making significant changes:

- Understand the problem.
- Ask questions if requirements are unclear.
- Identify assumptions.
- Discuss reasonable alternatives when appropriate.
- Explain tradeoffs.
- Reach agreement before implementing.

Do not immediately begin coding when the problem itself is still ambiguous.

---

# Agent Support Files

Additional agent guidance lives under `.agents/`.

Use these files when they are relevant to the current task:

- `.agents/skills/` for task-specific instructions
- `.agents/notes/` for durable project context
- `.agents/templates/` for reusable output formats

Read the `README.md` in each directory before using its contents.

For ordinary implementation work, follow `CONTRIBUTING.md`, especially the
sections on working within the project, architecture, testing, code review, and
definition of done.

---

# Communication

Be transparent.

If unsure:

- say so

If making assumptions:

- state them

If multiple good solutions exist:

- explain them

If there are tradeoffs:

- describe them

Never present speculation as established fact.

---

# Git Responsibilities

The human developer owns repository history.

Unless explicitly instructed otherwise, do **not** perform Git operations that
modify repository history or branch state.

This includes, but is not limited to:

- creating commits
- amending commits
- rebasing
- squashing
- force pushing
- deleting branches
- resetting branches
- cherry-picking
- merging branches
- tagging releases

Instead:

- leave changes unstaged or staged as appropriate
- explain recommended Git workflows
- allow the human to review changes before committing

Git assistance is encouraged when requested.

When helping recover from Git issues:

- inspect before modifying
- explain the current repository state
- explain why the proposed recovery works
- prefer reversible operations whenever practical
