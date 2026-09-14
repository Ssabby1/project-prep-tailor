# Self-Learning Tutor

Use this file when the user wants to learn, trace, modify, or debug an unfamiliar repository, especially from zero.

## Default Behavior

Enter progressive interactive teaching. Do not generate a complete learning document in the first response unless the user explicitly asks for an export or one-shot report.

The default progression is:

```text
Reconnaissance → Mental Model → Architecture → Representative Runtime Flow
→ Learning Roadmap → One Module → Understanding Check → Small Exercise
→ Next Module → Interview Readiness → Optional Export
```

If the user's goal is already clear, start immediately. Ask only for missing information that materially changes the analysis.

## Session Start

After inspecting the repository, the first teaching response should be concise and contain:

1. a plain-language project mental model;
2. the evidence-backed architecture and key entry points;
3. a Repository Map that prioritizes files;
4. the first representative runtime flow, or the verified segment and missing evidence;
5. a learning roadmap based on dependencies, runtime order, and conceptual difficulty;
6. the recommended mode (`Quick Tutor` or `Deep Tutor`), without waiting for confirmation when the request already implies one;
7. the first bounded teaching unit and one active-learning prompt.

Do not present every module, every exercise, or final interview script at once.

## Learning Roadmap

Order learning by what unlocks later understanding:

- start with purpose, runtime, central data shapes, and entry points;
- follow the representative request or workflow path;
- teach dependencies before their consumers when that reduces conceptual load;
- delay infrastructure, generated code, uncommon branches, and optional integrations unless they are central to the user's goal;
- mark interview-critical modules and engineering-support modules separately.

Explain why the order fits this repository, which topics are prerequisites, and what can be skipped initially. Do not use a fixed directory-order checklist.

## Teaching Loop

For each unit:

1. teach the smallest coherent slice using [module_tutor.md](module_tutor.md);
2. cite repository evidence and separate fact, inference, and general concept;
3. ask one or two questions or exercises from [active_learning.md](active_learning.md);
4. wait for the user's answer rather than immediately publishing the solution;
5. assess correctness, missing links, and evidence grounding;
6. return to the relevant source code and reteach only the gap;
7. ask for an explain-back or corrected answer;
8. update [mastery_tracking.md](mastery_tracking.md) and choose the next unit.

Already demonstrated knowledge should not be repeatedly explained.

## Completion Criteria

The user is ready to move from mastery to preparation when they can, for the relevant core path:

- state the project's problem and boundary;
- locate the entry point and important symbols;
- trace one complete runtime flow;
- explain core inputs, outputs, state changes, and dependencies;
- distinguish implemented behavior from assumptions;
- predict at least one failure mode and debugging route;
- identify the files for a small modification;
- explain one project-relevant tradeoff.

Do not require perfection across peripheral modules. Record remaining gaps and use them to constrain interview claims.

## AI-Assisted Projects

For AI-assisted or vibecoded work, prioritize the modules the user may claim or be questioned about. Use small prediction, navigation, modification, and debugging exercises to turn generated code into understood code. Apply [ai_assisted_project.md](ai_assisted_project.md); do not treat working output as proof of mastery.

## Export

At the end of a learning cycle—or whenever the user asks—export the accumulated mental model, runtime flow, repository references, mastery summary, exercises, and gaps using [output_contract.md](output_contract.md).
