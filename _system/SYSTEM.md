# SYSTEM.md — MASTER CONTEXT FILE
# Treatment: Tofacitinib (Tofacitinib Citrate) for Alopecia Universalis
# This file lives in Google Drive (_system folder) and is loaded into Claude Project Knowledge.
# Version: update the version number and date every time this file is edited.
# Version: 1.3 | Last updated: 2026-06-02

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
| Treatment status | Active — Day 38 as of 2026-06-02 |
| Treatment start date | 2026-04-25 |
| Current phase | Phase 1 — Initiation |
| Current dose | 5 mg BID |
| Adjunct therapy | Rosuvastatin 5 mg QD + Ezetimibe 10 mg QD (lipid management, started 2026-04-22) — confirmed continue |
| Last SALT score | 100 — estimated Day 38 (no terminal regrowth expected; functional baseline photo set taken 2026-06-02) |
| Last labs date | 2026-06-02 (Day 38 — Forte Diagnostics, Sample ID: 01183588) |
| Next labs due | 2026-07-25 (Month 3 — CBC, LFTs, renal, lipids, CPK — flag CPK explicitly on requisition) |
| Next milestone | Month 3 labs + first formal SALT score: 2026-07-25 |

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
| CPK (Creatine Kinase) | NOT COLLECTED | — | 22–198 U/L — obtain at Month 3 draw (2026-07-25); missed at both baseline and Day 38 |
| HBsAg | Negative | 2026-04-21 | Negative |
| Anti-HBs (HBsAb) | 8.25 (Non-reactive) | 2026-04-21 | Non-reactive <10 — no protective immunity; HBV vaccination series recommended |
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
- **Anti-HBs 8.25** — non-reactive; susceptible to HBV; Hepatitis B vaccination series recommended; HBV Dose 1 is overdue as of Day 38 — initiate immediately
- **Prior history of muscle discomfort on statins** — informed selection of rosuvastatin (hydrophilic, lower myopathy risk, no CYP3A4 overlap with tofacitinib) over alternatives
- **CPK not collected at baseline or Month 1** — explicitly request on Month 3 draw (2026-07-25)
- **Lipid baseline (LDL 239.8, TC 325 at age 22)** — magnitude suggests possible familial hypercholesterolemia; rosuvastatin + ezetimibe are likely long-term therapy independent of tofacitinib; FH workup / family lipid history discussion recommended with treating physician

---

## LATEST LAB VALUES
# Updated after each lab session. Claude populates this from uploaded reports.
# Last updated: 2026-06-02 (Day 38)

| Test | Latest Value | Date | Change from Baseline | Status |
|---|---|---|---|---|
| ALC | 2,190 cells/mm³ | 2026-06-02 | −150 from baseline | ✅ Clear |
| ANC | 3,350 cells/mm³ | 2026-06-02 | Unchanged | ✅ Clear |
| Hemoglobin | 15.6 g/dL | 2026-06-02 | −0.9 from baseline | ✅ Clear |
| Platelets | 209 ×10³/µL | 2026-06-02 | −16 from baseline | ✅ Clear |
| ALT | 18.0 U/L | 2026-06-02 | +6.0 from baseline | ✅ Within range |
| AST | 23.0 U/L | 2026-06-02 | +6.0 from baseline | ✅ Within range |
| ALP | 116.0 U/L | 2026-06-02 | +33 from baseline (+39%) | ⚠️ In range (ULN 129) — but 39% rise in 6 weeks; watch Month 3; if >129 investigate |
| GGT | 37.0 U/L | 2026-06-02 | Unchanged | ✅ Clear |
| Bilirubin (Total) | 1.30 mg/dL | 2026-06-02 | Unchanged | ✅ Consistent with Gilbert's baseline |
| Bilirubin (Direct) | 0.27 mg/dL | 2026-06-02 | −0.23 from baseline | ✅ Improved |
| Creatinine | 0.97 mg/dL | 2026-06-02 | −0.30 from personal baseline | ✅ Now within lab range |
| Urea | 47.6 mg/dL | 2026-06-02 | +19.6 from baseline | ⚠️ High-normal — likely hydration; watch Month 3 |
| Uric Acid | 3.9 mg/dL | 2026-06-02 | −0.3 from baseline | ✅ Clear |
| LDL | 110.6 mg/dL | 2026-06-02 | −129.2 (−53.9% from pre-statin baseline) | ✅ Excellent response — no escalation |
| HDL | 48 mg/dL | 2026-06-02 | −10 from baseline | ⚠️ Still in range — declining trend; watch Month 3 |
| Total Cholesterol | 173.0 mg/dL | 2026-06-02 | −152 from baseline | ✅ Now normal |
| Triglycerides | 72 mg/dL | 2026-06-02 | −64 from baseline | ✅ Excellent |
| TC/HDL Ratio | 3.6 | 2026-06-02 | −2.0 from baseline | ✅ Now within range |
| Fasting Glucose | 81 mg/dL | 2026-06-02 | +4 from baseline | ✅ Normal |
| HbA1c | 5.5% | 2026-06-02 | +0.4% from baseline | ⚠️ Approaching 5.6% high-risk threshold — monitor; dietary discretion re refined carbohydrates |
| TSH | 1.400 mIU/mL | 2026-06-02 | +0.381 from baseline | ✅ Normal |
| CRP | 3.8 mg/L | 2026-06-02 | −2.2 from baseline | ✅ Improving — consistent with JAK inhibition |
| ESR | 5.0 mm/hr | 2026-06-02 | −5.0 from baseline | ✅ Improving |
| CPK | Not collected | — | — | ⚠️ Pending — explicitly request on Month 3 draw 2026-07-25 |

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
| 2026-06-02 | Day 38 (functional baseline) | 100 (estimated) | 0% | Baseline photo set taken Day 38 — no Day 1 photos recorded; no terminal regrowth expected at this stage |
| — | Month 3 (2026-07-25) | — | — | First formal SALT score due |
| — | Month 6 (2026-10-25) | — | — | First escalation decision point |
| — | Month 9 | — | — | |
| — | Month 12 (2027-04-25) | — | — | Full annual assessment |

---

## MEDICATION LOG

| Drug | Dose | Frequency | Start Date | Status | Notes |
|---|---|---|---|---|---|
| Tofacitinib citrate | 5 mg | BID | 2026-04-25 | Active | Primary treatment |
| Rosuvastatin (Sun Pharmaceutical) | 5 mg | QD | 2026-04-22 | Active — confirmed continue | Lipid management; hydrophilic — lower myopathy risk; no CYP3A4 overlap with tofacitinib; likely long-term independent of tofacitinib given pre-treatment LDL magnitude |
| Ezetimibe / MIBE 10 (ATOZ Pharmaceuticals) | 10 mg | QD | 2026-04-22 | Active — confirmed continue | Combination lipid management; LDL 53.9% reduction at Day 38; no de-escalation indicated |
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

**⚠️ High-ambush-risk drugs to check before taking anything new:**
- **Fluconazole** (common antifungal for thrush/skin infections) — near-doubles tofacitinib exposure; requires dose reduction to 5 mg QD for duration
- **Clarithromycin** (common antibiotic) — strong CYP3A4 inhibitor; same consequence
- Any new antibiotic, antifungal, or antiviral: check against this list before the first dose

---

## VACCINATION LOG

| Vaccine | Dose 1 | Dose 2 | Status | Notes |
|---|---|---|---|---|
| Shingrix (RZV) — recombinant, non-live | N/A | N/A | Unavailable in Sri Lanka | Zoster risk managed via prodrome education and valacyclovir access — see plan below |
| Hepatitis B series — 3 dose | ⚠️ OVERDUE | Pending | Not started — URGENT as of Day 38 | Anti-HBs 8.25 non-reactive; no protective immunity; initiate Dose 1 immediately; Dose 2 at 1 month after Dose 1; Dose 3 at 6 months; check Anti-HBs 4–8 weeks post-series |
| MMR | Unknown | — | Verify vaccination records | Live vaccine — contraindicated while on tofacitinib; verify historical records only |
| Varicella | Unknown | — | Verify vaccination records or confirm prior infection | Live vaccine — same restriction as MMR |
| Influenza (annual, inactivated) | Pending | — | Due next flu season | Safe during therapy — inactivated formulation only; NOT live nasal spray |
| COVID-19 booster | Pending | — | Per national schedule | Safe during therapy |

**Zoster management plan (replacing unavailable Shingrix):**
- Patient educated on prodrome: unilateral dermatomal burning / tingling / pain typically 2–4 days before skin changes — act at this stage, do not wait for rash
- **Treatment dose if episode occurs: Valacyclovir 1000 mg TID × 7 days** — must begin within 72 hours of rash onset
- Do NOT confuse with prophylactic dose (500 mg QD ongoing) — these are different regimens
- **Tofacitinib action:** Hold from prodrome recognition; resume only after all lesions fully crusted AND 7-day valacyclovir course complete (typically 10–14 days total hold)
- **⚠️ Physical possession of valacyclovir 1000 mg tablets not yet confirmed** — must be in hand, not just "accessible locally"
- Low-dose prophylaxis (valacyclovir 500 mg QD ongoing) is a separate clinical option — discuss with treating doctor

---

## TIMELINE AND MILESTONES

| Milestone | Target Date | Completed | Notes |
|---|---|---|---|
| Baseline labs collected | 2026-04-21 | [x] | Forte Diagnostics — all panels complete |
| IGRA result confirmed negative | 2026-04-24 | [x] | Final mandatory clearance test |
| Baseline clearance session with Claude | 2026-04-24 | [x] | All mandatory prerequisites satisfied |
| **Treatment start (Day 1)** | **2026-04-25** | **[x]** | **Tofacitinib 5 mg BID commenced** |
| Valacyclovir 1000 mg — physical possession confirmed | Before Day 1 | [ ] ⚠️ | Physical confirmation still pending — confirm immediately |
| MMR / Varicella vaccination status verified | Before Day 1 | [ ] | Check records; live vaccines contraindicated during therapy |
| **Hepatitis B Dose 1** | **Before or near Day 1** | **[ ] ⚠️ OVERDUE** | **38 days into immunosuppression — initiate this week** |
| Month 1 labs (CBC, LFTs, renal + CPK) | 2026-05-25 | [x] — collected 2026-06-02 (Day 38) | 8 days late; complete except CPK — CPK missed again |
| **4–8 week lipid recheck** | **2026-06-06 to 2026-06-20** | **[x] — collected 2026-06-02** | **4 days before window; clinically valid at Day 38** |
| Functional baseline photo set | 2026-06-02 | [x] | 4 angles taken Day 38; stored: Drive/SALT_Photos/2026-06-02_Day38_baseline/ |
| Next interim photo set | ~2026-07-05 (Day 68) | [ ] | Match conditions: same angles, lighting, wet vs dry hair |
| Hepatitis B Dose 2 | ~1 month after Dose 1 | [ ] | Schedule once Dose 1 is given |
| **Month 3 labs + first formal SALT score** | **2026-07-25** | **[ ]** | **CBC, LFTs, renal, lipids, CPK (explicit on requisition), SALT score** |
| Hepatitis B Dose 3 | ~6 months after Dose 1 | [ ] | Schedule once Dose 1 is given |
| Post-HBV series Anti-HBs check | ~4–8 weeks after Dose 3 | [ ] | Confirm seroconversion |
| Month 6 escalation review | 2026-10-25 | [ ] | Escalate to 10 mg BID if SALT improvement <50% and labs stable |
| Month 6 full labs | 2026-10-25 | [ ] | All panels |
| Month 12 full assessment | 2027-04-25 | [ ] | Full labs + SALT + clinical review |
| Annual TB rescreening (IGRA) | 2027-04-25 | [ ] | 12 months from baseline |
| Annual skin exam | 2027-04-25 | [ ] | NMSC surveillance — full body dermatology exam |
| Influenza vaccine (inactivated) | Next flu season | [ ] | Annually while on treatment |
| FH workup / family lipid history discussion | At next clinical visit | [ ] | Pre-treatment LDL 239.8 + TC 325 at age 22 — magnitude suggests possible familial hypercholesterolemia; statins may be lifelong independent of tofacitinib |

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
| Any new medication prescribed by another provider | Cross-check against Drugs and substances to avoid BEFORE first dose |