# CONTRIBUTING.md

# Purpose

The goal of this repository is **not** to maximize implementation speed.

The goal is to produce software that is understandable, maintainable,
well-tested, and easy for humans to own long after the implementation is
complete.

When tradeoffs exist between speed and maintainability, prefer maintainability
unless explicitly instructed otherwise.

---

# Engineering Principles

## Optimize for future maintainers

Every implementation should make the codebase easier to understand.

Prefer:

- simple solutions
- boring solutions
- idiomatic solutions
- well-known patterns
- explicitness over cleverness

Avoid introducing abstraction until it provides clear value.

---

## Code ownership

Assume another engineer will eventually debug, extend, or replace everything you
write.

Produce code that someone unfamiliar with the feature can understand quickly.

---

# Working Within the Project

## Getting started

Each project should document its local setup steps here.

Include:

- supported runtime versions
- required system dependencies
- package installation commands
- environment variables
- database or service setup
- seed data or fixture setup

Prefer copyable commands where possible.

Example:

```sh
[install dependencies]
[copy environment file]
[run database setup]
[start development server]
```

---

## Common commands

Document the commands contributors should use most often.

At minimum, define:

- how to run the app locally
- how to run the full test suite
- how to run focused tests
- how to run linters
- how to run formatters
- how to run type checks, if applicable

Example:

```sh
[run app]
[run tests]
[run focused test]
[run linter]
[run formatter]
[run type check]
```

If commands differ by package, service, or workspace, document those differences
explicitly.

---

## Before making changes

Before starting work:

- read the relevant code
- read nearby tests
- understand existing patterns
- check related documentation
- identify the smallest reasonable change

For ambiguous work, clarify the expected behavior before implementation.

---

## Match the existing project

Unless there is a compelling reason not to:

- follow existing architecture
- follow project conventions
- follow naming conventions
- follow formatting
- follow dependency choices

Avoid introducing new frameworks or architectural patterns without
justification.

---

## Keep changes focused

Prefer:

- small changes
- isolated features
- incremental improvements

Avoid mixing unrelated improvements into the same change.

---

## Minimize complexity

Before introducing new code, ask:

- Can this be simpler?
- Can existing code solve this?
- Is this abstraction necessary?
- Would an experienced maintainer merge this?

---

## Document assumptions

Whenever assumptions are made, make them explicit.

Examples include:

- API guarantees
- lifecycle assumptions
- concurrency expectations
- performance assumptions
- data invariants

Avoid relying on hidden assumptions.

---

# Architecture

Respect existing architectural boundaries.

Avoid leaking implementation details across layers.

Prefer separation of concerns.

When introducing new architecture, explain:

- why it is needed
- alternatives considered
- why those alternatives were rejected

When appropriate, follow principles such as:

- the Law of Demeter
- clean architectural boundaries

---

# Testing

Every implementation should increase confidence in the software.

Tests should verify:

- expected behavior
- edge cases
- failure scenarios
- regressions

Prefer meaningful tests over coverage for coverage's sake.

Maintain or improve repository coverage goals where applicable.

Never knowingly reduce confidence in the test suite.

---

# Documentation

Code should be self-explanatory where possible.

When documentation is appropriate:

- update existing documentation
- document public APIs
- explain non-obvious behavior
- document architectural decisions

Avoid documenting implementation details that are likely to change frequently.

---

# Structural vs Behavioral Changes

Keep behavioral and structural changes separate whenever practical.

Behavioral changes intentionally change what the software does.

Structural changes improve maintainability without intentionally changing
behavior.

During behavioral work:

- fix directly related issues
- remove obsolete code
- make small readability improvements

Avoid unrelated cleanup or broad refactoring.

If larger structural improvements are needed, implement them separately whenever
practical.

---

# Code Review

Before considering work complete, review it critically.

Review for:

- correctness
- readability
- maintainability
- unnecessary complexity
- naming
- consistency
- edge cases
- tests
- documentation

Review your own work with the same standards you would apply to another
contributor's pull request.

---

# Pull Requests

Pull requests should be easy to review.

Prefer PRs that:

- have a clear purpose
- explain the user-facing or maintainer-facing impact
- identify meaningful tradeoffs
- call out risky areas
- include testing notes
- avoid unrelated cleanup

When opening a PR, include:

- summary of changes
- tests performed
- screenshots or recordings for UI changes, when useful
- migration or deployment notes, when applicable
- follow-up work that is intentionally out of scope

---

# Review Expectations

Reviewers should prioritize correctness, maintainability, and clarity.

Review feedback should distinguish between:

- blocking issues
- important non-blocking concerns
- optional suggestions
- personal preferences

Authors should respond to material feedback by either making a change or
explaining why a different tradeoff is appropriate.

---

# Failure Recovery

If implementation becomes significantly more complex than expected:

Stop.

Reevaluate.

Explain:

- what changed
- why the original approach became unsuitable
- possible alternatives

Do not continue adding complexity solely to preserve the original approach.

---

# Definition of Done

Work is considered complete when it is:

- correct
- maintainable
- appropriately tested
- documented where necessary
- understandable
- reviewable
- easy to extend
- easy to debug
