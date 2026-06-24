# NEIS Closing Mode

Use this reference only when the teacher says `사안종료`.

`사안종료` means: "Summarize the current conversation and working files into student-by-student NEIS cumulative record drafts." It does not mean the incident is legally or administratively closed.

## Process

1. Re-read deidentified records and outputs.
2. Group entries by student.
3. Sort by date and time period.
4. Keep only information relevant to that student's cumulative record.
5. Remove unnecessary sensitive details about other students.
6. Mark uncertain points as `확인 필요`.
7. Produce drafts for teacher review and manual entry.

## Output

Create `outputs/neis-student-log-draft.md`:

```md
# NEIS Student Log Draft

## 학생A

| Date | Time | Record Type | Draft Text | Source | Review Needed |
|---|---|---|---|---|---|

## 학생B

| Date | Time | Record Type | Draft Text | Source | Review Needed |
|---|---|---|---|---|---|

## Before Manual NEIS Entry

- [ ] Records are separated by student.
- [ ] Dates and time periods are included where known.
- [ ] No real names or direct identifiers remain.
- [ ] Other students' unnecessary sensitive statements are removed.
- [ ] No final school violence, education activity infringement, sanction, or offender-victim determination is made.
- [ ] Teacher reviews and manually enters the final text in NEIS.
```

## Drafting Style

Use short neutral Korean sentences. Example:

```text
더미일자1 2교시 후 복도에서 학생B와 말다툼이 있었다는 교사 관찰 기록이 있어, 학생A의 진술을 분리해 청취함. 학생A는 상대가 먼저 놀렸다고 진술함. 추가 확인 필요.
```
