# .agents/skills/

This directory contains task-specific instructions for AI agents.

Use a skill when the current prompt matches the work described by that skill.
Only read skill files that are relevant to the current task.

Current skills include:

- `write_ticket.md`
- `maintain_project_notes.md`

For ordinary implementation work, follow `CONTRIBUTING.md` rather than looking
for a separate implementation skill.

Add new skills when a task type needs durable instructions that would be too
detailed or too specialized for `AGENTS.md`.

Prefer snake_case filenames.
