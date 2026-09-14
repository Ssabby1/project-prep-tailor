# Mastery Tracking

Maintain lightweight state in the current conversation. Do not create a database or persistent tracking system unless the user explicitly requests one.

## States

Use the highest demonstrated state per core module:

1. `Not Studied`
2. `Introduced`
3. `Understands Conceptually`
4. `Understands Implementation`
5. `Can Explain`
6. `Can Modify`
7. `Interview Ready`

These states are cumulative only when prior abilities remain demonstrated. `Interview Ready` also requires accurate scope and evidence boundaries.

## Evidence For Advancement

| State | Minimum signal |
|---|---|
| Introduced | The module and its role were taught |
| Understands Conceptually | User can explain the problem and general pattern |
| Understands Implementation | User can trace important symbols, inputs, outputs, and state |
| Can Explain | User gives a coherent repository-specific explain-back |
| Can Modify | User correctly identifies a safe change path or completes a small change |
| Interview Ready | User answers accurately, handles follow-ups, tradeoffs, limits, and contribution boundaries |

Reading an explanation, receiving a model answer, or having runnable code is not sufficient evidence by itself.

## Display

Show a compact table only when it helps choose the next step or the user asks for status:

| Module | State | Evidence From User | Gap | Next Check |
|---|---|---|---|---|

Do not repeat the full table every turn. Track only core modules and claims relevant to the goal.

## Routing

- Advance when the user demonstrates the current level.
- If a later answer reveals a misconception, lower or qualify the state and reteach the exact gap.
- Do not repeat mastered material unless it is a prerequisite for a new flow.
- Use remaining gaps to constrain exports, resume wording, and interview talking points.
