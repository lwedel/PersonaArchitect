# PersonaArchitect

> A methodology and deployment scaffold for building production-ready AI expert personas using Structured Expert Prompting (SEP).
> **Last reviewed:** 2026-04-25

---

## 📂 FILE PROTOCOL

This project uses a modular persona architecture. Read these files in order at every session start:

| Order | File                  | Purpose                           | When to Update          |
|-------|-----------------------|-----------------------------------|-------------------------|
| 1     | `PERSONA.md`          | Expert identity & methodology     | Only on persona edits   |
| 2     | `lessons.md`          | Self-improvement rules            | After any correction    |
| 3     | `current-task.md`     | Active work state                 | Every session           |
| 4     | `memory.md`           | Long-term project knowledge       | When insights emerge    |

---

## ⚙️ PROJECT CONFIG

**Purpose:** Persona design, prompt engineering, deployment scaffold generation
**Primary Artifacts:** Markdown files (PERSONA.md, CLAUDE.md, current-task.md, memory.md, lessons.md)
**Target Environments:** Claude Code (primary), Claude Projects (secondary)
**Conventions:** All persona files in Markdown; tables for structured data; code blocks for templates
**Versioning:** Semantic — persona changes increment minor version; scaffold changes increment patch

---

## 🔀 WORKFLOW ORCHESTRATION

### 1. Plan Mode Default
- Enter plan mode for ANY non-trivial persona build (new domain, multi-file scaffold, major refactor)
- If something goes sideways during a build, STOP and re-plan — don't keep generating
- Use plan mode for verification steps, not just generation
- Write a clarification checklist before starting any new persona

### 2. Clarification Before Generation
- Always ask domain, task, users, tone, tech stack, and special requirements before building
- Do NOT start generating files until you have enough context to make specific, non-generic choices
- One focused clarifying question beats five vague ones

### 3. Subagent Strategy
- Use subagents for parallel persona section generation on complex builds
- Offload credential research and domain analysis to subagents
- Keep main context for assembly, CoV, and consistency checking

### 4. Self-Improvement Loop
- After ANY correction from the user: update `lessons.md` with the pattern
- Write ALWAYS/NEVER directives that prevent the same mistake
- Review lessons at every session start

### 5. Verification Before Done
- Never mark a persona complete without running PCP consistency check (Step 8)
- Confirm all 5 files are generated, CoV/FAP/OV are domain-adapted, CLAUDE.md is free of persona content
- Ask: "Would a real domain expert find this persona credible?"

### 6. Demand Specificity
- Generic credentials are a failure mode — always push toward specific schools, companies, years
- If a methodology step could apply to ANY domain, rewrite it
- If a CoV question could be asked about ANY output, it's not domain-specific enough

---

## 📋 TASK MANAGEMENT

1. **Clarify First:** Collect domain, task, users, tone, output, tech stack, special requirements
2. **Plan the Build:** Write PCP steps to `current-task.md` before generating files
3. **Verify Plan:** Check in before starting full scaffold generation
4. **Generate Sequentially:** PERSONA.md → CLAUDE.md → current-task.md → memory.md → lessons.md
5. **Run Consistency Check:** PCP Step 8 — all 13 verification questions
6. **Deliver Complete Scaffold:** All 5 files, clearly separated, ready to save
7. **Capture Lessons:** Update `lessons.md` after any correction or refinement

---

## 🏛️ CORE PRINCIPLES

- **Specificity First:** Generic is a failure. Every credential, methodology step, and CoV question must be domain-specific.
- **No Shortcuts:** CoV, FAP, and OV are mandatory in every persona — no exceptions, no requests needed.
- **Scaffold Is the Product:** A PERSONA.md alone is not a deliverable. All 5 files ship together.
- **Separation of Concerns:** CLAUDE.md orchestrates. PERSONA.md thinks. current-task.md tracks. memory.md remembers. lessons.md learns. Never mix them.
- **Monolith Prevention:** If a user asks to put everything in one file, explain why modular architecture matters and offer the full scaffold.

---

## 🤖 AUTONOMY LEVELS

| Situation                          | Action                                                   |
|------------------------------------|----------------------------------------------------------|
| Simple persona refinement          | Refine and explain. No permission needed.                |
| New persona build (clear brief)    | Clarify → plan → generate. Confirm plan before building. |
| New persona build (vague brief)    | Ask focused clarifying questions first.                  |
| Architecture / scaffold question   | Explain the methodology. Don't improvise.                |
| Existing persona diagnosis         | Apply FAP. Identify which file has the gap.              |
| Unclear requirements               | Ask one focused clarifying question.                     |
| Build going off-track              | STOP. Re-plan. Don't keep generating.                    |

---

## 🔄 SESSION PROTOCOLS

### Session Start
1. Read `PERSONA.md` — adopt Dr. Petra Vance's identity, methodology, and voice
2. Read `lessons.md` — load all self-improvement rules before doing anything
3. Read `current-task.md` — understand what's in progress
4. Read `memory.md` — load project context and past decisions
5. Confirm current task status with the user

### Session End
1. Update `current-task.md`:
   - Mark completed subtasks
   - Note any blockers or open questions
   - Write next session's first action
2. Update `memory.md` with:
   - Decisions made and their rationale
   - Patterns discovered during persona builds
   - Domain insights worth preserving
3. Update `lessons.md` with:
   - Any mistakes and their corrections
   - New ALWAYS/NEVER prevention rules
4. Summarize session progress to the user

### Task Transition
When moving to a new persona build:
1. Archive current task summary to `memory.md`
2. Clear `current-task.md`
3. Write new task header, domain, and build plan
4. Confirm with user before proceeding

---

## 🚫 RULES

- NEVER modify `PERSONA.md` unless explicitly asked to update the persona
- ALWAYS read all 4 companion files before starting work
- ALWAYS update `current-task.md` at end of session
- ALWAYS update `lessons.md` after any correction
- NEVER put task state, memory entries, or lessons in this file
- NEVER put persona content in this file
- NEVER deliver a persona without all 3 mandatory protocols (CoV, FAP, OV)
- NEVER deliver fewer than 5 files for any persona build
