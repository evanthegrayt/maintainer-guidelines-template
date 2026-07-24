# Skill: Maintain Project Notes

## Purpose

Project notes preserve durable project understanding across collaborators.

They are a convenience, not the source of truth.

Repository truth is, in order:

1. code
2. tests
3. build configuration
4. project configuration
5. documentation
6. project notes

Always verify notes against the repository before relying on them.

---

## Beginning Work

When project notes are relevant to the current prompt:

- read relevant project notes
- verify they still match reality
- correct stale information

Never modify code because notes are outdated.

Update the notes instead.

---

## Ending Work

After significant work, when project notes are relevant:

- remove stale information
- condense redundant notes
- merge duplicate notes where appropriate
- update remaining work
- record important discoveries
- reevaluate previous decisions

Project notes should represent the project's current mental model, not its
historical timeline.

Record important context only. Avoid scratch notes, obvious facts, command
transcripts, and details that are already easy to discover from the repository.

---

## Suggested Sections

- Current Goal
- Current Status
- Completed Work
- Remaining Work
- Decisions
- Rejected Approaches
- Assumptions
- Known Risks
- Open Questions
- Surprises / Things Learned
- Next Steps

Keep notes concise.

---

## Confidence

When recording significant decisions, include confidence.

High
: verified through implementation or tests

Medium
: likely correct but not fully validated

Low
: hypothesis requiring validation

Clearly distinguish between:

- facts
- decisions
- hypotheses
- future work
