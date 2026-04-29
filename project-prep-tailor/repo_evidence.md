# Repository Evidence

When a repository is available, inspect it before writing the final project prep document. Prefer high-signal evidence over broad listing.

## High-Signal Files

Prioritize:
- `README`, project docs, architecture docs, design notes
- package manifests and dependency files
- source entry points
- API route definitions
- service, controller, model, schema, repository, DAO, workflow, or agent files
- database migrations or schema files
- config files and environment examples
- tests
- Docker, compose, CI, deployment, and runtime files

Down-rank:
- generated files
- dependency directories
- build artifacts
- caches
- minified assets
- unrelated images and static files
- lockfiles unless dependency confirmation is needed

## Repository Review Steps

1. Identify project type and likely runtime.
2. Identify entry points.
3. Identify major directories and module boundaries.
4. Identify external dependencies and whether they are actually wired into code.
5. Trace core user or system flows when possible.
6. Identify data models, storage, API boundaries, background jobs, retrieval flows, or agent workflows where relevant.
7. Check tests, deployment, and configuration evidence.
8. Record unknowns and weak evidence.

## Output Evidence

When writing repository structure, include only directories that help understanding.

When naming core files, explain why each file matters:

| File | Role | Evidence Level | Why It Matters |
|---|---|---|---|

When describing flows, separate confirmed flow from inferred flow:
- confirmed by route/service/model code
- inferred from naming or partial wiring
- unknown because files are missing or not inspected

## Avoid Overclaiming

Do not claim:
- a service is production-grade because Docker exists
- a project has robust tests because a test framework exists
- a full agent workflow exists because an LLM SDK is installed
- a system is scalable because it uses a common backend framework
- a feature is complete because a directory exists

## Reading Route

A useful reading route should tell the user:
- where to start
- what to read next
- what each module teaches
- which files are core
- which files are optional
- what to skip initially

For `from-zero`, include a learning sequence:
1. project overview
2. runtime setup or entry point
3. request or workflow flow
4. data model
5. core business logic
6. integrations
7. tests and deployment
8. extension exercises
