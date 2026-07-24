# Contributing

Reusable collaboration boilerplate for projects.

This repository contains default guidance for how humans and AI agents should
work in a codebase.

## What to copy

Copy these into the root of a project:

- `CONTRIBUTING.md`
- `AGENTS.md`
- `.agents/`

Do not copy this `README.md` into consuming projects unless you want the project
to explain this boilerplate repository itself.

## How it is intended to work

`CONTRIBUTING.md` is for human contributors. It should contain the engineering
standards, setup instructions, common commands, review expectations, and
definition of done for the project.

`AGENTS.md` is for AI agents. It should add agent-specific collaboration
expectations while still requiring agents to follow `CONTRIBUTING.md`.

`.agents/` contains supporting material for AI agents, including skills, notes,
and templates.

## Recommended usage

Treat this repository as a source template, not as a runtime dependency.

For a new project:

1. Copy `CONTRIBUTING.md`, `AGENTS.md`, and `.agents/` into the project root.
2. Fill in project-specific setup, commands, and workflow details in
   `CONTRIBUTING.md`.
3. Add or remove `.agents/` skills and templates based on what the project
   actually needs.
4. Keep project notes concise, durable, and verified against the current
   repository.

Avoid using this repository as a git submodule. These files are meant to be
customized per project, and they work best when they live directly in the
project root.

## Updating existing projects

When this boilerplate improves, copy changes into existing projects
intentionally.

Review differences before overwriting local files, because consuming projects
may have project-specific guidance that should be preserved.
