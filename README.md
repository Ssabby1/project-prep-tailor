# project-prep-tailor

[中文说明](README.zh-CN.md)

`project-prep-tailor` v2 is a repository-grounded interactive project tutor and preparation skill. It helps users master a real codebase first, then prepare accurate interview, resume/JD, thesis-defense, company-review, or onboarding material.

## What Changed In v2

For self-learning and from-zero requests, the default is no longer a complete Markdown report. The skill now follows:

```text
Repository reconnaissance → architecture → representative runtime flow
→ dependency-based roadmap → module tutoring → active checks
→ small modification/debugging tasks → interview preparation → optional export
```

It uses three provenance labels for project explanations:

- `[Repo Fact]`: directly verified in source, cited with file and symbol;
- `[Inference]`: a reasoned but unproven interpretation;
- `[General Concept]`: transferable knowledge tied to the inspected code.

Existing claim-strength labels and anti-fabrication rules remain in place for resume, impact, ownership, maturity, and production claims.

## Goals

- **Project Mastery:** purpose, architecture, entry points, runtime flow, modules, dependencies, AI/RAG/agent/tool implementation, failure modes, modifications, and debugging.
- **Project Preparation:** interactive interview practice, JD alignment, resume claim audit, thesis defense, company review, and honest AI-assisted project explanations.

The core rule is: understand first, express second.

## Modes

- `Quick Tutor`: fast mental model, Repository Map, core files, one real flow, key decisions, limits, and checks.
- `Deep Tutor`: progressive module learning, code walkthroughs, exercises, and mastery tracking.
- `Interview`: one-question-at-a-time mock interview with source checks and Tutor Mode fallback.

Existing `quick`, `standard`, `deep`, and `from-zero` prompts remain compatible. `self-learning`/`from-zero` defaults to Deep Tutor; interview requests default to interactive Interview mode.

## Inputs And Scenarios

Repository-grounded modes still support:

- repo-only;
- repo + learning goal;
- repo + resume;
- repo + JD;
- repo + JD + resume;
- repo + thesis/defense requirement;
- repo + company context.

Scenarios remain `repo-review`, `self-learning`, `interview`, `thesis-defense`, and `company-review`.

Without a repository, the skill is limited to claim audit and conservative wording. It must not invent source structure, runtime flows, implementation, maturity, or personal contribution.

## Usage

Interactive learning:

```text
Use $project-prep-tailor to teach me this repository from zero.
Trace one real request first, then teach one module at a time and test my understanding.
Learning goal: understand the backend and agent tool flow.
```

Interview preparation:

```text
Use $project-prep-tailor to run an evidence-grounded mock interview for this repository.
JD: ...
Resume project text: ...
```

Export after learning:

```text
Export our current project learning state as Obsidian-friendly Markdown, including the runtime flow, source anchors, mastery summary, and remaining gaps.
```

See [docs/usage.zh-CN.md](docs/usage.zh-CN.md) and the tool-specific docs for more examples.

## Scope

This remains a lightweight skill/prompt package. v2 adds workflow guidance, not a parser, database, persistent learning-state service, Web UI, or model-calling CLI.
