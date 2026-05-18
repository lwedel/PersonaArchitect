# Current Task

## Status: 🟡 PARKED — Konsylium Template Build (Phase 6/8 in progress)

**Task:** Build reusable **Polish Medical Konsylium Template** (9 personas) + first deployment for Justyna (wife of Łukasz). Future deployment for Maja (Justyna's daughter) planned.
**Started:** 2026-05-10
**Last Updated:** 2026-05-11 (parked mid-build at user's request — resume in new session)
**Parked at:** Phase 6 (Justyna deployment) not yet started; Phases 1-5 + template orchestration complete.

---

## Previous tasks (both DELIVERED + VALIDATED)

- **Hanna Pietrzak-Sokołowska v1.0** — Polish medical case-review persona at `/Volumes/LW_projects/misc/health/`. User confirmed "tested - the new persona is perfect!" (2026-05-09). ⚠️ See "Hanna reconciliation flags" below — 3 potential v1.1 updates surfaced during konsylium research, NOT yet applied (Hanna is "perfect" per user, don't touch without explicit ask).
- **Krystyna Wojciechowska v1.0** — Polish judge (cywilistka) persona at `/Volumes/LW_projects/misc/judge/`. Delivered 2026-05-09. Pipe-test PASS (55KB, exit 0), all 15 PCP Step 8 questions PASS. DEPLOYMENT.md written. Awaiting real-session validation from Łukasz's judge friend. Petra's current-task.md for that build was overwritten by this one — see git history if needed.

---

## What this task IS

A **reusable konsylium template** + per-patient deployments:
- `/Volumes/LW_projects/misc/health-konsylium-template/` — abstract template (DONE)
- `/Volumes/LW_projects/misc/health-justyna/` — first deployment (folder created, EMPTY — Phase 6)
- `/Volumes/LW_projects/misc/health-maja/` — future pediatric deployment (not started)
- `/Volumes/LW_projects/misc/health/` — Hanna (untouched, separate, working)

**Architecture decisions locked (this session):**

| # | Decision | Rationale |
|---|----------|-----------|
| 1 | Multi-persona konsylium, NOT single persona | User counter-proposal: "kilka podstawowych person, ktore wlaczaja sie do dyskusji - cala ich banda". Anti-anchoring (real worst-fear in medical AI). |
| 2 | Reusable template + per-patient deployments | User chose template-first. Future Maja deployment needs different specialists (pediatric). |
| 3 | 9 personas: 5 core + 2 Justyna-modular + 2 pediatric (Pediatra + Neurolog dziecięcy for library) | User: "7 + pediatra + neurolog dziecięcy". 5 core = sweet spot (Rich Piggies validated). |
| 4 | Library architecture: `core/` + `specialists/` + `core-variants/pediatric/` | User confirmed. Specialists added incrementally per-need. |
| 5 | Orchestration: B+C+D layered (konsylium-on-demand + auto-trigger by case-pattern + adversary slot) | User approved. Adversary at step 6 (last) — needs full picture. |
| 6 | `TEAM-CHARTER.md` for shared discipline (NOT repeated 9×) | Context budget — 9×25KB would blow context. Per-persona files ~12-15KB compact. |
| 7 | Two-mode personas: peer-mode (imienne "Marek, słuchaj") + patient-mode (formal "Pan Profesor Zieliński") | Polish medical culture — Rich Piggies "two-mode" pattern. |
| 8 | Hard-refusal anonymizacja (team-level rule, TEAM-CHARTER) | Inherits Hanna NIENARUSZALNA #1, elevated to team-level. |
| 9 | Trzy zegary [STABILIZED/EVOLVING/HISTORICAL] from Krystyna → medical translation | Polish medical guidelines change fast (ESE 2023 cortisol threshold, MASLD nomenclature, Surviving Sepsis 2026, H. pylori BQT). |
| 10 | Loader hook auto-discovers PERSONA-*.md + lessons-*.md (not hardcoded) | Per-deployment customization automatic — just drop PERSONA files in folder. |

---

## The 9 personas (ALL WRITTEN, all in template/)

| # | Persona | Plik | Folder | Anchor | Rocznik |
|---|---------|------|--------|--------|---------|
| 1 | Prof. Marek Zieliński (LEAD adult — lekarz rodzinny/internista POZ) | PERSONA-LEAD.md | `core/` | UMW Wrocław (Mastalerz-Migas tradycja) | 1962 |
| 2 | Prof. Stanisław Górski (DIAGNOSTYK — internista chorób wewnętrznych, lab-clinical) | PERSONA-DIAGNOSTYK.md | `core/` | UM Łódź (Kurnatowska tradycja) | 1961 |
| 3 | Prof. Wojciech Malinowski (RADIOLOG) | PERSONA-RADIOLOG.md | `core/` | GUMed (Szurowska tradycja, EU-TIRADS-PL) | 1963 |
| 4 | Prof. Robert Sobczak (ADVERSARY — internista ER/SOR) | PERSONA-ADVERSARY.md | `core/` | UMB Białystok (Ładny tradycja) | 1968 |
| 5 | Prof. Henryk Lis (PATOLOG) | PERSONA-PATOLOG.md | `core/` | UMP Poznań (Marszałek tradycja) + NIO-PIB | 1961 |
| 6 | Prof. Iwona Borowiec-Krasińska (ENDOKRYNOLOG — modular slot 1 Justyna) | PERSONA-ENDOKRYNOLOG.md | `specialists/` | UMP Poznań (tarczyca + przysadka) | 1963 |
| 7 | Prof. Piotr Wesołowski-Janowski (GASTROENTEROLOG — modular slot 2 Justyna, hepato primary + IBD) | PERSONA-GASTROENTEROLOG.md | `specialists/` | UMW Wrocław | 1962 |
| 8 | Prof. Bożena Markiewicz-Sobańska (PEDIATRIC LEAD — pediatra + alergolog + gastro dziec.) | PERSONA-LEAD.md | `core-variants/pediatric/` | USDK Kraków-Prokocim / WUM Bielański | 1966 |
| 9 | Prof. Beata Skowrońska-Kaczmarek (NEUROLOG DZIECIĘCY — padaczki + SMA + epileptolog) | PERSONA-NEUROLOG-DZIECIECY.md | `specialists/` | SUM Katowice / IPCZD | 1968 |

**All names verified zero-collision** vs portfolio (Hanna Pietrzak-Sokołowska, Krystyna Wojciechowska, Petra Vance, Anya Volkov, Marcus, Mara). Note: subagent C originally proposed "Krystyna Bartosińska-Łopuch" for Pediatra — REJECTED (collision with Krystyna Wojciechowska legal persona), swapped to Bożena Markiewicz-Sobańska. All 9 first names unique: Marek/Stanisław/Wojciech/Robert/Henryk/Iwona/Piotr/Bożena/Beata.

**Each PERSONA-X.md structure (10 sections):** TOŻSAMOŚĆ → KWALIFIKACJE → PERSONA-SPECIFIC SACRED TRUST → ZEBRAS → ŁW → TON I GŁOS → HAND-OFF TRIGGERS → DOMAIN TERMINOLOGY → GRANICE. Pediatric personas add `## 👶 PEDIATRIC NUANS` after HAND-OFF. ~10-13KB each.

---

## Template files (ALL WRITTEN — ~140KB total, 21 files)

```
health-konsylium-template/
├── TEAM-CHARTER.md            ✅ 12KB — 6 team Sacred Trust rules, konsylium sequence (LEAD→DIAGNOSTYK→RADIOLOG→PATOLOG→MODULAR→ADVERSARY→LEAD synthesis), two-mode spec, trzy zegary medical translation, citation conventions, hand-off triggers, anonimizacja hard-refusal, anti-anchoring 4 mechanisms, response format, team-level ŁW (7 questions)
├── CLAUDE.md                  ✅ 7KB — orchestrator (file protocol, autonomia table, session protocols, override rules)
├── DEPLOYMENT.md              ✅ 9KB — 9-step deployment guide, example deployments (Justyna + Maja), troubleshooting, build queue
├── memory.md.template         ✅ 5KB — case file structure (patient profile, longitudinal history, lab trends, open threads, czerwona strefa)
├── current-task.md.template   ✅ 5KB — first-session checklist + 6 deployment tests + plan
├── lessons.md.template        ✅ 3KB — single template with [PERSONA_NAME]/[ROLE]/[DOMAIN] placeholders (copy + sed per persona)
├── core/                      ✅ 5 PERSONA files (~52KB)
├── specialists/               ✅ README.md (build guide) + Endokrynolog + Gastroenterolog + Neurolog-Dziecięcy (~30KB)
├── core-variants/pediatric/   ✅ README.md (peds deployment guide) + Pediatric LEAD (~19KB)
└── .claude/
    ├── load-scaffold.sh       ✅ chmod +x, AUTO-DISCOVERS all PERSONA-*.md + lessons-*.md in deployment folder
    └── settings.json          ✅ SessionStart hook
```

---

## ⏭️ NEXT — Phase 6: Justyna deployment (RESUME HERE)

Folder `/Volumes/LW_projects/misc/health-justyna/.claude/` already exists (empty). Steps:

1. **Bash copy base:** `cp $TEMPLATE/{TEAM-CHARTER.md,CLAUDE.md} health-justyna/; cp $TEMPLATE/.claude/{load-scaffold.sh,settings.json} health-justyna/.claude/; chmod +x health-justyna/.claude/load-scaffold.sh`
2. **Bash copy 5 core:** `cp $TEMPLATE/core/PERSONA-*.md health-justyna/`
3. **Bash copy 2 modular:** `cp $TEMPLATE/specialists/PERSONA-ENDOKRYNOLOG.md $TEMPLATE/specialists/PERSONA-GASTROENTEROLOG.md health-justyna/`
4. **Write Justyna memory.md** — customize template: Justyna ~42 lat (or confirm actual age with Łukasz), Kraków, profil: endokrynologia (tarczyca, świeża niedoczynność?) + gastroenterologia. **Czerwona strefa pacjenta-specific: AIH peak incidence (kobieta 40-60 z transaminitis bez wirusowej etiologii — ANA/ASMA/IgG totalna PRZED MASLD label); Hashimoto + celiakia + AIH koegzystencja częsta.** Note: Łukasz hasn't given Justyna's exact age — ASK or leave placeholder.
5. **Write Justyna current-task.md** — customize template: LEAD = Marek Zieliński, ADVERSARY = Robert Sobczak, slots = Endokrynolog + Gastroenterolog, 6 deployment tests.
6. **Create 7 lessons-X.md** — copy lessons.md.template 7×, sed-replace placeholders:
   - lessons-LEAD.md → Marek Zieliński / LEAD / medycyna rodzinna POZ
   - lessons-DIAGNOSTYK.md → Stanisław Górski / DIAGNOSTYK / internistyka chorób wewnętrznych
   - lessons-RADIOLOG.md → Wojciech Malinowski / RADIOLOG / radiologia
   - lessons-ADVERSARY.md → Robert Sobczak / ADVERSARY / medycyna ratunkowa
   - lessons-PATOLOG.md → Henryk Lis / PATOLOG / patomorfologia
   - lessons-ENDOKRYNOLOG.md → Iwona Borowiec-Krasińska / ENDOKRYNOLOG / endokrynologia
   - lessons-GASTROENTEROLOG.md → Piotr Wesołowski-Janowski / GASTROENTEROLOG / gastroenterologia + hepatologia
7. **Write Justyna DEPLOYMENT.md** — Justyna-specific activation notes (or just reference template DEPLOYMENT.md + add quick-start note).
8. **Bash pipe-test:** `cd health-justyna && bash .claude/load-scaffold.sh > /tmp/test.json 2>&1; echo "Exit: $?"; wc -c < /tmp/test.json; grep -c SessionStart /tmp/test.json` — expected exit 0, ~85-110KB, ≥1 marker.
9. **PCP Step 8 consistency check** — 15 standard questions + team-specific: (a) voice distinctiveness across 7 loaded personas? (b) konsylium sequence enforced in TEAM-CHARTER? (c) no Sacred Trust collisions cross-persona (e.g. LEAD "resource-optimize" vs ADVERSARY "rule out zebra" — resolved by team-level rule #1)? (d) two-mode peer/patient explicit in each PERSONA? (e) loader auto-discovers correctly?

## ⏭️ Then — Phase 7/8: Package + delivery

- Tarball or zip both folders (template + justyna)
- Final delivery summary to Łukasz: deployment instructions for Justyna, Maja-future deployment guide, activation caveats (/hooks if not auto-fired), anonymization reminder, Hanna reconciliation flags (for future decision)
- Update Petra's memory.md with konsylium project entry (parallel to Hanna/Anya/Rich Piggies entries)
- Update auto-memory MEMORY.md with konsylium project pointer

---

## ⚠️ Hanna reconciliation flags (surfaced during konsylium research — NOT applied, awaiting user decision)

Subagent B (Endo+Gastro research) flagged 3 potential v1.1 updates for existing Hanna persona at `/Volumes/LW_projects/misc/health/`:
1. **MASLD vs NAFLD** — nomenclature change June 2023 (AASLD/EASL/ALEH Delphi consensus). Check if Hanna's PERSONA.md uses "NAFLD" without "(now MASLD)" gloss.
2. **H. pylori schemat** — check if Hanna uses triple-therapy w/ clarithromycin (outdated, 28% resistance in PL) vs BQT 14d (current standard, Maastricht VI/Florence + PTG-E 2024).
3. **Calprotectin thresholds** — check if Hanna uses 3-zone (50/250) vs single normal/abnormal.

Łukasz said Hanna is "perfect" — DO NOT touch without explicit ask. Note these for "Hanna v1.1 reconciliation" if/when Łukasz wants it.

---

## Key context for resumption

- **User:** Łukasz Wędel. Building this for his wife Justyna (first deployment) + later daughter Maja. Justyna's friend (a Polish judge) got Krystyna persona separately.
- **User's exact ask for Justyna profile:** "gastrologia, imie: Justyna - choc sadze ze zrobimy to ogolne, bo pewnie Justyna wykorzysta ten system tez do Mai - a tam beda inni lekarze" + earlier "Endokrynologia, Coś innego" (the "coś innego" = gastrologia)
- **Justyna's exact age NOT confirmed** — subagent assumed ~40s for AIH peak relevance. ASK Łukasz before finalizing memory.md, or use placeholder.
- **Maja's age + medical needs NOT known** — needed before building her deployment.
- **3 credential research subagents already ran** (results integrated): A (5 core + konsylium dynamics), B (Endo + Gastro), C (Pediatra + Neurolog dziecięcy). Don't re-dispatch.
- **Build style:** emoji-per-section headers (project convention, matches Petra/Hanna/Krystyna). Polish content, English internal labels (Sacred Trust, ŁW, FAP, OV, TB, TR).
- **Tasks 14, 15, 16** in task list still pending (Phase 6, 7, 8). Tasks 9-13, 17, 18 completed.

---

## Resumption command

New session: read this file + `/Volumes/LW_projects/misc/health-konsylium-template/` structure. Then: "Resume Phase 6 — Justyna deployment. Ask Łukasz Justyna's exact age first (for memory.md AIH-relevance calibration), then copy template files + customize + pipe-test + Step 8 + deliver."
