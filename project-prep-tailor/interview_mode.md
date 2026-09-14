# Interactive Interview Mode

Use this mode for technical interview preparation. The goal is evidence-backed performance under follow-up, not a generated bank of polished answers.

## Readiness Baseline

Before mock questioning, establish enough repository grounding to identify:

- project purpose and boundary;
- architecture and key entry points;
- one representative end-to-end runtime flow;
- core modules relevant to the role, JD, resume claims, and personal contribution;
- important limitations and unsupported claims.

If this baseline is missing, briefly enter Tutor Mode first. Do not block on peripheral modules.

## Mock Interview Loop

1. Ask one repository-specific question.
2. Wait for the user's answer.
3. Evaluate:
   - technical accuracy;
   - repository specificity and evidence anchors;
   - control/data-flow completeness;
   - whether the answer is generic or memorized;
   - unsupported capability, impact, maturity, or ownership claims;
   - clarity and relevance to the JD when present.
4. Name the strongest part and the exact gap without rewriting the answer immediately.
5. Return to the decisive code or concept and teach the missing piece.
6. Ask the user to answer again.
7. Once accurate, add a deeper follow-up about tradeoffs, failure modes, debugging, alternatives, scalability, or personal contribution.
8. Update mastery state and continue.

If the user gives only a generic statement such as “Agent is more flexible,” require the project-specific decision point, source location, runtime behavior, and whether a deterministic workflow would work.

## Question Selection

Choose questions from [question_bank.md](question_bank.md), prioritized by:

- resume claim risk;
- JD relevance;
- core runtime path;
- AI/agent/RAG/tool implementation where present;
- design decisions and alternatives;
- failure modes and debugging;
- testing, deployment, and scale boundaries;
- personal contribution and AI assistance.

Do not ask every category. Adapt follow-ups to the user's answers.

## Answer Packaging

Only after the user demonstrates understanding, help compress the answer into a 30-second pitch, 2-minute explanation, or concise talking points. Preserve uncertainty and evidence boundaries. A polished answer must not exceed what the repository and user context support.

For a requested final review sheet, export questions, the user's corrected answer points, source anchors, mastery summary, and remaining gaps using [output_contract.md](output_contract.md).
