# PROMPTS.md — SESSION PROMPTS
# You attach a file, paste the relevant prompt, Claude does the extraction and analysis.
# No manual data entry required.
# Last updated: [YYYY-MM-DD]

---

## HOW TO USE

1. Start every session with the SESSION STARTER below — always, no exceptions.
2. Identify your session type from the list.
3. Attach your file(s) to the Claude chat.
4. Copy and paste the matching prompt.
5. Add one or two sentences of personal context if anything is unusual.
6. At the end of Claude's response, check the FILE UPDATE SUGGESTIONS block.
   Apply those updates to SYSTEM.md in Drive.

---

## SESSION STARTER
# Paste this at the top of every conversation before anything else.
# This orients Claude, confirms it has your current data, and activates the
# file update detection behavior for the whole session.

```
Session start. You are my tofacitinib treatment tracking assistant.

Confirm you have read my SYSTEM.md from Project Knowledge by telling me:
- My current treatment status (pre-treatment / active — phase / dose)
- My last recorded SALT score and date
- My next scheduled lab or milestone date
- Any values currently flagged as needing attention

Then proceed with today's session. Monitor throughout for any new, updated,
or corrected information that should be recorded in my .md files, and output
FILE UPDATE SUGGESTIONS at the end of your response wherever relevant.
```

---

## PROMPT 1 — BASELINE LAB CLEARANCE
# Use when: you have your pre-treatment baseline reports and want Claude
# to assess whether you are clear to start tofacitinib.
# Attach: all baseline lab report files.

```
Baseline lab reports attached. I have not started tofacitinib yet.

1. Extract every value from these reports
2. Populate my SYSTEM.md baseline table with all extracted values
3. Fill in the ULN values for ALT and AST from these reports
4. Assess each value against the standard tofacitinib initiation criteria
5. Give me a clear go / no-go verdict with reasoning
6. Flag any value that is borderline or requires attention before starting
7. Identify any test from the required baseline panel that is missing
8. If cleared: tell me the dates I should schedule my 4–8 week lipid recheck
   and my Month 1 labs based on today's date
```

---

## PROMPT 2 — LAB REPORT (ONGOING MONITORING)
# Use when: you have a lab report PDF or photo from a monitoring blood test.
# Attach: the lab report file.

```
Lab report attached. This is from [Month X / date of test].

Extract every value from this report. For each one:
- Compare to my baseline in SYSTEM.md
- Calculate percentage change from baseline
- Check against my hard stop thresholds
- Flag anything crossing a threshold or trending in a concerning direction

Output a structured table: Test | Result | Baseline | Change | Status
Then give me a plain-language summary of what this means for my current phase.
```

---

## PROMPT 3 — PRESCRIPTION OR MEDICATION DOCUMENT
# Use when: you have a new prescription, pharmacy label, or medication record.
# Attach: photo or scan of the document.

```
Prescription or medication document attached.

Extract the drug name, dose, frequency, prescribing date, and any listed
warnings or interactions. Cross-check immediately against my contraindicated
substances list in SYSTEM.md. If anything conflicts, flag it at the top
before any other analysis.

Then tell me what needs to be updated in my medication log.
```

---

## PROMPT 4 — VACCINE CERTIFICATE OR RECORD
# Use when: you have a vaccination certificate, clinic record, or shot card.
# Attach: photo or scan of the document.

```
Vaccine record attached.

Extract the vaccine name, manufacturer if listed, dose number, and date
administered. Confirm whether this vaccine is safe during tofacitinib
therapy (live vs non-live). Tell me if any follow-up dose is due and when.
```

---

## PROMPT 5 — SALT PHOTOS
# Use when: you are doing your monthly SALT assessment.
# Attach: four photos — top (vertex), back (occipital), left side, right side.
# Claude guides you through quadrant estimates one at a time.

```
SALT photos attached — top, back, left side, right side.
Date of photos: [YYYY-MM-DD]
Month on treatment: [X]

Prompt me for my estimated percentage hair loss per quadrant, one at a time.
Then calculate my SALT score, show the working, compare to my baseline and
my last recorded SALT score in SYSTEM.md, and tell me what this means for
my current phase.
```

---

## PROMPT 6 — SYMPTOM UPDATE
# Use when: you want to log how you have been feeling. No file needed.

```
Symptom update — [date / day and month on treatment].

[Write 2–5 sentences: how you have been feeling, any hair changes, skin,
energy, GI issues, infections, unusual events, missed doses, new medications.]

Assess against my protocol. Flag anything that could indicate a side effect
requiring action. Note patterns if any symptom has appeared in previous
updates this session.
```

---

## PROMPT 7 — MEDICAL REPORT OR CLINIC LETTER
# Use when: you have a doctor's letter, dermatology note, or any clinical document.
# Attach: the document file.

```
Medical document attached.

Extract key clinical findings, recommendations, values or scores mentioned,
and any instructions given. Summarise in plain language and flag anything
relevant to my tofacitinib protocol or that requires action on my part.
```

---

## PROMPT 8 — MONTHLY CHECK-IN (FULL SESSION)
# Use when: it is your monthly review.
# Attach: all files for that month — lab PDF, SALT photos, any other documents.

```
Monthly check-in — Month [X], [date].

Files attached: [list them — e.g. lab PDF, four SALT photos]
Context: [2–3 sentences — how the month went, adherence, anything unusual]

Run the full monthly analysis:
1. Extract and assess all lab values vs my baseline and thresholds
2. Guide me through the SALT assessment from the photos
3. Calculate SALT score and compare to previous readings
4. Review current phase and whether any dose decision is approaching
5. Flag anything needing action
6. Output session summary and FILE UPDATE SUGGESTIONS
```

---

## PROMPT 9 — DRUG OR SUPPLEMENT CHECK
# Use when: you are considering a new drug, supplement, or OTC product.
# No file needed.

```
I am considering taking [drug / supplement name, dose].

Check this against my contraindicated substances list in SYSTEM.md and
against known tofacitinib interactions. Tell me if it is safe, if a dose
adjustment is needed, or if I should avoid it. Give me the mechanism.
```

---

## QUICK REFERENCE

| Situation | Prompt |
|---|---|
| Have baseline reports, not yet started | Prompt 1 — Baseline Clearance |
| Got monitoring lab results | Prompt 2 — Lab Report |
| New prescription or medication | Prompt 3 — Prescription |
| Had a vaccine, need to log it | Prompt 4 — Vaccine Record |
| Monthly hair assessment | Prompt 5 — SALT Photos |
| Logging symptoms or observations | Prompt 6 — Symptom Update |
| Doctor's letter or clinic note | Prompt 7 — Medical Report |
| Full monthly review | Prompt 8 — Monthly Check-In |
| Checking if a new drug is safe | Prompt 9 — Drug Check |