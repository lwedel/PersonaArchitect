# 🧠 Persona Architect

> **Structured Expert Prompting (SEP) — A methodology for building production-ready AI expert personas with complete deployment scaffolds.**

---

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Compatible](https://img.shields.io/badge/Claude-Compatible-blueviolet)](https://www.anthropic.com)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Optimized-blue)](https://www.anthropic.com)

---

## What Is This?

**Persona Architect** is a methodology — and a deployable AI persona (`Dr. Petra Vance`) — for building structured, expert-grade AI collaborators using Claude.

The core thesis: **generic AI assistants underperform not because of model capability, but because of poor persona architecture.** Research on the "Persona Depth Gap" demonstrates that LLMs perform significantly better when given specific, deeply constructed personas containing credentials, named methodologies, and domain-specific verification protocols.

This repository provides:

- **The Persona Construction Protocol (PCP)** — an 8-step repeatable framework for designing expert AI personas
- **The 5-File Deployment Scaffold** — a production-ready file architecture that separates identity, state, memory, and self-improvement
- **Dr. Petra Vance** — the Persona Architect herself, deployable in Claude Code or Claude Projects
- **Mandatory Protocol Templates** — Chain of Verification (CoV), Forensic Analysis Protocol (FAP), and Operational Verification (OV) for every persona type

---

## The Problem

Most AI persona prompts fail in predictable ways:

| Symptom | Root Cause |
|---------|------------|
| Inconsistent responses across sessions | No persistent state or memory architecture |
| Generic outputs despite "expert" labeling | Missing named methodology and domain-specific frameworks |
| Errors that repeat across sessions | No self-improvement mechanism |
| No root cause analysis capability | No forensic diagnostic protocol |
| Work marked "done" without verification | No operational verification step |
| Monolithic prompt files that become unmanageable | No separation of concerns |

The result: personas that feel like assistants wearing a costume — not experts with a systematic way of working.

---

## The Solution — The 5-File Scaffold

Every persona built with this methodology ships as a **complete file system**, not just a prompt document.

```
project-root/
├── CLAUDE.md         ← Session orchestrator: workflow rules, file read order, project config
├── PERSONA.md        ← Expert identity: credentials, methodology, CoV, FAP, OV
├── current-task.md   ← Active state tracker: current work, subtasks, blockers
├── memory.md         ← Long-term knowledge store: decisions, patterns, learnings
└── lessons.md        ← Self-improvement log: mistake patterns → prevention rules
```

### Separation of Concerns

| File | Responsibility | Volatility |
|------|---------------|------------|
| `CLAUDE.md` | Session orchestration + workflow discipline | Stable |
| `PERSONA.md` | Expert identity, methodology, verification protocols | Stable |
| `current-task.md` | Active work state, subtask checklist | Volatile (every session) |
| `memory.md` | Long-term project knowledge | Append-only (grows over time) |
| `lessons.md` | Mistake → prevention rule log | Append-only (after corrections) |

**Why not just one file?**

Putting everything in `CLAUDE.md` creates a monolith — a single 1000+ line file where persona identity, task state, project config, and accumulated knowledge blur together. Over time, the model can't focus on what matters per session, and the file becomes impossible to maintain.

Modular architecture solves this: each file has exactly one job, files can be updated independently, and the read order at session start ensures the right context loads at the right time.

---

## Mandatory Protocols

Every persona produced by this methodology includes three non-negotiable protocols. These are not optional add-ons — they are structural requirements.

### ✅ Chain of Verification (CoV)

**Verifies thinking before output is delivered.**

Real experts review their own work before presenting it. CoV builds this into the persona's response loop:

1. **Initial Response** — generate the first-pass answer
2. **Domain-Specific Challenge Questions** — 3–5 questions targeting the most common failure modes in the field
3. **Independent Verification** — re-examine output against each challenge question
4. **Final Revised Output** — apply corrections, note changes, flag remaining uncertainties

Challenge questions are **domain-specific**, not generic. Example:

| Domain | Example CoV Questions |
|--------|-----------------------|
| Trading / Finance | "Does this survive a black swan event?" / "Am I confusing correlation with causation?" |
| Software Engineering | "What happens when this input is null/0/∞?" / "Will this still work at 100x load?" |
| Game Development | "Is this fun, or just technically clever?" / "What happens when the player does the unexpected?" |
| Marketing / Content | "Would I click this if I saw it in the wild?" / "Is this for the audience or for my ego?" |

---

### 🔍 Forensic Analysis Protocol (FAP)

**Diagnoses root causes, not just symptoms.**

When a persona needs to investigate failures, unexpected results, or system behavior, it applies a domain-adapted **5W2H forensic framework**:

| Factor | Core Question | Purpose |
|--------|--------------|---------|
| WHO | Who is involved? | Identify actors, systems, dependencies |
| WHAT | What happened? | Describe the symptom or failure precisely |
| WHEN | When did it occur? | Timeline, triggers, frequency, patterns |
| WHERE | Where in the system? | Locate the layer, component, environment |
| WHY | Why did it happen? | Root cause — not the symptom |
| HOW | How did it manifest? | Mechanism, sequence of events |
| HOW MUCH | How much impact? | Severity, blast radius, cost |

Every persona rewrites these questions in domain-specific language. A trading persona's FAP asks about P&L impact, market sessions, and execution failures. A software persona's FAP asks about stack traces, deploy versions, and error rates.

---

### 🔬 Operational Verification (OV)

**Proves execution is correct before declaring work done.**

CoV verifies thinking. OV verifies execution. Both are required.

Before any persona marks a task complete, it must:

1. **Prove it works** — run tests, check logs, demonstrate correctness
2. **Staff-level review** — ask "Would a senior expert in this field approve this?"
3. **Diff check** — demonstrate behavior before vs. after changes
4. **Edge case coverage** — verify the domain-specific boundary conditions

Domain-adapted evidence requirements:

| Domain | OV Evidence |
|--------|-------------|
| Trading | Backtest results, risk metrics, paper-trade confirmation |
| Software | Unit tests pass, integration tests pass, no regressions |
| Game Dev | Playtesting results, performance benchmarks, edge case coverage |
| Content | Audience testing, readability scores, brand consistency |

---

## The Persona Construction Protocol (PCP)

The 8-step process Petra follows when building any new persona:

```
Step 1: Domain Analysis          — Core field, sub-specialization, task analysis, user context
Step 2: Credential Research      — Education, experience, certifications (specific, verifiable)
Step 3: Methodology Design       — Named framework, 4–6 steps, output format
Step 4: Voice Calibration        — Tone attributes, communication style, signature phrases
Step 5: Constraint Definition    — Scope boundaries, quality standards, interaction rules
Step 6: Mandatory Protocol Integration — CoV, FAP, OV (domain-adapted, no exceptions)
Step 7: Deployment Scaffold Generation — All 5 files with correct separation of concerns
Step 8: Assembly & Polish        — Consistency check, practical additions, quick reference
```

---

## Core Design Principles

### 1. Specificity Over Generality
Real experts have names, backgrounds, and scars. Credentials must be specific and verifiable — real schools, real certifications, real years of experience that shape perspective.

### 2. Methodology Is Memory
Every expert has a repeatable framework they always use. Named frameworks create consistency across responses and feel credible. Generic step-by-step instructions do not.

### 3. Voice Is Identity
Tone must match the persona's background. Include specific phrases, pet peeves, and communication quirks. What a persona **never says** is as important as what they say.

### 4. Constraints Create Expertise
Real experts have opinions and limits. Include what the persona refuses to do, what red flags they watch for, and what corners they never cut.

### 5. Verification Is Non-Negotiable
CoV, FAP, and OV are not features — they are the difference between a tool that generates text and a persona that operates like a senior expert.

### 6. Personas Are Deployed, Not Just Written
A persona document alone is not production-ready. It needs a session orchestrator, state tracking, persistent memory, and a self-improvement loop. The 5-file scaffold is the product.

---

## Persona Categories

Personas built with this methodology fall into five archetypes, each with specific adaptations:

| Category | CoV Focus | FAP Focus | OV Focus |
|----------|-----------|-----------|----------|
| **Technical** | Edge cases, null inputs, scale failures | Debugging, system failures, performance degradation | Tests pass, no regressions, benchmarks met |
| **Business / Strategy** | Market assumptions, competitive blind spots, financial projections | Strategy failures, missed KPIs, market shifts | Data validation, model backtesting, stakeholder sign-off |
| **Creative** | Audience fit, originality, brand consistency | Engagement drops, creative blocks, audience misalignment | Audience testing, A/B results, stakeholder review |
| **Analytical / Research** | Methodology flaws, sample bias, confounders | Data anomalies, replication failures, contradictions | Statistical validation, reproducible results |
| **Translation / Bridge** | Semantic drift, lost context, false equivalences | Translation failures, context mismatches | Round-trip validation, side-by-side comparison |

---

## Getting Started

### Deploy Petra in Claude Code

1. Clone this repository into your project root
2. Open Claude Code in the project directory
3. Claude Code automatically reads `CLAUDE.md` on startup
4. Petra adopts her identity from `PERSONA.md` and begins the session

### Request a New Persona

Tell Petra what you need:

```
DOMAIN: [Field/specialty — e.g., "crypto quant trading"]
TASK: [Primary responsibilities — e.g., "design and validate trading strategies"]
USERS: [Who interacts — e.g., "the developer building the system"]
TONE: [Preferred style — e.g., "direct, technical, no hand-holding"]
OUTPUT: [Expected deliverables — e.g., "strategy specs, backtest configs, risk frameworks"]
TECH STACK: [Languages and platforms — e.g., "Python, Freqtrade, Hyperliquid"]
SPECIAL: [Any specific requirements — e.g., "needs a Diagnose mode for live trade post-mortems"]
```

Petra will ask clarifying questions, then deliver all 5 deployment files ready to save directly into a project directory.

> **Note:** You never need to request CoV, FAP, OV, the deployment scaffold, or workflow orchestration rules. They are included automatically in every persona Petra builds.

### Refine an Existing Persona

```
EXISTING PERSONA: [Reference or paste]
CHANGE: [What to modify]
REASON: [Why the change is needed]
FILE: [Which file(s) need updating]
```

---

## CLAUDE.md Design Rules

The `CLAUDE.md` is the session orchestrator — not the persona. It must:

- Open with a one-line project description
- Define the file read protocol (order, purpose, when to update)
- Contain project-level config (tech stack, conventions, testing standards)
- Contain Workflow Orchestration rules (plan mode, subagent strategy, elegance, autonomy levels)
- Contain Task Management lifecycle (plan → verify → track → explain → document → learn)
- Contain Core Principles (simplicity, no laziness, minimal impact)
- Reference all 4 companion files
- Stay under ~150 lines for maintainability

**It must NOT contain:**
- Persona content (that belongs in `PERSONA.md`)
- Task state or memory entries (those belong in `current-task.md` and `memory.md`)
- Lesson entries (those belong in `lessons.md`)

---

## Autonomy Model

Every persona ships with an explicit autonomy table:

| Situation | Action |
|-----------|--------|
| Bug report | Just fix it. No hand-holding. |
| Simple / obvious fix | Fix and explain. No permission needed. |
| Non-trivial change | Plan first. Check in before implementing. |
| Architecture decision | Plan + verify plan with user before building. |
| Unclear requirements | Ask one focused clarifying question. |
| Task going sideways | STOP. Re-plan. Don't push through. |

---

## Self-Improvement Loop

`lessons.md` is not passive documentation — it is an active prevention system.

After any correction from the user, the persona:
1. Records the **mistake** (what went wrong)
2. Records the **correction** (what the right approach was)
3. Writes a **prevention rule** as an imperative directive (`ALWAYS...` / `NEVER...`)
4. Reviews all lessons at the **start of every session**

The goal: mistake rate approaches zero over time, as patterns accumulate into a permanent knowledge base.

---

## Repository Structure

```
persona-architect/
├── CLAUDE.md              ← Petra's session orchestrator
├── PERSONA.md             ← Dr. Petra Vance — the Persona Architect
├── current-task.md        ← Active task template
├── memory.md              ← Long-term knowledge store
├── lessons.md             ← Self-improvement log
└── README.md              ← This document
```

---

## Philosophy

> *"A persona without a methodology is just a costume."*

> *"Specificity is the soul of expertise."*

> *"CoV catches what you missed. FAP finds why you missed it. OV proves you fixed it."*

> *"CLAUDE.md orchestrates. PERSONA.md thinks. current-task.md tracks. memory.md remembers. lessons.md learns."*

> *"Plan before you build. Verify before you ship. Learn from every mistake."*

The Persona Architect methodology was developed from the observation that the gap between a useful AI collaborator and an impressive-sounding but unreliable one is almost entirely architectural — not a question of model capability.

Good architecture forces the right behaviors: verification before delivery, forensic thinking when things go wrong, persistent learning across sessions, and clear separation between who the persona is, what it's working on, and what it knows.

These are not prompting tricks. They are engineering principles applied to persona design.

---

## Contributing

Contributions welcome — especially:

- **New persona examples** across domains not yet covered
- **Domain-adapted CoV question sets** for niche fields
- **Forensic Analysis templates** for specific industries
- **Lessons.md patterns** derived from real deployment experience
- **CLAUDE.md templates** for specific tech stacks or team configurations

Please open an issue before submitting large changes, so we can align on direction.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

Use, adapt, and build on this methodology freely. Attribution appreciated but not required.

---

## About

This methodology was developed through hands-on deployment of AI personas across crypto trading automation, software architecture, game development, e-commerce, and HR platform engineering. It reflects the operational reality of using AI collaborators across multiple concurrent, high-stakes technical projects.

The 5-file scaffold emerged from repeated failure of single-file approaches — monoliths that grew unmanageable, personas that forgot their own history, and experts that couldn't learn from their own mistakes.

**Dr. Petra Vance** is the distillation of everything that worked.
