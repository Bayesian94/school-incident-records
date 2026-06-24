---
name: school-incident-records
description: Use when a teacher needs to organize school incident records, including suspected school violence, education activity infringement, student guidance, counseling, parent-related incidents, transcripts, audio-derived notes, or incident documents, without making legal, disciplinary, school-violence, offender-victim, or final procedural determinations.
---

# School Incident Records

## Overview

Use this skill to turn teacher-provided school incident material into privacy-protected records, timelines, report drafts, and NEIS-ready student log notes. The core rule is: document, separate, and preserve; do not judge, decide, classify conclusively, report externally, or enter official systems.

## Required Boundaries

- Do not determine whether an incident is school violence, education activity infringement, harassment, abuse, or a disciplinary matter.
- Do not label any student as perpetrator, victim, offender, aggressor, or complainant unless the teacher's official source already uses that label; even then, mark the source.
- Do not recommend final sanctions, disciplinary measures, legal actions, external reports, or official conclusions.
- Do not contact guardians, agencies, police, committees, or school staff.
- Do not enter NEIS or any official system. Produce drafts only for teacher review and manual entry.
- Do not modify or delete original incident materials or immutable reference manuals.

## First-Run Setup

When the project has no prepared reference folder, stop incident processing and guide the teacher to create:

```text
references/immutable-manuals/
  education-activity-protection-manual.*
  school-violence-or-student-guidance-manual.*
  internal-reporting-procedure.*
  neis-cumulative-record-guideline.*
  local-report-template-or-style-sample.*
```

If manuals are missing or insufficient, create `outputs/needed-reference-materials.md` and ask for the missing materials. Do not draft conclusions or procedural recommendations until references are available.

Use `assets/project-template/` as the folder template for new work.

## Normal Incident Workflow

When the teacher provides incident text, documents, notes, audio files, or transcripts:

1. Preserve input in `raw/` or ask the teacher to place it there. Do not rewrite originals.
2. For audio, use only available trusted local transcription tools. If transcription is unavailable, ask for a transcript or teacher-verified summary. Do not upload audio to external services without explicit permission.
3. Create or update `data/masking-map.teacher-only.md` with real-name to placeholder mappings for teacher verification only.
4. Create `data/deidentified-incident-record.md` and use only masked names in all shared outputs.
5. Read `references/immutable-manuals/` and summarize source coverage in `data/reference-materials.csv`.
6. Separate records into facts, statements, teacher actions, unresolved items, and follow-up checks.
7. Produce report materials in `outputs/` using neutral language and source references.

Read these references when needed:

- `references/workflow.md` for the full step-by-step process.
- `references/privacy-and-safety.md` for masking and prohibited outputs.
- `references/output-schemas.md` for file formats and section templates.
- `references/neis-closing.md` when the teacher says `사안종료`.

## Output Set

Create these outputs when enough information is available:

- `outputs/fact-statement-action-table.md`
- `outputs/incident-timeline.md`
- `outputs/incident-timeline-visual.md`
- `outputs/follow-up-checklist.md`
- `outputs/admin-report-draft.md`
- `outputs/teacher-review-checklist.md`

Each output must include only masked names, source references, and verification status. Use "확인 필요" when date, time, source, manual basis, or procedure is uncertain.

## Closing Trigger: 사안종료

When the teacher says `사안종료`, switch to NEIS preparation mode. This does not mean the incident is legally, administratively, or procedurally closed.

Produce:

- `outputs/neis-student-log-draft.md`
- `outputs/neis-entry-review-checklist.md`

Group notes by student, date, and time period. Write neutral cumulative-record draft text that a teacher can review and manually enter into NEIS. Do not include unnecessary sensitive statements about other students.

## Final Self-Check

Before responding, verify:

- No real names, phone numbers, addresses, school names, class identifiers, local file paths, or credentials appear in shared outputs.
- Originals and immutable manuals were not modified.
- Facts and statements are separated.
- Every assertion has a source or `확인 필요`.
- No final determination, sanction, external report, or official-system action is stated as completed.
