# Project Memory

> **Scope:** Long-term knowledge for the PersonaArchitect project — architecture decisions, persona-design patterns, domain learnings, and gotchas discovered while building Petra herself.
> **NOT for:** in-flight task state (use `current-task.md`), self-improvement rules (use `lessons.md`), or facts derivable from `PERSONA.md` / `CLAUDE.md` / git history.
> **Append-only — never delete entries.** Organized by category. Each entry includes a date.
> **Last reviewed:** 2026-04-25

---

## 🏗️ Architecture Decisions

| Date | Decision | Rationale |
|------|----------|-----------|
| 2025-01-01 | Adopted 5-file scaffold as the standard deployment unit | Single-file monoliths grow unmanageable; separation of concerns enables independent versioning and focused context per session |
| 2025-01-01 | Made CoV, FAP, and OV mandatory (non-requestable) | Optional verification is skipped verification; these protocols must be structural, not decorative |
| 2025-01-01 | CLAUDE.md capped at ~150 lines | Lean orchestrators load faster and stay maintainable; persona depth belongs in PERSONA.md |
| 2025-01-01 | lessons.md added as the 5th file | memory.md is passive knowledge; lessons.md is active prevention — different jobs, different files |
| 2025-01-01 | Autonomy Levels table added to CLAUDE.md template | Explicit autonomy rules reduce friction and clarify when to act vs. when to check in |

---

## 🔍 Persona Design Patterns

| Date | Pattern | Context |
|------|---------|---------|
| 2025-01-01 | Named proprietary methodologies outperform generic step lists | "The Signal-to-Settlement Protocol" feels expert; "Step 1: Analyze data" does not |
| 2025-01-01 | CoV challenge questions must target the domain's harshest critic | Generic self-check questions ("Did I answer the question?") add no value |
| 2025-01-01 | Voice mismatches destroy credibility faster than missing credentials | A quant who sounds like a life coach breaks the illusion immediately |
| 2025-01-01 | FAP should activate automatically on any failure/anomaly report | Personas that wait to be asked for root cause analysis miss their highest-value use case |
| 2026-04-25 | Founder-as-costly-signal for B2B personas (Sutherland insight) | For B2B SaaS marketing personas, the founder's identity IS the marketing — competitors literally cannot fake a real practitioner with skin in the game. Klaudia (HR-AI) and Łukasz-CEO (cocoo) aren't "doing content marketing" — they ARE the costly signal that buyers can't replicate. This shifts persona design for any B2B-product persona: the persona's job is to amplify founder presence, not substitute for it. Sourced from Sutherland's "nobody got fired for buying IBM" framing applied to B2B risk-aversion logic. |
| 2026-04-25 | External-thinker integration as methodology lens (NOT credential decoration, NOT parallel mode) | When a user wants to merge an external thinker's worldview (Sutherland, Kahneman, anyone) into a persona, naive merges create incoherence — especially when the thinker pushes against existing persona discipline. Pattern that works: (1) delegate proper research to subagent BEFORE designing the integration; (2) integrate at structural points (credentials + ONE trait reframe + ONE CoV question + ONE methodology hook + voice patterns); (3) ALWAYS add a Guardrail in the most-affected trait — "X is the corrective lens, not the operating system"; (4) ALWAYS add an explicit "Where this lens is misapplied" section to prevent long-term drift; (5) ALWAYS add a Deployment Success Test specifically targeting the new lens (verifies additive, not replacing). The Mara/Sutherland integration is the canonical reference example — see `j-agent/personas/mara/PERSONA.md` commit `072f3d15`. |

---

## 📚 Domain Learnings

| Date | Learning | Source |
|------|----------|--------|
| 2025-01-01 | Trading personas need explicit signal vs. execution failure distinction in FAP | Discovered during Kai Renner v1 build — mixing these obscures root cause |
| 2025-01-01 | Claude Projects consolidate PERSONA.md and CLAUDE.md into one instructions file | Platform constraint, not a design choice — document as known tradeoff |
| 2025-01-01 | lessons.md rules must be imperative directives, not observations | "I noticed X" doesn't change behavior; "ALWAYS do Y" does |

---

## ⚠️ Gotchas & Pitfalls

| Date | Gotcha | Resolution |
|------|--------|------------|
| 2025-01-01 | CLAUDE.md that contains persona content causes context bleed | Strict rule: CLAUDE.md orchestrates only — persona content always goes in PERSONA.md |
| 2025-01-01 | Memory.md organized chronologically becomes unsearchable | Always organize by category, not by date — dates are metadata, not structure |
| 2025-01-01 | Personas without specific credentials default to generic assistant behavior | Specificity (real schools, real certs, real years) is the forcing function for expert-level output |

---

## 📈 Project Evolution

| Date | Milestone | Notes |
|------|-----------|-------|
| 2025-01-01 | v1: 3-file scaffold (CLAUDE.md, PERSONA.md, current-task.md) | Original architecture — no persistent memory, no self-improvement |
| 2025-01-01 | v2: 4-file scaffold — memory.md added | Enabled knowledge persistence across sessions |
| 2025-01-01 | v3: 5-file scaffold — lessons.md added | Added self-improvement loop; memory.md for knowledge, lessons.md for prevention rules |
| 2025-01-01 | v3.1: Mandatory CoV, FAP, OV — no exceptions | Moved from "recommended" to "structural requirement" after seeing consistent omissions |
| 2025-01-01 | v3.2: Workflow Orchestration added to CLAUDE.md template | Plan mode, subagent strategy, autonomy levels, demand-elegance rule |
| 2026-04-25 | v3.3: Karpathy audit + Alex field report + J directive integration | Largest single methodology update. Inputs: (a) Karpathy's 4 principles applied to Petra's own approach — surfaced 4 violations, locked 4 rule changes (Minimum Viable Brief input gate, one-file-diff refinement default, Deployment Success Tests mandatory, alternatives-stated-explicitly); (b) Alex's 11-week multi-persona deployment report — adopted Last Reviewed header convention + explicit memory scope rule; (c) J's 11-week soul-evolution directive — added Sacred Trust as mandatory PERSONA.md section, Trait Grounding rule (PCP 4.4), Soul vs Method tagging (PCP 4.5), Identity Growth lessons category, COMMUNICATION CONTRACT + USER WORLDVIEW Optional Enrichment fields. Deferred to a separate conversation: tiered scaffold (rejected — full scaffold is the day-zero gain), R6 Relationship-Rich Personas template category. J's directive saved verbatim as `references/J-persona-design-principles.md`. |
| 2026-04-25 | v3.3 first real deployment test: Mara v2 build (j-agent repo) | Reseed of an existing pre-v3.3 persona (Mara, growth marketing strategist for HR-AI.pl + cocoo.tech + whale.academy) under v3.3 + J↔Mara outcome-request protocol + Rory Sutherland integration as methodology lens. Largest single test of v3.3 in practice. **Validated**: alternatives-stated-explicitly accelerates iteration cycles (user could redirect with single-letter responses); cascade-flag prevents silent scope creep (Test 4 was the cleanest case); Sacred Trust as separate structural concept earns its weight; Guardrail-as-structural-concept enabled clean Sutherland integration without dissolving Mara's evidence discipline. **Still untested**: methodology on cold-start (no existing bones to reseed); Mara's actual live behavior on first request (CoV Q7 generative-not-gating discipline risk). Committed to j-agent `master` as `072f3d15`. |
