# Depth Modes

Use depth to control how much detail the final Markdown document contains. Default depth is `standard`.

## quick

Use when:
- the user has little time before an interview, defense, or review
- the user asks for a quick prep version

Output characteristics:
- concise but still evidence-labeled
- focus on the most likely questions and highest-risk claims
- avoid long module walkthroughs

Include:
- project one-liner
- top evidence sources
- 3 to 5 strongest project points
- 5 to 10 likely questions
- claims that should not be actively emphasized
- 30-second explanation
- final checklist

## standard

Use by default.

Output characteristics:
- detailed enough for Obsidian reading
- covers repo structure, modules, evidence, questions, risks, and learning notes
- avoids unnecessary exhaustive file-by-file listing

Include:
- input and evidence scope
- project background and goals
- tech stack and capability map
- repository structure and reading route
- core files and entry points
- architecture, interface flow, and data flow when evidenced
- core module review
- scenario-specific preparation
- evidence matrix
- question bank
- study gaps
- AI-assisted project understanding check
- final checklist

## deep

Use when:
- the user is preparing for an important technical interview
- the user needs thesis defense depth
- the user wants to understand design choices and implementation details
- the repo has enough evidence for deeper analysis

Output characteristics:
- module-level and flow-level analysis
- stronger emphasis on tradeoffs, alternatives, testing, deployment, and failure modes
- includes deeper questions and answer strategies

Include:
- everything in `standard`
- expanded architecture and data-flow walkthrough
- module-by-module implementation notes
- technical tradeoffs and alternatives
- dependency and integration analysis
- testing and validation review
- deployment or runtime review when evidenced
- edge cases and failure modes
- advanced question bank
- claim-risk table with conservative wording

## from-zero

Use when:
- the user says they do not understand the project
- the project was AI-assisted or vibecoded and the user needs to truly learn it
- the user wants onboarding from scratch
- the user asks for a learning path rather than only interview notes

Output characteristics:
- teaching-oriented
- explains concepts before modules
- gives a reading order and hands-on tasks
- marks what the user must be able to explain personally

Include:
- project mental model in plain language
- prerequisite concept map
- recommended repository reading order
- module-by-module learning route
- key terms and concepts
- hands-on exercises
- self-check questions
- "can I explain this?" checklist
- AI-assisted understanding checkpoints
- list of topics not to claim before understanding

## Depth Selection

If the user does not specify depth:
- use `standard`
- use `from-zero` if the user asks to learn the project from scratch
- use `deep` if the user asks for very detailed technical review or defense preparation
- use `quick` only if the user asks for fast prep or a short version
