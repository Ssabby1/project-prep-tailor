# Session And Depth Modes

Mode controls the interaction; export depth controls document detail. Do not let a request for deep analysis turn the first self-learning response into a giant document.

## Quick Tutor

Use when the user explicitly has little time or asks for a fast understanding.

Cover:

- project purpose and boundary;
- concise Repository Map and 5–10 core files;
- architecture and key entry points;
- one representative end-to-end runtime flow;
- major design decisions, limits, and debugging points;
- a small number of understanding checks;
- evidence-backed interview talking points after the checks.

Compress breadth, not evidence discipline. A quick session may combine closely related units, but should still let the user answer at least one meaningful question.

## Deep Tutor

Default for `self-learning`, `from-zero`, “吃透”, unfamiliar AI-assisted projects, and detailed learning requests.

Use the full tutor loop:

- reconnaissance and architecture;
- representative runtime flow before directory-by-directory study;
- dependency-based roadmap;
- bounded module lessons and real code walkthroughs;
- project-specific concepts and tradeoffs;
- prediction, navigation, explain-back, modification, and debugging exercises;
- mastery tracking;
- interview preparation only after relevant understanding is demonstrated.

## Interview

Use for explicit interview preparation. This is an interactive mock interview, not a static standard-answer generator.

Begin with a concise evidence baseline and representative runtime flow. Then ask one question at a time, assess the user's answer against code and claim boundaries, teach gaps, request a revised answer, and continue with deeper follow-ups. Read [interview_mode.md](interview_mode.md).

## Compatibility Aliases

Preserve existing prompts as follows:

| Existing value | v2 behavior |
|---|---|
| `quick` | `Quick Tutor` for learning/interview; concise export when explicitly requested |
| `standard` | Moderate review/export depth; for self-learning, use interactive tutoring rather than document-first behavior |
| `deep` | `Deep Tutor` or deep scenario review/export |
| `from-zero` | `Deep Tutor` with plain-language prerequisites and more frequent understanding checks |

The existing scenarios `repo-review`, `self-learning`, `interview`, `thesis-defense`, and `company-review` remain valid.

## Selection

- Infer mode when the request is clear; do not pause for confirmation.
- Default self-learning/from-zero to `Deep Tutor`.
- Default explicit interview preparation to `Interview`.
- Use `Quick Tutor` only for explicit speed or brevity.
- For repo review, defense, and company review, follow the requested deliverable; add tutoring when the user asks to learn or shows a material understanding gap.
- Treat Markdown/Obsidian as an export format, not a session mode.
