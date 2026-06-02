# DESIGN.md — SYSTEM ARCHITECTURE AND WORKFLOW
# Tofacitinib Treatment Tracking System
# Read this once. Follow it. Do not redesign until you have used it for 3 months.
# Last updated: [YYYY-MM-DD]

---

## WHAT THIS SYSTEM IS

A personal medical tracking system using Google Drive as permanent cloud storage
and Claude Projects as the analysis engine. You upload documents, Claude reads and
interprets them against your protocol, and structured update instructions are
generated at the end of every session. No manual data entry. No files lost.

---

## PART 1 — STORAGE: GOOGLE DRIVE

### Why Google Drive
- Permanently backed up and accessible from any device
- Claude's Google Drive connector can search and fetch files directly during sessions
- Nothing is lost if your device is replaced or damaged
- No extra services needed — already set up

### Folder structure (already created in your Drive)

```
Medical - Tofacitinib - Personal Health System/
├── _system/
│   ├── SYSTEM.md                          ← Master context. Update after every session.
│   ├── PROMPTS.md                         ← Session prompts. Reference at session start.
│   ├── DESIGN.md                          ← This file. Architecture and workflow.
│   ├── PROJECT_INSTRUCTIONS.md            ← Exact text for Claude Project Instructions field.
│   └── Clinical Reference — Tofacitinib AU.md  ← Full clinical reference. Static.
│
├── labs/
│   └── YYYY-MM-DD_labs_[context].pdf
│       e.g. 2025-07-15_labs_baseline.pdf
│           2025-09-15_labs_month3.pdf
│
├── symptoms/
│   └── [Google Sheet — auto-populated from symptom Google Form]
│
├── medications/
│   └── YYYY-MM-DD_prescription_[drugname].pdf
│
├── vaccines/
│   └── YYYY-MM-DD_vaccine_[name]_dose[N].pdf
│
├── reports/
│   └── SALT_photos/
│       └── SALT_YYYY-MM-DD_[top/back/left/right].jpg
│
├── checkins/
│   └── Treatment Log — Running Record.md  ← Single doc. Append monthly. Never delete.
│
└── exports/
    └── YYYY-MM-DD_session_output.md
```

### File naming rule
Always prefix with YYYY-MM-DD. Alphabetical sort = chronological sort automatically.

---

## PART 2 — CLAUDE PROJECT SETUP

### What is already done
- Project created: Tofacitinib Treatment Log
- Folder structure created in Drive
- Symptom Google Form created

### What to keep current in Project Knowledge
Upload these two files to Project Knowledge. They are loaded into Claude's context
at the start of every conversation automatically.

| File | Purpose | When to re-upload |
|---|---|---|
| SYSTEM.md | Your personal data — baselines, current values, milestones | When phase changes, dose changes, or quarterly |
| Clinical Reference — Tofacitinib AU.md | Full clinical protocol — static reference | Once only. Never needs updating. |

### Project Instructions
The exact text for the Project Instructions field lives in PROJECT_INSTRUCTIONS.md
in your _system folder. Copy and paste from there. Do not paraphrase it.
This is the most important configuration in the entire system — it controls
how Claude behaves in every session, including the file update detection protocol.

### Google Drive connector
Ensure the Drive connector is active in the Claude Project. This allows Claude to
search and fetch files from your Drive during sessions when needed, without
requiring you to manually attach every file.

---

## PART 3 — FILE UPDATE DETECTION PROTOCOL

This is the core behavior added in the current version of the system.

### What it does
During every conversation, Claude monitors for information that is new, updated,
or corrected relative to what is recorded in your .md files. At the end of any
response where such information is detected, Claude outputs a FILE UPDATE
SUGGESTIONS block with precise, copy-paste ready instructions — specifying the
exact file, section, action, and content. You make only the listed changes.
Nothing else is touched.

### Why this approach
- Eliminates rewriting whole files to capture a single new value
- Reduces token cost — only changed content is generated
- Creates a clear audit trail of what changed and when
- Keeps SYSTEM.md accurate without requiring you to remember what to update

### Your responsibility
After every session that produces FILE UPDATE SUGGESTIONS:
1. Open the relevant file in Google Drive
2. Apply each listed change exactly as specified
3. Update the version number and "Last updated" date at the top of SYSTEM.md
4. Save the file

That is the only manual step in the entire workflow.

### When to re-upload SYSTEM.md to Project Knowledge
- After the baseline clearance session (first major population of values)
- After a dose change
- After a phase change (pre-treatment → active → escalation → consolidation)
- Otherwise: quarterly is sufficient, since Claude can fetch the live version
  from Drive via the connector during sessions

---

## PART 4 — SYMPTOM LOGGING: GOOGLE FORM

A Google Form is already created: "Tofacitinib Protocol - SYMPTOM LOGGING"

Fill it in once a day or whenever something notable happens.
Responses auto-populate a Google Sheet in your Drive.
At your monthly session, Claude can access the Sheet directly via the Drive
connector, or you can paste the last month's rows into the chat.

---

## PART 5 — RUNNING RECORD: SINGLE GOOGLE DOC

One file: "Treatment Log — Running Record.md" in your checkins folder.
After every Claude session, append the session summary to the bottom.
Use this format for each entry:

```
---
## [Month Name] [Year] — Month [N] on treatment / Pre-treatment
Date: YYYY-MM-DD
SALT: [score] ([X]% improvement from baseline)
Dose: [X] mg BID / Not started
Key labs: [one-line summary or "Baseline pending"]
Events: [one-line summary]
Next action: [one specific thing + date]
---
[Paste Claude's full session summary below]
```

This document is your complete treatment narrative. Never delete entries.
If a physician ever asks for your treatment history, this is the document to share.

---

## PART 6 — SESSION WORKFLOW

### Before the session (2–5 minutes)
- Collect any new files — lab PDF, prescription scan, vaccine record, SALT photos
- Name files correctly (YYYY-MM-DD prefix) and save to the correct Drive subfolder
- If monthly session: note anything significant from your symptom Google Sheet

### Running the session
1. Open claude.ai → Tofacitinib Treatment Log project → New conversation
2. Paste the SESSION STARTER from PROMPTS.md — always first, every session
3. Confirm Claude's orientation response is correct before proceeding
4. Attach your files
5. Paste the relevant session prompt from PROMPTS.md
6. Add a sentence of context if anything unusual happened

### Ending the session
1. Read Claude's SESSION SUMMARY block
2. Read the FILE UPDATE SUGGESTIONS block
3. Apply each update to the relevant file in Drive
4. Update SYSTEM.md version number and date
5. Paste Claude's full response into your Running Record doc
6. Save a copy to exports/ as YYYY-MM-DD_session_output.md

### Total time per session
- Monthly full check-in: 30–45 minutes
- Lab-only or single document: 10–15 minutes
- Quick symptom or drug check: 5 minutes

---

## PART 7 — MONTHLY SCHEDULE

| Timing | Action | Time |
|---|---|---|
| Week 1 | Book labs if due this month | 2 min |
| Week 2–3 | Get labs done at clinic | At clinic |
| Week 3–4 | Take 4 SALT photos | 5 min |
| Week 3–4 | Full Claude session | 30–45 min |
| Daily | Fill in symptom Google Form | 60 sec |

---

## PART 8 — WHAT LIVES WHERE

| Item | Location | Updated by |
|---|---|---|
| SYSTEM.md — live version | Drive / _system/ | You, after each session (FILE UPDATE SUGGESTIONS) |
| SYSTEM.md — Claude's copy | Claude Project Knowledge | You, re-upload at phase/dose changes or quarterly |
| Clinical Reference | Claude Project Knowledge | Once — never update |
| Lab PDFs | Drive / labs/ | You, after each blood test |
| SALT photos | Drive / reports/SALT_photos/ | You, monthly |
| Symptom data | Drive / symptoms/ (Sheet) | Auto-populated from Google Form |
| Prescriptions | Drive / medications/ | You, when new prescription issued |
| Vaccine records | Drive / vaccines/ | You, after each vaccination |
| Monthly summaries | Drive / checkins/ Running Record | You, paste after each session |
| Raw session outputs | Drive / exports/ | You, paste after each session |

---

## PART 9 — RELIABILITY RULES

1. Always use the SESSION STARTER at the top of every conversation.
   It activates the file update detection behavior for the whole session.

2. Apply FILE UPDATE SUGGESTIONS after every session that produces them.
   Skipping this is the only way the system breaks down.

3. Name files with YYYY-MM-DD prefix from day one.
   Fix this habit in week one and you will never hunt for a file again.

4. Keep the Running Record append-only.
   Never edit or delete past entries. It is your audit trail.

5. Do not add new .md files without also updating the FILE STRUCTURE MAP
   in SYSTEM.md so Claude knows where to route new information.

6. When in doubt whether a drug or supplement is safe, use Prompt 9
   before taking it — not after.

7. Do not redesign this system while actively using it.
   Note improvements and review at the 3-month mark.