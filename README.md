# project-prep-tailor

[中文说明](README.zh-CN.md)

`project-prep-tailor` is a lite, evidence-first skill for project review, learning, interview prep, thesis defense prep, company review prep, and claim-risk audit.

It generates detailed Obsidian-friendly Markdown documents from a project repository and optional context such as a learning goal, resume project text, job description, defense requirement, or company review background.

## Positioning

This project is not a client, model runner, or API-based CLI. It is a reusable skill and prompt package for Codex, Claude Code, Cursor, and similar AI coding tools.

The core value is repo-based understanding:

- inspect repository evidence
- explain project structure and flows
- map resume or JD claims to evidence
- prepare interview, defense, company review, or self-learning notes
- identify unsupported or risky claims
- handle AI-assisted / vibecoding projects honestly

## Relationship To repo-to-resume-tailor

`repo-to-resume-tailor`:

```text
repository + target role / JD -> resume-ready project description
```

`project-prep-tailor`:

```text
repository + optional context -> project prep, learning, interview, defense, or review document
```

The first writes resume text. This skill helps the user understand and explain the project.

## Repo-First Modes

Full project prep requires a repository:

- repo-only
- repo + learning goal
- repo + resume
- repo + JD
- repo + JD + resume
- repo + thesis / defense requirement
- repo + company context

No-repo fallback is claim-audit-only and must not generate repository structure, core files, data flow, API flow, module implementation details, code reading routes, or repository evidence matrices.

## Scenarios

- interview
- thesis-defense
- company-review
- self-learning
- repo-review

## Depth

- quick
- standard
- deep
- from-zero

Default output is `standard` depth and Obsidian-friendly Markdown.

## MVP Scope

This lite MVP intentionally does not include:

- client UI
- API model calls
- API key configuration
- complex workflow CLI
- installer CLI
- `pyproject.toml`
- `install.py`
- `src/`

An install-only CLI may be added later as a roadmap item.

## Usage

In a repository:

```text
Use $project-prep-tailor to generate a standard repo-review document for this repository.
```

Interview prep:

```text
Use $project-prep-tailor to prepare this project for interview.
Scenario: interview
Depth: deep
JD:
...
Resume project text:
...
```

Self-learning:

```text
Use $project-prep-tailor to help me learn this repository from zero.
Scenario: self-learning
Depth: from-zero
Learning goal: understand the backend API flow.
```
