# AI-Assisted And Vibecoding Projects

AI-assisted projects are allowed, but the output must help the user understand and explain the project honestly. Do not disguise AI assistance as unsupported independent engineering depth.

## Core Principles

- Do not shame AI-assisted work.
- Do not inflate AI-assisted work.
- Help the user identify what they truly understand.
- Separate generated code, user-modified code, and user-understood code when evidence or user context allows.
- Do not claim independent architecture design unless evidence supports it.

## Understanding Check

Include this section for AI-assisted or suspected vibecoding projects:

| Module | What You Must Be Able To Explain | Evidence | Current Risk | Study Priority |
|---|---|---|---|---|

Ask the user to be able to explain:
- what problem the module solves
- where the entry point is
- what data enters and leaves
- which dependency is used and why
- what happens on failure
- what they changed or understood personally

## Honest Interview Wording

Good wording:
- "我使用 AI 辅助完成了初版实现，但我重点理解和调整了..."
- "这部分代码是基于 AI 辅助生成后，我围绕数据流、异常处理和接口行为做了验证。"
- "我能解释核心流程，但某些工程化细节还需要继续补充。"

Risky wording:
- "我独立设计并实现了完整架构。"
- "这个系统已经达到生产级。"
- "我完整掌握了所有模块。"
- "性能和稳定性都有明显提升。"

Use risky wording only if repository evidence and user context strongly support it.

## Vibecoding Risk Signals

Mark as higher risk when:
- code exists but README is thin
- many dependencies are present but flows are unclear
- no tests or examples exist
- project runs but the user cannot explain modules
- resume claims exceed repository evidence
- architecture terms appear without implementation support

## Study Before Claiming

Before the user actively emphasizes a module, they should be able to:
- locate the core files
- trace one complete flow
- explain one design tradeoff
- describe one bug or edge case
- modify a small behavior safely
- state what is not implemented
