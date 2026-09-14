# End-to-End Runtime Flow

Trace a representative real behavior before teaching modules in isolation.

## Select The Flow

Choose the scenario that best reveals the system's purpose: for example a user message, API request, upload, task creation, agent invocation, tool execution, or retrieval query. The choice must come from repository evidence, not from a generic stack template.

Prefer a flow that crosses several core boundaries and is relevant to the user's goal. If multiple flows matter, fully establish one first and list the others for later.

## Trace Method

Start from an actual entry point and follow calls, registrations, events, data structures, and external boundaries. For each hop record:

| Step | Evidence Anchor | Input | Action / State Change | Output | Why This Layer | Next Hop |
|---|---|---|---|---|---|---|

An evidence anchor should normally be `path::symbol` and a reliable line or range when available. Cite the smallest useful code fragment; do not paste large source blocks.

Separate:

- `[Repo Fact]` for confirmed calls and transformations;
- `[Inference]` for an architectural purpose or an unobserved runtime assumption;
- `[General Concept]` for the pattern this hop illustrates.

Explain control flow, data flow, state, external calls, error handling, and return path. A dependency, matching function name, or nearby module is not enough to assert that an edge executes.

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
