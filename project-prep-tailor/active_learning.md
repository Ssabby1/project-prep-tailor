# Active Learning

Use active checks throughout repository learning and interview preparation. Questions must point back to the actual repository and current learning goal.

## Exercise Types

- **Prediction:** ask what happens for a concrete input, empty result, exception, or state transition.
- **Code Navigation:** ask where the user would look for an entry point, missing handoff, validation, persistence, tool registration, or error.
- **Explain Back:** ask the user to reconstruct a flow or module in their own words without copying the prior explanation.
- **Modification Exercise:** ask which files and symbols would change for a small feature before writing code.
- **Debugging Exercise:** present a repository-plausible failure and ask for the first evidence to inspect and why.

## Interaction Protocol

1. Ask one meaningful question, or at most two tightly related questions.
2. Do not reveal the complete answer in the same turn.
3. Wait for the user's response.
4. Evaluate technical correctness, missing hops, unsupported assumptions, and evidence use.
5. Point to the decisive repository evidence and explain only the gap.
6. Ask the user to revise, explain back, or apply the correction.
7. Update mastery status only from demonstrated performance.

If the user explicitly asks for the answer or cannot proceed after a useful attempt, provide a scaffolded answer and then ask a smaller verification question.

## Quality Rules

- Avoid trivia, filename memorization, and questions answerable only by guessing.
- Test causal understanding: what enters, what changes, what calls next, what can fail, and where to modify or debug.
- Do not require the user to know a peripheral module before the main flow.
- Make exercises safe and small. Planning a modification is enough unless the user asks to edit code.
- Do not interpret silence or agreement as mastery.
