# Skill: Write Tickets

## Purpose

Write clear, implementation-ready engineering tickets based on the repository as
it exists today.

The goal is to produce work items that are easy for humans to understand and
useful as future AI context. Tickets should explain what needs to be
accomplished, why it matters, where to start, what success looks like, and what
is still unknown.

Avoid over-prescribing implementation unless a technical detail is an
architectural requirement or a known constraint from the current codebase.

---

## Before Writing

Understand the current implementation before drafting the ticket.

Inspect relevant:

- source code
- tests
- existing architecture
- similar implementations
- API contracts
- database/stored procedure boundaries
- user-facing screens or workflows
- related tickets, docs, or comments when available

Base the ticket on facts from the repository. If something is inferred, label it
as an assumption or hypothesis.

---

## Choose the Right Template

Use the smallest template that fully captures the work.

### Bug Template

Use `.agents/templates/bug_ticket.md` when the request is a focused defect,
regression, data issue, broken UI behavior, incorrect save/load behavior, or
small workflow failure.

Good examples:

- a field truncates
- a button calls the wrong data source
- a voided record is still treated as active
- a modal fails to populate expected values

### Feature Template

Use `.agents/templates/feature_ticket.md` when the request adds new behavior, expands a
workflow, introduces a report/export, touches multiple systems, or requires
product decisions.

Good examples:

- add a missing report
- support a new reconciliation workflow
- build a new admin screen
- change a cross-system import process

### Spike Template

Use `.agents/templates/spike_ticket.md` when there is not enough information to safely
write an implementation ticket.

Good examples:

- legacy behavior must be mapped
- report parameters/output are unknown
- root cause could be in external systems
- business rules need confirmation
- stored procedure behavior is unavailable in the repo

A spike should produce enough knowledge to write one or more implementation
tickets later.

---

## Ticket Guidelines

A good ticket should:

- describe the problem
- explain why it matters
- define success
- identify affected systems
- include useful code references
- distinguish facts from assumptions
- identify risks and unknowns when relevant
- include observable, testable acceptance criteria

Implementation details should only be included when they are:

- required by architecture
- necessary to avoid a known pitfall
- part of an existing pattern that must be followed
- needed to identify the affected system boundary

Avoid speculative implementation instructions.

---

## Code References

When possible, include precise references to files, functions, endpoints,
components, jobs, migrations, stored procedures, or tests.

Prefer references that answer:

- where does the current behavior live?
- where is the likely fault boundary?
- where is a similar implementation?
- where should verification start?

Do not overload the ticket with every file touched by a search. Include the
highest-signal references.

---

## Acceptance Criteria

Acceptance criteria should be:

- observable
- testable
- unambiguous
- written from the outside-in when possible

Avoid vague statements such as:

- "works correctly"
- "improve performance"
- "handle edge cases"
- "make it better"

Prefer measurable outcomes:

- "The City, ST, ZIP field displays the full value `Vancouver, Washington 98660`."
- "A voided check does not prevent the invoice from appearing in the batch check query."
- "The exported file contains one row per selected invoice and downloads as `.xlsx`."

---

## Technical Investigation

If uncertainty exists:

- identify unknowns
- explain what must be investigated
- distinguish facts from hypotheses
- name the system or person likely needed to resolve the question

Do not present guesses as established facts.

If the uncertainty is large enough that acceptance criteria would require
guessing, write a spike instead of an implementation ticket.

---

## Sizing Guidance

Do not force every section to be long.

For small bugs, keep the ticket compact. It is acceptable for sections like
Risks or Open Questions to be short or omitted if the chosen template does not
include them.

For larger features, include more context, risks, non-goals, and assumptions so
future implementers understand the boundaries.

---

## Output

Use the selected template exactly enough to stay consistent, but do not fill
sections with boilerplate. Every line should help a human or future AI do the
work with less guessing.
