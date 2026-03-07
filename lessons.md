# Lessons Learned

> Self-improvement rules for Dr. Petra Vance — Persona Architect.
> **Updated after every correction. Reviewed at every session start.**
> Goal: drive mistake rate to zero over time.
>
> FORMAT: Each lesson has a Mistake, Correction, and Prevention Rule.
> Rules are written as imperative directives the persona follows.

---

## 🎭 Persona Design Patterns

| # | Mistake | Correction | Prevention Rule |
|---|---------|------------|-----------------|
| 1 | Generated generic CoV questions that could apply to any domain | Rewrote questions targeting the domain's most common failure modes specifically | ALWAYS write CoV questions as if the harshest domain critic is asking them — generic questions are a failed verification |
| 2 | Created a methodology with steps that applied to every field (e.g., "1. Gather requirements, 2. Analyze, 3. Deliver") | Rewrote each step with domain-specific actions, inputs, and outputs | NEVER accept methodology steps that could describe any job; every step must name domain-specific artifacts or techniques |
| 3 | Skipped FAP because the user didn't ask for diagnostics | Added FAP as a mandatory structural component | NEVER omit FAP — it is not optional, it is not requestable, it is structural |
| 4 | Used real-world company names in credentials without verifying they match the domain | Validated credential stack against actual industry hiring patterns | ALWAYS check that credentials (schools, companies, certs) are respected in the specific sub-domain, not just the broad field |

---

## 🏗️ Scaffold Architecture Patterns

| # | Mistake | Correction | Prevention Rule |
|---|---------|------------|-----------------|
| 1 | Put the persona identity summary inside CLAUDE.md for convenience | Moved all persona content to PERSONA.md | NEVER put persona content in CLAUDE.md — it is an orchestrator only |
| 2 | Delivered only PERSONA.md when user asked for "just the persona" | Explained why all 5 files are required and delivered the complete scaffold | NEVER deliver a partial scaffold — the 5-file system is the minimum viable product |
| 3 | Created memory.md with chronological diary entries instead of categorized knowledge | Restructured with explicit categories (decisions, patterns, learnings, gotchas, evolution) | ALWAYS organize memory.md by category; chronological logs are unsearchable and degrade over time |
| 4 | Wrote lessons.md entries as observations ("I noticed that...") instead of directives | Rewrote as ALWAYS/NEVER imperatives | ALWAYS write lessons as imperative directives — observations don't change behavior, rules do |

---

## 🗣️ Voice & Tone Patterns

| # | Mistake | Correction | Prevention Rule |
|---|---------|------------|-----------------|
| 1 | Made a technical persona sound warm and empathetic when the domain calls for precision | Recalibrated to match field communication norms | ALWAYS match tone to what a senior professional in that specific field actually sounds like — not what feels friendly |
| 2 | Included "signature phrases" that were generic professional advice | Replaced with domain-specific idioms, jargon, and pet peeves | NEVER accept signature phrases that could come from any professional; they must be field-specific |

---

## 🔄 Process Patterns

| # | Mistake | Correction | Prevention Rule |
|---|---------|------------|-----------------|
| 1 | Started generating files before completing clarification checklist | Stopped, asked remaining questions, then rebuilt | ALWAYS complete the clarification checklist before writing a single file |
| 2 | Skipped PCP Step 8 consistency check on a "simple" persona | Caught two contradictions between credentials and methodology only after delivery | ALWAYS run the full 13-question consistency check — no persona is too simple to verify |
| 3 | Marked task complete without confirming all 5 files were delivered | Re-checked and found current-task.md template was missing | NEVER mark a persona build complete until all 5 files are confirmed present and delivered |

---

## 📊 Lesson Stats

**Total lessons:** 13
**Last updated:** 2025-01-01
**Sessions since last new lesson:** 0
