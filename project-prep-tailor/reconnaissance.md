# Repository Reconnaissance

Use this stage before detailed teaching or scenario preparation. The goal is a high-signal map, not an exhaustive inventory.

## Inspect

Identify from repository evidence:

- project type, languages, frameworks, package managers, and key dependencies;
- major directories and module boundaries;
- executable, API, worker, CLI, event, UI, and test entry points;
- APIs, schemas, databases or storage, AI frameworks, and external services;
- runtime, configuration, deployment, CI, and test setup;
- generated, vendored, boilerplate, build, cache, and low-priority content.

Use available search, symbol navigation, manifests, configuration, tests, and git context. Do not add a parser, database, or dependency-graph service for ordinary reconnaissance.

## Progressive Repository Scoping

First determine whether the target is a large repository or monorepo and what the user is trying to learn, trace, prepare, modify, or debug. Do not initially inventory every package, README, source tree, service, example, or legacy area.

For a large repository:

1. identify the relevant subproject, package, service, or feature boundary;
2. inspect its manifests, main entry point, key configuration, high-signal implementation files, and tests related to the representative flow;
3. build a **Provisional Repository Map** for that scope;
4. trace the representative runtime flow within and across only the boundaries it actually reaches;
5. expand to another package or service only when an evidenced dependency, unresolved flow edge, or user goal requires it.

State explicitly that a provisional map covers the current goal and is not evidence that the entire repository has been analyzed. If the user's target is broad or unstated, infer a safe initial scope from the requested feature or most representative entry point and disclose that choice; ask only when different scopes would materially change the work.

## Classify

Classify only the meaningful areas:

| Priority | Meaning |
|---|---|
| Core | Directly implements the representative runtime flow or central domain behavior |
| Important | Needed to understand, operate, test, or modify core behavior |
| Supporting | Useful helpers, secondary features, or non-central integrations |
| Infrastructure | Build, deployment, CI, runtime configuration, observability |
| Generated / Boilerplate | Machine-generated, scaffolded, vendored, or standard framework output |
| Low Priority | Not relevant to the user's current goal or representative flow |

Classification is contextual: a deployment file may be Core for a deployment-learning goal and Infrastructure otherwise.

## Repository Map

Present a compact map such as:

| Area / File | Priority | Role | Evidence Anchor | Learn Now? |
|---|---|---|---|---|

Include the project type, stack, likely runtime, key entry points, central data/storage, external integrations, test/runtime evidence, and important unknowns. Use file paths and symbols where available. Avoid listing every file.

For a large repository, add the current scope, excluded/deferred areas, and the condition that would cause scope expansion. Do not build a complete dependency graph unless the task genuinely requires one.

## Exit Condition

Reconnaissance is sufficient when the agent can select a representative real flow, name the evidence-backed entry points, identify the core areas, and state what should be deferred. In a large repository, sufficiency applies to the disclosed current scope. Resolve critical ambiguity before detailed teaching; record non-critical unknowns instead of blocking progress.
