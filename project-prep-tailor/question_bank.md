# Question Bank And Exercise Categories

Use these categories to select the next interactive question. Ask one question at a time in tutor or interview mode; do not automatically emit a static bank with model answers.

## Core Project Understanding

- What problem does this project solve, and what is outside its boundary?
- Where does the program start?
- Trace a representative request or job from input to response.
- Which data shape or state object is central?
- Which modules are core, and why are the others supporting?

## Implementation And Navigation

- Which `path::symbol` performs the decisive transformation?
- Where is a dependency registered, and where is it actually called?
- Where does input validation, persistence, external I/O, or error handling occur?
- If a handoff fails, which file or runtime evidence would you inspect first?

## Design And Tradeoffs

- Why is this layer or abstraction useful in the observed flow?
- Which rationale is proven, and which is inferred?
- Could a simpler deterministic path replace the current agent/workflow?
- What relevant alternative would change complexity, reliability, or latency?

## Failure, Testing, And Operations

- What happens for an empty result, invalid input, timeout, or dependency failure?
- Which tests exercise the main path, and what important behavior remains untested?
- What does repository evidence establish about deployment, observability, scale, and reliability?
- How would you reproduce and narrow a concrete failure?

## Modification

- To add or change a small behavior, which files and symbols would need modification?
- What contract, schema, test, or state transition must remain compatible?
- How would you verify that the change follows the representative runtime flow?

## AI-Specific Categories

When present in the repository, ask about prompt construction, LLM invocation, structured output, tool registration and execution, agent termination, memory/state, retrieval and context construction, evaluation, retries, streaming, concurrency, and guardrails. Require the project-specific implementation before accepting a general definition.

## Scenario-Specific Categories

- **Interview:** project pitch, runtime, design choices, failure modes, debugging, scale boundaries, JD relevance, resume claims, contribution, and AI assistance.
- **Thesis defense:** problem definition, method, validation, innovation boundary, limitations, and self-implemented versus third-party parts.
- **Company review:** scope, responsibility boundary, delivery, decisions, blockers, collaboration, business evidence, and next steps.
- **Self-learning:** prediction, navigation, explain-back, modification, and debugging checks from [active_learning.md](active_learning.md).

## Evaluation Discipline

Evaluate answers against repository evidence and user context. When an answer is generic, ask for the concrete source and runtime role. When it overclaims, state the boundary. When it reveals a gap, return to Tutor Mode and ask for a revised answer after targeted teaching.

Use a question table only for a requested export:

| Question | Why It Matters | User's Corrected Answer Points | Evidence Anchor | Remaining Risk |
|---|---|---|---|---|
