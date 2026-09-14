# End-to-End Runtime Flow

Construct an evidence-backed representative flow before teaching modules in isolation, and distinguish its statically supported edges from runtime-confirmed behavior.

## Select The Flow

Choose the scenario that best reveals the system's purpose: for example a user message, API request, upload, task creation, agent invocation, tool execution, or retrieval query. The choice must come from repository evidence, not from a generic stack template.

Prefer a flow that crosses several core boundaries and is relevant to the user's goal. If multiple flows matter, fully establish one first and list the others for later.

## Trace Method

Start from an actual entry point and follow calls, registrations, events, data structures, and external boundaries. For each hop record:

| Step | Evidence Anchor | Evidence Type | Input | Action / State Change | Output | Why This Layer | Next Hop |
|---|---|---|---|---|---|---|---|

An evidence anchor should normally be `path::symbol` and a reliable line or range when available. Cite the smallest useful code fragment; do not paste large source blocks.

Use `Static`, `Test`, `Runtime`, or `External / User-provided` as the evidence type when flow complexity or confidence makes it useful. Do not force the table into every answer.

Separate:

- `[Repo Fact]` for inspected code, registrations, calls, and transformations, with the evidence type stating whether support is static, test-based, or runtime-confirmed;
- `[Inference]` for an architectural purpose or an unobserved runtime assumption;
- `[General Concept]` for the pattern this hop illustrates.

Explain control flow, data flow, state, external calls, error handling, and return path. A dependency, matching function name, or nearby module is not enough to assert that an edge executes.

## Runtime Verification Ladder

Increase confidence only as evidence supports it:

1. **Level 1 — Static Inspection:** inspect source, symbols, call sites, registration, configuration, tests, and dependency wiring. Describe static wiring as static; use `[Inference]` for the behavior expected when a dynamic condition occurs.
2. **Level 2 — Existing Tests:** inspect the smallest relevant unit, integration, or targeted test. Run it when safe and useful; do not run a large suite merely to verify one edge unless broader execution is necessary.
3. **Level 3 — Safe Targeted Execution:** when static evidence remains ambiguous, prefer a pure function, local demo, single CLI operation, mock request, fake data, test environment, sandbox, or dry run. Verify the smallest important edge rather than starting the full production system.
4. **Level 4 — Runtime Logs / Trace:** use existing logs, traces, test output, observability, or safe local execution output to verify call order and state transitions. Treat user-provided or external runtime artifacts as such and assess their scope and reliability.
5. **Level 5 — Confirmed Runtime Behavior:** use `[Repo Fact — Runtime Confirmed]` only when tests, safe execution, logs, traces, or equivalent evidence sufficiently establish the stated path. Name the confirming evidence and keep the conclusion within its environment and inputs.

Each level adds confidence but does not automatically prove production behavior, all inputs, or personal authorship. A passing unit test proves the tested case; local execution proves that local case; neither alone proves a production deployment.

## Execution Safety

Before running code, consider side effects, environment, secrets, network calls, cost, and whether the action is within the user's request and permissions. Follow the high-risk operation boundary in [safety_rules.md](safety_rules.md).

If dynamic verification would deploy, mutate real data or infrastructure, send real communications, perform financial/payment actions, expose or upload private data/secrets, incur substantial paid-API usage, run a destructive migration, or execute a script with unclear effects, do not run it automatically. Continue static/test analysis, state the unverified edge, name the evidence needed, and seek a mock, sandbox, test, or dry-run alternative.

## Incomplete Or Dynamic Flows

For dependency injection, framework registration, callbacks, queues, reflection, model-selected tools, or remote services, distinguish static wiring from observed runtime behavior.

If a complete path cannot be verified:

1. show the longest confirmed segment;
2. mark the missing or dynamic edge explicitly;
3. name the file, runtime log, test, configuration, or execution needed to verify it;
4. do not replace the gap with a plausible template.

Do not proceed to a confident module-by-module explanation of the missing link. Teach the confirmed segment and make the unknown a navigation or debugging exercise when appropriate.

## Understanding Check

Before moving on, ask the user to predict a hop, explain the flow back, locate where a value changes shape, or identify where they would debug a failure. Use [active_learning.md](active_learning.md) and update [mastery_tracking.md](mastery_tracking.md).
