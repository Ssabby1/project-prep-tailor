# Module Tutor

Teach one bounded core module or tightly coupled slice at a time. Select modules from the runtime flow and learning roadmap rather than directory order.

## Lesson Shape

Adapt this structure to the module; omit fields that do not apply.

### A. Purpose

State what problem the module solves in this repository.

### B. Runtime Role

Show where it appears in the representative flow and what triggers it.

### C. Inputs, Outputs, And State

Identify inputs, outputs, validation, mutation, persistence, and side effects.

### D. Dependencies

Name what it calls and what calls it. Distinguish construction/registration from runtime invocation.

### E. Important Files And Symbols

List only the files, functions, classes, schemas, interfaces, services, or models required to understand this unit. Use `path::symbol` and reliable line references when available.

### F. Real Code Walkthrough

Walk through a small amount of decisive code. Emphasize control flow, data flow, state, external calls, error handling, and the handoff to the next module. Avoid large source dumps.

### G. Why This Design

Use `[Repo Fact]` for documented or encoded constraints and `[Inference]` for plausible rationale. Do not present a conventional design explanation as the authors' intent without evidence.

### H. General Concept

Explain only the transferable concept needed to understand this code, labeled `[General Concept]`.

### I. Alternatives And Tradeoffs

Discuss only project-relevant alternatives, such as sync/async, workflow/agent, direct call/queue, SQL/vector storage, framework/custom orchestration, or monolith/services. Tie the tradeoff back to observable constraints.

### J. Check And Apply

End with one or two active tasks: prediction, code navigation, explain-back, a small modification plan, or debugging. Do not immediately include the answer.

## Pacing

- Keep one turn to a coherent learning unit.
- Reuse the established mental model instead of restating it.
- If the answer is correct, advance or deepen; if partially correct, teach only the missing link; if unsupported, return to evidence.
- Do not move a module to interview-ready because the user merely read the explanation.
