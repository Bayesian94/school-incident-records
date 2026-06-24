# Workflow

Use this workflow for education activity infringement, suspected school violence, student guidance, counseling, parent-related incidents, or still-unclear school incident records.

## 1. Prepare References

Check `references/immutable-manuals/`.

Required reference categories:

- Education activity protection or teacher protection manual
- School violence or student guidance manual
- Internal school reporting procedure
- NEIS cumulative record guidance
- Local report template or style sample, if used by the school

If a category is missing, create `outputs/needed-reference-materials.md` and stop before report drafting.

## 2. Preserve Inputs

Accept these input types:

- Teacher-written incident summary
- Uploaded documents
- Counseling notes
- Student or guardian statement notes
- Audio file
- Transcript
- Photo or scan after text extraction

Store or ask the teacher to store original materials in `raw/`. Do not edit originals. If audio transcription is not available locally, ask for a transcript or teacher-verified summary.

## 3. Mask Personal Data

Create:

- `data/masking-map.teacher-only.md`
- `data/deidentified-incident-record.md`

Use placeholders:

- `학생A`, `학생B`
- `보호자A`
- `교사A`
- `관리자A`
- `학교A`

Never include the masking map in shared outputs.

## 4. Separate Records

Create `outputs/fact-statement-action-table.md` with these columns:

| Date | Time | Student | Category | Content | Source | Manual Basis | Verification | Follow-up |
|---|---|---|---|---|---|---|---|---|

Categories:

- Fact
- Statement
- Teacher action
- Unresolved item
- Follow-up check

## 5. Draft Outputs

Create:

- `outputs/incident-timeline.md`
- `outputs/incident-timeline-visual.md`
- `outputs/follow-up-checklist.md`
- `outputs/admin-report-draft.md`
- `outputs/teacher-review-checklist.md`

Use neutral language. Mark uncertain dates, times, source status, and manual basis as `확인 필요`.

## 6. Handle New Material

When the teacher adds more material in the same conversation:

1. Preserve the new input.
2. Update the masking map if new people appear.
3. Update the deidentified record.
4. Rebuild or append the table and outputs.
5. Keep prior uncertainty unless the new source resolves it.
