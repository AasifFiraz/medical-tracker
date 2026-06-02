# SYSTEM.md — MASTER CONTEXT FILE
# Treatment: Tofacitinib (Tofacitinib Citrate) for Alopecia Universalis
# This file lives in Google Drive (_system folder) and is loaded into Claude Project Knowledge.
# Version: update the version number and date every time this file is edited.
# Version: 1.1 | Last updated: 2026-04-24

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
| Treatment status | Active — Day 1 commences 2026-04-25 |
| Treatment start date | 2026-04-25 |
| Current phase | Phase 1 — Initiation |
| Current dose | 5 mg BID |
| Adjunct therapy | Rosuvastatin 5 mg QD + Ezetimibe 10 mg QD (lipid management, started 2026-04-22) |
| Last SALT score | 100 — baseline (pre-treatment) |
| Last labs date | 2026-04-21 |
| Next labs due | 2026-05-25 (Month 1 — CBC, LFTs, renal, CPK) |
| Next milestone | 4–8 week lipid recheck: 2026-06-06 to 2026-06-20 |

---

## BASELINE LAB VALUES
# Recorded before treatment started. Permanent reference. Never overwrite these.
# Claude compares every future result against these numbers.
# Collected: 2026-04-21 | Lab: Forte Diagnostics | Sample ID: 01183013

| Test | Baseline Value | Date | Reference Range |
|---|---|---|---|
| ALC (Absolute Lymphocyte Count) | 2,340 cells/mm³ | 2026-04-21 | ≥1,500 cells/mm³ |
| ANC (Absolute Neutrophil Count) | 3,350 cells/mm³ | 2026-04-21 | ≥2,000 cells/mm³ |
| Hemoglobin | 16.5 g/dL | 2026-04-21 | 13.0–17.0 g/dL |
| Platelets | 225 ×10³/µL | 2026-04-21 | 150–410 ×10³/µL |
| ALT (SGPT) | 12.0 U/L | 2026-04-21 | Up to 41 U/L |
| AST (SGOT) | 17.0 U/L | 2026-04-21 | 15–37 U/L |
| ALP | 83.0 U/L | 2026-04-21 | 40–129 U/L |
| GGT | 37.0 U/L | 2026-04-21 | 15–85 U/L |
| Bilirubin (total) | 1.30 mg/dL | 2026-04-21 | Up to 1.2 — NOTE: personal baseline; transaminases normal; likely Gilbert's syndrome |
| Bilirubin (direct) | 0.50 mg/dL | 2026-04-21 | ≤0.2 — elevated in context of Gilbert's; transaminases normal |
| Creatinine | 1.27 mg/dL | 2026-04-21 | Lab: 0.67–1.17; Protocol: 0.74–1.35 — PERSONAL BASELINE; monitoring threshold >1.905 mg/dL |
| eGFR | Not reported | 2026-04-21 | ≥60 mL/min/1.73m² |
| Urea | 28.0 mg/dL | 2026-04-21 | 15–53 mg/dL |
| Uric Acid | 4.2 mg/dL | 2026-04-21 | 3.5–7.2 mg/dL |
| LDL | 239.8 mg/dL | 2026-04-21 | <130 mg/dL — PRE-STATIN BASELINE; management plan in place |
| HDL | 58 mg/dL | 2026-04-21 | >40 mg/dL |
| Total Cholesterol | 325.0 mg/dL | 2026-04-21 | <200 mg/dL — PRE-STATIN BASELINE |
| Triglycerides | 136 mg/dL | 2026-04-21 | <150 mg/dL |
| VLDL | 27.2 mg/dL | 2026-04-21 | 10–30 mg/dL |
| TC/HDL Ratio | 5.6 | 2026-04-21 | 2.5–4.5 |
| Fasting Glucose | 77 mg/dL | 2026-04-21 | 70–109 mg/dL |
| HbA1c | 5.1% | 2026-04-21 | Normal <5.7% |
| TSH | 1.019 mIU/mL | 2026-04-21 | 0.35–5.1 mIU/mL |
| CPK (Creatine Kinase) | NOT COLLECTED | — | 22–198 U/L — obtain at Month 1 draw |
| HBsAg | Negative | 2026-04-21 | Negative |
| Anti-HBs (HBsAb) | 8.25 (Non-reactive) | 2026-04-21 | Non-reactive <10 — no protective immunity; HBV vaccination recommended |
| Anti-HBc Total | 0.2 (Negative) | 2026-04-21 | Negative <0.7 — no past HBV exposure |
| HCV Antibody | <1.0 Index (Non-reactive) | 2026-04-21 | Negative |
| HIV I & II | Negative | 2026-04-21 | Negative |
| TB Screening (IGRA) | Negative | 2026-04-24 | Negative |
| CRP | 6.0 mg/L | 2026-04-21 | 0–10 mg/L |
| ESR | 10 mm/hr | 2026-04-21 | 2–20 mm/hr |

**Pre-existing variants at baseline — not adverse effects, do not flag as new findings:**
- **Bilirubin elevated** (Total 1.30, Direct 0.50) with entirely normal transaminases (ALT 12, AST 17, ALP 83, GGT 37) — pattern consistent with Gilbert's syndrome; benign; established as personal baseline
- **Creatinine 1.27 mg/dL** — above Forte lab range but within protocol-acceptable range (0.74–1.35); personal baseline locked; monitoring trigger is >1.905 mg/dL (>50% rise)
- **Low MCV (79.6 fL) + elevated RBC (5.7 ×10⁶/µL) + normal RDW (12.3%)** — classic thalassemia trait pattern; hemoglobin normal at 16.5 g/dL; not a treatment concern
- **MCHC 36.3 g/dL** — marginally above range; consistent with thalassemia trait pattern; not clinically significant
- **Albumin 5.1 g/dL** — marginally above lab range; not clinically significant
- **Anti-HBs 8.25** — non-reactive; susceptible to HBV; Hepatitis B vaccination series recommended before or during early treatment
- **Prior history of muscle discomfort on statins** — informed selection of rosuvastatin (hydrophilic, lower myopathy risk, no CYP3A4 overlap with tofacitinib) over alternatives
- **CPK not collected at baseline** — add to Month 1 draw (2026-05-25)

---

## LATEST LAB VALUES
# Updated after each lab session. Claude populates this from uploaded reports.

| Test | Latest Value | Date | Change from Baseline | Status |
|---|---|---|---|---|
| ALC | 2,340 cells/mm³ | 2026-04-21 | Baseline | ✅ Clear |
| ANC | 3,350 cells/mm³ | 2026-04-21 | Baseline | ✅ Clear |
| Hemoglobin | 16.5 g/dL | 2026-04-21 | Baseline | ✅ Clear |
| ALT | 12.0 U/L | 2026-04-21 | Baseline | ✅ Clear |
| AST | 17.0 U/L | 2026-04-21 | Baseline | ✅ Clear |
| Creatinine | 1.27 mg/dL | 2026-04-21 | Baseline | ✅ Personal baseline set |
| LDL | 239.8 mg/dL | 2026-04-21 | Baseline (pre-statin) | ⚠️ Management plan active |
| HDL | 58 mg/dL | 2026-04-21 | Baseline | ✅ Clear |
| Triglycerides | 136 mg/dL | 2026-04-21 | Baseline | ✅ Clear |
| Fasting Glucose | 77 mg/dL | 2026-04-21 | Baseline | ✅ Clear |
| CPK | Not collected | — | — | ⚠️ Pending — Month 1 draw |

---

## HARD STOP THRESHOLDS
# Claude must flag immediately if any result crosses these lines.

| Parameter | Hold | Discontinue / Emergency |
|---|---|---|
| ALC | — | <500 cells/mm³ → discontinue |
| ANC | <1,000 cells/mm³ → hold | <500 cells/mm³ → discontinue |
| Hemoglobin | Drop >2 g/dL from baseline (i.e., <14.5) OR absolute <8 g/dL → hold | Confirmed decline |
| ALT / AST | >3× ULN → hold and investigate | >5× ULN confirmed OR any elevation + jaundice → discontinue |
| Creatinine | Rise >50% from personal baseline (i.e., >1.905 mg/dL) → hold and reassess | Confirmed |
| LDL | Rise >25% from pre-statin baseline OR >160 mg/dL → reassess statin plan | — |
| DVT / PE symptoms | Unilateral leg swelling, chest pain, dyspnea, tachycardia → hold immediately | Emergency evaluation |
| Serious infection | Fever >38.5°C + systemic symptoms → hold | — |
| Herpes zoster prodrome | Unilateral dermatomal burning / tingling / pain → hold tofacitinib; start valacyclovir 1000 mg TID | Treat within 72 hrs of rash onset |

**ULN values for threshold calculation (Forte Diagnostics):**
- ALT ULN: 41 U/L → 3× = 123 U/L → 5× = 205 U/L
- AST ULN: 37 U/L → 3× = 111 U/L → 5× = 185 U/L

---

## SALT SCORE LOG
# Updated monthly. Claude calculates and records after each SALT session.

| Date | Month on Treatment | SALT Score | % Improvement from Baseline | Notes |
|---|---|---|---|---|
| 2026-04-25 | Baseline | 100 | 0% | Pre-treatment — Day 1 |
| | Month 1 | | | |
| | Month 3 | | | |
| | Month 6 | | | |
| | Month 9 | | | |
| | Month 12 | | | |

---

## MEDICATION LOG

| Drug | Dose | Frequency | Start Date | Status | Notes |
|---|---|---|---|---|---|
| Tofacitinib citrate | 5 mg | BID | 2026-04-25 | Active — Day 1 | Primary treatment |
| Rosuvastatin (Sun Pharmaceutical) | 5 mg | QD | 2026-04-22 | Active | Lipid management; hydrophilic — lower myopathy risk; no CYP3A4 overlap with tofacitinib |
| Ezetimibe / MIBE 10 (ATOZ Pharmaceuticals) | 10 mg | QD | 2026-04-22 | Active | Combination with rosuvastatin; chosen given prior statin intolerance and degree of LDL elevation |
| Oral minoxidil | [X] mg | QD | [date] | Not started | Adjunct — to be discussed at Month 3 or Month 6 review |

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
| Shingrix (RZV) — recombinant, non-live | N/A | N/A | Unavailable in Sri Lanka | Zoster risk managed via prodrome education and valacyclovir access — see plan below |
| Hepatitis B series — 3 dose | Pending | Pending | Not started — recommended before or during early treatment | Anti-HBs 8.25 non-reactive; no protective immunity; Dose 2 at 1 month; Dose 3 at 6 months; check Anti-HBs 4–8 weeks post-series |
| MMR | Unknown | — | Verify vaccination records | Live vaccine — must be given ≥2 weeks before Day 1 if due; contraindicated once treatment starts |
| Varicella | Unknown | — | Verify vaccination records or confirm prior infection | Live vaccine — same restriction as MMR |
| Influenza (annual, inactivated) | Pending | — | Due next flu season | Safe during therapy — inactivated formulation only; NOT live nasal spray |
| COVID-19 booster | Pending | — | Per national schedule | Safe during therapy |

**Zoster management plan (replacing unavailable Shingrix):**
- Patient educated on prodrome: unilateral dermatomal burning / tingling / pain typically 2–4 days before skin changes — act at this stage, do not wait for rash
- **Treatment dose if episode occurs: Valacyclovir 1000 mg TID × 7 days** — must begin within 72 hours of rash onset
- Do NOT confuse with prophylactic dose (500 mg QD ongoing) — these are different regimens
- **Tofacitinib action:** Hold from prodrome recognition; resume only after all lesions fully crusted AND 7-day valacyclovir course complete (typically 10–14 days total hold)
- Valacyclovir 1000 mg tablet access confirmed locally before Day 1 — do not wait until an episode to arrange this
- Low-dose prophylaxis (valacyclovir 500 mg QD ongoing) is a separate clinical option — discuss with treating doctor

---

## TIMELINE AND MILESTONES

| Milestone | Target Date | Completed | Notes |
|---|---|---|---|
| Baseline labs collected | 2026-04-21 | [x] | Forte Diagnostics — all panels complete |
| IGRA result confirmed negative | 2026-04-24 | [x] | Final mandatory clearance test |
| Baseline clearance session with Claude | 2026-04-24 | [x] | All mandatory prerequisites satisfied |
| **Treatment start (Day 1)** | **2026-04-25** | **[ ]** | **Tofacitinib 5 mg BID commences** |
| Valacyclovir 1000 mg access confirmed locally | Before Day 1 | [ ] | Essential given Shingrix unavailability |
| MMR / Varicella vaccination status verified | Before Day 1 | [ ] | Check records; administer if due — live vaccines contraindicated after Day 1 |
| Hepatitis B Dose 1 | Before or near Day 1 | [ ] | Immune response better before immunosuppression |
| CPK baseline draw | 2026-05-25 | [ ] | Add to Month 1 blood draw |
| Month 1 labs (CBC, LFTs, renal + CPK) | 2026-05-25 | [ ] | First on-treatment safety check |
| **4–8 week lipid recheck** | **2026-06-06 to 2026-06-20** | **[ ]** | **Mandatory — captures tofacitinib LDL peak effect + ~6 weeks statin effect** |
| Hepatitis B Dose 2 | ~2026-05-25 | [ ] | 1 month after Dose 1 |
| Month 3 labs + first formal SALT score | 2026-07-25 | [ ] | Key efficacy checkpoint |
| Hepatitis B Dose 3 | ~2026-10-25 | [ ] | 6 months after Dose 1 |
| Post-HBV series Anti-HBs check | ~2026-12-25 | [ ] | 4–8 weeks after Dose 3 — confirm seroconversion |
| Month 6 escalation review | 2026-10-25 | [ ] | Escalate to 10 mg BID if SALT improvement <50% and labs stable |
| Month 6 full labs | 2026-10-25 | [ ] | All panels |
| Month 12 full assessment | 2027-04-25 | [ ] | Full labs + SALT + clinical review |
| Annual TB rescreening (IGRA) | 2027-04-25 | [ ] | 12 months from baseline |
| Annual skin exam | 2027-04-25 | [ ] | NMSC surveillance — full body dermatology exam |
| Influenza vaccine (inactivated) | Next flu season | [ ] | Annually while on treatment |

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
| LDL rise >25% from pre-statin baseline OR >160 mg/dL | Reassess statin plan; repeat lipid panel in 6 weeks |
| Herpes zoster prodrome (unilateral dermatomal pain/tingling) | Hold tofacitinib; start valacyclovir 1000 mg TID immediately; do not wait for rash |
| Any hard stop threshold crossed | See HARD STOP THRESHOLDS section — act immediately |