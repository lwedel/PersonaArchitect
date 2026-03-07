# Contributing to PersonaArchitect

Thanks for your interest in contributing. This is a methodology repository — contributions that strengthen the framework, add real-world examples, or improve the deployment scaffold are all welcome.

---

## What We're Looking For

### High-Value Contributions

| Type | Examples |
|------|---------|
| **New persona examples** | A complete 5-file scaffold for a domain not yet covered (e.g., cybersecurity, UX research, supply chain) |
| **Domain CoV question sets** | 5 domain-specific Chain of Verification questions for a niche field, with rationale |
| **Forensic Analysis templates** | Domain-adapted 5W2H tables for industries not in the main methodology |
| **Lessons.md patterns** | Real ALWAYS/NEVER rules derived from actual deployment experience |
| **CLAUDE.md templates** | Tech-stack-specific orchestrators (e.g., optimized for Rust projects, data science pipelines, mobile dev) |
| **Methodology improvements** | Identified gaps in PCP steps, new Edge cases in the scaffold design |

### Lower Priority (but still welcome)
- Typo and grammar fixes
- Formatting improvements
- Badge additions

---

## Before You Start

**Open an issue first for anything substantial.**

If you're planning to add a new persona example or propose a methodology change, open an issue to align on direction before writing code. This saves everyone time.

For small fixes (typos, broken links, formatting), go ahead and submit a PR directly.

---

## Standards for Persona Contributions

If you're contributing a persona example, it must meet the full methodology standard:

### Required
- [ ] All 5 files present: `CLAUDE.md`, `PERSONA.md`, `current-task.md`, `memory.md`, `lessons.md`
- [ ] `CLAUDE.md` is lean (under 150 lines) and free of persona content
- [ ] `PERSONA.md` includes named methodology with domain-specific steps
- [ ] CoV protocol present with domain-specific challenge questions (not generic)
- [ ] FAP present with domain-adapted 5W2H table
- [ ] OV present with domain-specific evidence requirements
- [ ] Credentials are specific (real schools, real certifications, realistic years)
- [ ] Voice matches the domain's professional communication norms
- [ ] `memory.md` has categorized entries (not chronological diary)
- [ ] `lessons.md` entries written as ALWAYS/NEVER directives

### Disqualifying Issues
- Generic CoV questions that could apply to any domain
- Methodology steps that don't reference domain-specific artifacts
- CLAUDE.md containing persona content
- Fewer than 5 files

---

## Contribution Process

1. **Fork** the repository
2. **Create a branch** with a descriptive name (`feat/cybersecurity-persona`, `fix/cov-trading-questions`)
3. **Make your changes**
4. **Test your persona** — if contributing a persona, deploy it in Claude Code and run at least one session
5. **Submit a PR** with a clear description of what you added and why

---

## PR Description Template

```
## What this adds / fixes
[One paragraph description]

## Persona domain (if applicable)
[e.g., "Cybersecurity Red Team Analyst"]

## Files changed
- [ ] CLAUDE.md
- [ ] PERSONA.md
- [ ] current-task.md
- [ ] memory.md
- [ ] lessons.md

## Tested in Claude Code?
Yes / No — [brief note on what you tested]

## Methodology compliance check
- [ ] All 5 files present
- [ ] CoV is domain-specific
- [ ] FAP is domain-adapted
- [ ] OV has domain-specific evidence
- [ ] CLAUDE.md is free of persona content
```

---

## Questions?

Open an issue with the `question` label. No question is too basic — the methodology has nuance and we'd rather explain it than have people guess.
