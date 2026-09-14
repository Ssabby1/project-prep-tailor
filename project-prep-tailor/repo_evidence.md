# Repository Evidence

Inspect repository evidence before teaching project-specific behavior or preparing code-level claims. Prefer high-signal call paths over broad file listing.

## High-Signal Evidence

Prioritize:

- README, architecture notes, design documents, and runnable examples;
- package manifests, runtime configuration, and environment examples;
- executable, API, UI, worker, event, and CLI entry points;
- routes, controllers, services, workflows, agents, tools, models, schemas, repositories, and migrations;
- registrations, dependency injection, callbacks, queues, and external-client wiring;
- tests that execute representative behavior;
- Docker, compose, CI, deployment, logging, and observability files when relevant.

Down-rank generated, vendored, dependency, build, cache, minified, lock, unrelated static, and boilerplate files unless needed to verify a specific fact.

## Inspection Sequence

1. Establish scope: repository root, relevant revision if known, available inputs, and important inaccessible components.
2. Perform the high-signal scan in [reconnaissance.md](reconnaissance.md).
3. Identify entry points, central data shapes, storage, external boundaries, tests, and runtime setup.
4. Select and trace a representative behavior using [runtime_flow.md](runtime_flow.md).
5. Follow actual references, calls, registrations, and transformations; distinguish installed dependencies from wired capabilities.
6. Record contradictions, dynamic edges, missing files, dead or partial implementations, and unverified runtime assumptions.
7. Use the resulting evidence to build a learning roadmap, scenario preparation, or requested export.

Run or test code only when it materially resolves an important uncertainty and remains within the user's request and permissions. Static evidence alone must not be described as observed runtime behavior.

## Evidence Anchors

For important repository-specific statements, prefer:

```text
path/to/file.ext::SymbolName (reliable line or range when available)
```

Use the smallest useful source excerpt. Line numbers are optional when tools cannot obtain them reliably; file and symbol are still expected when possible.

When describing a call path, verify each edge. A matching name, import, dependency, comment, or directory is not proof that the edge executes.

## Unknowns And Negative Evidence

State what was searched and not found when absence matters, while avoiding claims that uninspected or inaccessible systems do not exist. Examples:

- “No call site was found in the inspected source” is safer than “this dependency is unused.”
- “The repository does not provide deployment evidence” is safer than “the project was never deployed.”

If the repository cannot establish a full flow, show the longest confirmed segment and the evidence needed to close the gap. Do not fabricate a bridge.

## Teaching And Review Output

Use [reconnaissance.md](reconnaissance.md) for the Repository Map and [evidence_rules.md](evidence_rules.md) for statement labels. In tutor mode, reveal evidence in bounded units. In exports, consolidate core files and evidence matrices without turning the document into an exhaustive inventory.
