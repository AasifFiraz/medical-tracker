# SYSTEM.md — MASTER CONTEXT FILE
# Treatment: Tofacitinib (Tofacitinib Citrate) for Alopecia Universalis
# This file lives in Google Drive (_system folder) and is loaded into Claude Project Knowledge.
# Version: update the version number and date every time this file is edited.
# Version: 1.0 | Last updated: [YYYY-MM-DD]

---

## HOW TO USE THIS FILE

This is the single source of truth Claude reads at the start of every session.
After each session, apply the FILE UPDATE SUGGESTIONS Claude outputs — update only
the specific fields listed, then save the file back to Drive.
Re-upload to Claude Project Knowledge when: a new phase starts, a dose changes,
or significant baseline values are first filled in. Otherwise update quarterly.

---

## FILE STRUCTURE MAP
# This section tells Claude exactly where each type of data lives across all files.
# Claude must reference this map when generating FILE UPDATE SUGGESTIONS.

| Data type | File | Section |
|---|---|---|
| Patient status, phase, dose, dates | SYSTEM.md | ## PATIENT SNAPSHOT |
| Permanent baseline lab values | SYSTEM.md | ## BASELINE LAB VALUES |
| Most recent lab values | SYSTEM.md | ## LATEST LAB VALUES |
| SALT score history | SYSTEM.md | ## SALT SCORE LOG |
| Active medications | SYSTEM.md | ## MEDICATION LOG |
| Contraindicated substances | SYSTEM.md | ### Drugs and substances to avoid |
| Vaccination records | SYSTEM.md | ## VACCINATION LOG |
| Side effects experienced | SYSTEM.md | ## KNOWN SIDE EFFECTS |
| Timeline and milestones | SYSTEM.md | ## TIMELINE AND MILESTONES |
| ULN values for threshold calculation | SYSTEM.md | ## HARD STOP THRESHOLDS |
| Monthly summaries and session outputs | Running Record (checkins folder) | Appended monthly |
| Session prompts and starters | PROMPTS.md | Relevant prompt section |

---

## PATIENT SNAPSHOT

| Field | Value |
|---|---|
| Condition | Alopecia Universalis |
| SALT at baseline | 100 |
| Treatment | Tofacitinib citrate 5 mg BID |
| Treatment status | Pre-treatment — awaiting baseline clearance |
| Treatment start date | [YYYY-MM-DD — fill in on Day 1] |
| Current phase | Pre-treatment |
| Current dose | Not started |
| Adjunct therapy | Not started |
| Last SALT score | 100 — baseline (pre-treatment) |
| Last labs date | [YYYY-MM-DD] |
| Next labs due | [YYYY-MM-DD] |
| Next milestone | Baseline lab clearance session |

---

## BASELINE LAB VALUES
# Recorded before treatment started. Permanent reference. Never overwrite these.
# Claude compares every future result against these numbers.
# Status: PENDING — to be filled in from baseline lab upload session.

| Test | Baseline Value | Date | Reference Range |
|---|---|---|---|
| ALC (Absolute Lymphocyte Count) | | | ≥1,500 cells/mm³ |
| ANC (Absolute Neutrophil Count) | | | ≥2,000 cells/mm³ |
| Hemoglobin | | | 13.5–17.5 g/dL |
| Platelets | | | 150–400 ×10³/μL |
| ALT | | | 7–56 U/L |
| AST | | | 10–40 U/L |
| ALP | | | 44–147 U/L |
| Bilirubin (total) | | | 0.1–1.2 mg/dL |
| Creatinine | | | 0.74–1.35 mg/dL |
| eGFR | | | ≥60 mL/min/1.73m² |
| LDL | | | <130 mg/dL |
| HDL | | | >40 mg/dL |
| Total Cholesterol | | | <200 mg/dL |
| Triglycerides | | | <150 mg/dL |
| Fasting Glucose | | | 70–99 mg/dL |
| HbA1c | | | <5.7% |
| CPK (Creatine Kinase) | | | 22–198 U/L |
| Uric Acid | | | 3.4–7.0 mg/dL |
| HBsAg | | | Negative |
| Anti-HBs | | | [result] |
| Anti-HBc | | | Negative |
| HCV Antibody | | | Negative |
| TB Screening (IGRA) | | | Negative |

---

## LATEST LAB VALUES
# Updated after each lab session. Claude populates this from uploaded reports.

| Test | Latest Value | Date | Change from Baseline | Status |
|---|---|---|---|---|
| ALC | | | | Pending baseline |
| ANC | | | | Pending baseline |
| Hemoglobin | | | | Pending baseline |
| ALT | | | | Pending baseline |
| AST | | | | Pending baseline |
| Creatinine | | | | Pending baseline |
| LDL | | | | Pending baseline |
| HDL | | | | Pending baseline |
| Triglycerides | | | | Pending baseline |
| Fasting Glucose | | | | Pending baseline |

---

## HARD STOP THRESHOLDS
# Claude must flag immediately if any result crosses these lines.
# Fill in ULN values from the baseline lab report once received.

| Parameter | Hold | Discontinue / Emergency |
|---|---|---|
| ALC | — | <500 cells/mm³ → discontinue |
| ANC | <1,000 cells/mm³ → hold | <500 cells/mm³ → discontinue |
| Hemoglobin | Drop >2 g/dL from baseline OR absolute <8 g/dL → hold | Confirmed decline |
| ALT / AST | >3× ULN → hold and investigate | >5× ULN confirmed OR any elevation + jaundice → discontinue |
| Creatinine | Rise >50% from baseline → hold and reassess | Confirmed |
| DVT / PE symptoms | Unilateral leg swelling, chest pain, dyspnea, tachycardia → hold immediately | Emergency evaluation |
| Serious infection | Fever >38.5°C + systemic symptoms → hold | — |

ULN values for threshold calculation (fill in from lab report):
- ALT ULN: [X] U/L → 3× = [X] → 5× = [X]
- AST ULN: [X] U/L → 3× = [X] → 5× = [X]

---

## SALT SCORE LOG
# Updated monthly. Claude calculates and records after each SALT session.

| Date | Month on Treatment | SALT Score | % Improvement from Baseline | Notes |
|---|---|---|---|---|
| [YYYY-MM-DD] | Baseline | 100 | 0% | Pre-treatment |
| | Month 1 | | | |
| | Month 3 | | | |
| | Month 6 | | | |
| | Month 9 | | | |
| | Month 12 | | | |

---

## MEDICATION LOG

| Drug | Dose | Frequency | Start Date | Status | Notes |
|---|---|---|---|---|---|
| Tofacitinib citrate | 5 mg | BID | [date] | Pending start | Primary treatment |
| Oral minoxidil | [X] mg | QD | [date] | Not started | Adjunct — to be discussed |

### Drugs and substances to avoid
Claude must flag immediately if any of these appear in uploaded documents.

| Category | Examples | Consequence |
|---|---|---|
| Strong CYP3A4 inhibitors | Ketoconazole, clarithromycin, ritonavir | Doubles tofacitinib exposure → reduce to 5 mg QD |
| Dual CYP3A4 + CYP2C19 inhibitors | Fluconazole | ~80% AUC increase → reduce to 5 mg QD for duration |
| Strong CYP3A4 inducers | Rifampin, carbamazepine, phenytoin, St. John's Wort | 84% AUC reduction → therapeutic failure |
| Strong immunosuppressants | Azathioprine, cyclosporine, biologics | Additive immunosuppression — do not combine |
| Live vaccines | Varicella, MMR, live influenza, yellow fever, oral typhoid | Contraindicated during therapy |
| Grapefruit / grapefruit juice | — | CYP3A4 inhibition — avoid excessive consumption |

---

## VACCINATION LOG

| Vaccine | Dose 1 | Dose 2 | Status | Notes |
|---|---|---|---|---|
| Shingrix (RZV) — recombinant, non-live | [date] | [date / pending] | Pending / In progress / Complete | Dose 2 ideally 2–6 months after dose 1 |
| Influenza (annual, inactivated) | [date] | — | Current / Due | Safe during therapy |
| COVID-19 booster | [date] | — | Current / Due | Safe during therapy |
| Hepatitis B series | [status] | — | Complete / NA | If serology indicated |

Note: All live vaccines are contraindicated during tofacitinib therapy.
Non-live vaccines (inactivated, recombinant, subunit) are safe.

---

## TIMELINE AND MILESTONES

| Milestone | Target Date | Completed | Notes |
|---|---|---|---|
| Baseline labs collected | [date] | [ ] | In progress |
| Baseline clearance session with Claude | [date] | [ ] | Upload all reports when ready |
| Shingrix dose 1 | [date] | [ ] | Ideally before or at treatment start |
| Treatment start (Day 1) | [TBD] | [ ] | Confirmed after baseline clearance |
| First lipid check (4–8 weeks post-start) | [TBD] | [ ] | Mandatory — LDL effect peaks by week 6 |
| Month 1 labs | [TBD] | [ ] | CBC, LFTs, renal panel |
| Month 3 SALT + labs | [TBD] | [ ] | First formal SALT assessment |
| Shingrix dose 2 | [TBD] | [ ] | 2–6 months after dose 1 |
| Month 6 escalation review | [TBD] | [ ] | Escalate if SALT improvement <50% |
| Month 6 full labs | [TBD] | [ ] | All panels |
| Month 12 assessment | [TBD] | [ ] | Full review |
| Annual TB rescreening | [TBD] | [ ] | IGRA |
| Annual skin exam | [TBD] | [ ] | NMSC surveillance |

---

## KNOWN SIDE EFFECTS (PERSONAL LOG)
# Claude populates this when side effects are reported or observed.

| Side Effect | Onset Date | Severity (1–10) | Status | Management |
|---|---|---|---|---|
| None recorded yet | | | | |

---

## PHASE DECISION RULES
# Claude references these when assessing progress and recommending next steps.

| Trigger | Protocol Action |
|---|---|
| Any baseline value outside initiation criteria | Do not start — flag specific value and required resolution |
| SALT improvement <20% at Month 3 | Check adherence and drug interactions. Continue — escalation not yet indicated |
| SALT improvement <50% at Month 6 | Consider escalation to 10 mg BID if labs stable and tolerated |
| SALT ≤10 sustained for 3+ months | Consider consolidation / taper discussion |
| SALT returns to ≥50 after prior response | Treat as relapse — return to last effective dose |
| LDL rise >25% from baseline | Repeat lipid panel in 6 weeks. If >160 mg/dL, apply ASCVD risk assessment |
| Any hard stop threshold crossed | See HARD STOP THRESHOLDS section — act immediately |