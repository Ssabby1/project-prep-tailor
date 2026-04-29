# Input Modes

`project-prep-tailor` is repo-centered. A repository is required for complete project review, onboarding, learning, interview prep, thesis defense prep, and company review prep.

No-repo modes are fallback only. They are claim-audit-only and cannot produce code-level project review.

## Full Project Prep Modes

These modes may generate complete project preparation documents because they include repository evidence.

### 1. repo-only

Input:
- project repository

Use when:
- the user wants to understand a project from scratch
- the user wants repo onboarding notes
- the user wants a general project review document
- the user has no JD, resume, thesis, defense, company, or learning context yet

Allowed output:
- project background inferred from evidence
- repository structure
- core files and entry points
- tech stack
- architecture and data flow
- core module review
- implementation walkthrough
- evidence matrix
- learning route
- question bank
- risk boundaries

### 2. repo + learning goal

Input:
- project repository
- learning goal, such as backend, AI agent, RAG, frontend architecture, data pipeline, deployment, testing, or system design

Use when:
- the user wants to learn a project by following a target direction
- the user needs a module reading order and study plan
- the user wants to understand only the parts relevant to a learning objective

Allowed output:
- all repo-only outputs
- goal-oriented reading route
- prerequisite concepts
- hands-on learning tasks
- self-check questions
- modules to prioritize or skip

### 3. repo + resume

Input:
- project repository
- resume project experience text

Use when:
- the user wants to align resume claims with repository evidence
- the user wants interview prep based on resume wording
- the user wants to identify inflated, weak, or unsupported claims

Allowed output:
- all repo-only outputs
- resume claim extraction
- claim-to-evidence matrix
- claims suitable for active discussion
- claims to mention only when asked
- claims not recommended for interview emphasis
- conservative wording suggestions

### 4. repo + JD

Input:
- project repository
- job description

Use when:
- the user wants to review the project against a target job
- the user wants to identify role-relevant capability points
- the user wants interview questions based on JD requirements and repo evidence

Allowed output:
- all repo-only outputs
- JD requirement analysis
- JD-to-repo capability mapping
- role-relevant modules and evidence
- likely interview follow-up questions
- gaps between JD requirements and repo evidence

### 5. repo + JD + resume

Input:
- project repository
- job description
- resume project experience text

Use when:
- the user wants full technical interview prep
- the user wants JD / resume / repo alignment
- the user needs project storytelling, follow-up questions, and study gaps

This is the primary technical interview prep mode.

Allowed output:
- all repo-only outputs
- JD analysis
- resume claim extraction
- JD / resume / repo three-way matrix
- 30-second and 2-minute project pitch
- technical deep-dive talking points
- high-frequency interview questions
- study checklist
- risk and boundary language

### 6. repo + thesis / defense requirement

Input:
- project repository
- thesis title, abstract, course project requirement, defense rubric, or defense target

Use when:
- the user is preparing thesis defense
- the user is preparing graduation project defense
- the user is preparing course project presentation

Allowed output:
- all repo-only outputs
- problem definition
- system design explanation
- implementation method
- testing or validation evidence
- innovation boundary
- defense question bank
- claims that need caution in academic defense

### 7. repo + company context

Input:
- project repository
- company project background, user's responsibility, review target, internship conversion requirement, or project report goal

Use when:
- the user needs company project review
- the user needs internship conversion defense
- the user needs internal technical report prep

Allowed output:
- all repo-only outputs
- business or team context from user input
- responsibility boundary
- delivery summary
- technical decisions and tradeoffs
- risk, blocker, and follow-up plan
- unsupported business impact warnings

## No-Repo Fallback Modes

No-repo modes are fallback only. They are not full project prep modes.

Before using fallback, warn the user that a full project review requires repository evidence:

> 当前缺少项目仓库，无法生成完整项目复盘文档。可以继续生成 no-repo fallback 文档，但只会包含 claims 审查、追问清单和保守话术；若需要完整项目学习文档，请提供项目仓库或在仓库目录中运行。

### 1. resume-only fallback

Input:
- resume project experience text

Use when:
- the user has no repository available
- the user only wants claim risk review and interview question preparation

Allowed output:
- claims found in the resume text
- unverifiable claims
- likely follow-up questions
- points that require repository verification
- conservative wording suggestions
- suggested materials to provide next

Forbidden output:
- repository structure
- core files
- code entry points
- concrete data flow
- API or interface flow
- module implementation details
- code reading route
- repository evidence matrix
- confirmed architecture claims
- confirmed technical depth

### 2. JD + resume fallback

Input:
- job description
- resume project experience text

Use when:
- the user has no repository available
- the user wants JD matching and interview risk review based only on resume text

Allowed output:
- JD requirement analysis
- resume claim extraction
- JD-to-resume match analysis
- likely follow-up questions
- unverifiable implementation details
- conservative interview language
- list of repo evidence needed for full prep

Required labeling:
- all implementation details must be labeled as `仅简历声称` or `待仓库验证`
- no implementation claim may be presented as verified

Forbidden output:
- repository directory structure
- core file list
- code entry points
- concrete data flow
- API or interface flow
- code reading route
- module implementation walkthrough
- repository evidence matrix
- confirmed architecture, deployment, testing, monitoring, or production-readiness claims

## Mode Selection Rule

If a repository exists, choose the most specific full mode that matches the provided context.

If no repository exists, use fallback only after warning the user. Fallback output must be visibly labeled as no-repo fallback and must not pretend to be a complete project review.
