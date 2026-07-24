# Skill: Write Tickets

## Purpose

Write implementation-ready engineering work items based on the existing
codebase.

The goal is to produce tickets that communicate *what* needs to be accomplished
and *why*, without unnecessarily prescribing *how* to implement the solution.

---

## Before Writing

Understand the current implementation.

Inspect:

- relevant source code
- tests
- existing architecture
- similar implementations
- related tickets or documentation, when available

Base the ticket on the repository as it exists today.

---

## Ticket Guidelines

A good ticket should:

- describe the problem
- explain why it matters
- define success
- identify affected systems
- identify assumptions
- identify risks
- include clear acceptance criteria

Implementation details should only be included when they are architectural
requirements rather than suggestions.

For formatting, use the template provided at `.agents/templates/issue.md`.

---

## Acceptance Criteria

Acceptance criteria should be:

- observable
- testable
- unambiguous

Avoid vague statements such as:

- "works correctly"
- "improve performance"

Instead describe measurable outcomes.

---

## Technical Investigation

If uncertainty exists:

- identify unknowns
- explain what must be investigated
- distinguish facts from hypotheses

Avoid presenting guesses as established facts.
