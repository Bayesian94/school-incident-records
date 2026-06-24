# school-incident-records

학교 사안 기록을 정리하는 Codex Skill입니다. 교육활동침해 의심 사안, 학교폭력 의심 사안, 생활지도·상담 사안, 보호자 민원과 연결된 학생 사안을 **개인정보 마스킹, 사실·진술·조치 분리, 매뉴얼 근거 확인, 보고서 초안, 학생별 NEIS 누가기록 초안**으로 정리합니다.

이 Skill은 사안을 판단하거나 결론 내리는 도구가 아닙니다. 교사가 책임 있게 검토하고 학교 절차에 따라 처리할 수 있도록 기록을 구조화하는 보조 도구입니다.

## 가장 쉬운 사용법

아래 문장을 Codex에 붙여넣고 `[repository-url]`을 이 저장소 주소로 바꾸세요.

```text
다음 GitHub 저장소의 school-incident-records Skill을 설치하고 사용 준비를 도와줘.

[repository-url]

설치한 뒤 project-template을 복사해 새 작업 폴더를 만들고,
references/immutable-manuals/에 학교 매뉴얼과 참고자료를 넣을 수 있게 안내해줘.
그 다음 사안 내용, 문서, 음성파일, 녹취록을 넣으면 개인정보를 마스킹하고,
학교 기준을 확인한 뒤 타임라인, 시각화, 관리자 보고 초안, 후속 확인 목록을 만들어줘.
내가 같은 대화창에서 사안종료라고 말하면 학생별·날짜별·시간대별 NEIS 누가기록 초안을 정리해줘.
```

## 이 Skill이 필요한 상황

- 교사가 사안을 인지했지만 사실, 진술, 조치, 미확인 사항이 섞여 있는 경우
- 교육활동침해 사안인지, 학교폭력 사안인지 아직 확정되지 않은 초기 기록을 정리해야 하는 경우
- 상담 메모, 보호자 상담 기록, 녹취록, 음성 전사본, 교사 메모를 한 흐름으로 묶어야 하는 경우
- 관리자에게 보고할 초안은 필요하지만 단정적 판단문은 피해야 하는 경우
- 사안이 마무리된 뒤 학생별 NEIS 누가기록 문구를 날짜와 시간대별로 정리해야 하는 경우

## 작업 흐름

```text
1. 참고자료 폴더 준비
   references/immutable-manuals/에 학교 매뉴얼과 원칙을 넣습니다.

2. 사안 자료 입력
   교사 메모, 문서, 음성파일, 녹취록, 상담 기록을 raw/ 또는 대화창에 제공합니다.

3. 개인정보 마스킹
   실제 이름, 연락처, 학번, 학교명 등은 학생A, 보호자A, 학교A처럼 바꿉니다.

4. 기록 분리
   사실, 진술, 교사 조치, 미확인 사항, 후속 확인으로 나눕니다.

5. 매뉴얼 대조
   참고자료에 근거가 있는 절차만 후보로 정리하고, 불명확한 부분은 확인 필요로 남깁니다.

6. 보고 산출물 작성
   타임라인, 시각화, 후속 확인 체크리스트, 관리자 보고 초안을 만듭니다.

7. 사안종료
   교사가 "사안종료"라고 말하면 학생별·날짜별·시간대별 NEIS 누가기록 초안으로 정리합니다.
```

## 먼저 넣어야 할 참고자료

새 작업을 시작하기 전에 `references/immutable-manuals/`에 다음 자료를 넣으세요.

```text
references/immutable-manuals/
  education-activity-protection-manual.*
  school-violence-or-student-guidance-manual.*
  internal-reporting-procedure.*
  neis-cumulative-record-guideline.*
  local-report-template-or-style-sample.*
```

이 폴더는 수정하지 않는 참고자료 폴더입니다. Skill은 이 폴더의 자료를 원본 기준으로 읽고, 내용을 바꾸거나 삭제하지 않습니다. 자료가 부족하면 Codex는 보고서 작성을 멈추고 필요한 자료 목록을 먼저 요청해야 합니다.

## 입력할 수 있는 자료

- 교사가 직접 쓴 사안 설명
- 상담 메모
- 학생 진술 메모
- 보호자 상담 메모
- 관리자 보고용 메모
- 문서 파일
- 음성파일
- 녹취록 또는 전사본
- 사진·스캔 자료에서 추출한 텍스트

음성파일은 로컬에서 전사할 수 있을 때만 전사합니다. 외부 서비스에 음성이나 문서를 업로드해야 하는 경우에는 교사의 명시적 허락이 필요합니다.

## 생성되는 결과물

일반 사안 정리 단계에서는 `outputs/`에 다음 파일을 만듭니다.

```text
fact-statement-action-table.md
incident-timeline.md
incident-timeline-visual.md
follow-up-checklist.md
admin-report-draft.md
teacher-review-checklist.md
```

교사가 `사안종료`라고 말하면 NEIS 정리 단계로 전환해 다음 파일을 만듭니다.

```text
neis-student-log-draft.md
neis-entry-review-checklist.md
```

NEIS 초안은 학생별, 날짜별, 시간대별로 정리됩니다. Codex가 NEIS에 자동 입력하지 않습니다. 교사가 검토한 뒤 직접 입력해야 합니다.

## 하지 않는 일

- 학교폭력 여부를 판단하지 않습니다.
- 교육활동침해 여부를 판단하지 않습니다.
- 가해·피해, 고의성, 책임 소재를 단정하지 않습니다.
- 징계나 조치 결정을 권고하지 않습니다.
- 보호자, 기관, 경찰, 위원회, 교직원에게 자동 연락하지 않습니다.
- NEIS나 공식 시스템에 자동 입력하지 않습니다.
- 외부 신고, 공문 발송, 결재 상신을 자동으로 하지 않습니다.

## 저장소 구조

```text
school-incident-records/
  README.md
  LICENSE
  .gitignore
  skills/
    school-incident-records/
      SKILL.md
      agents/
        openai.yaml
      references/
        workflow.md
        privacy-and-safety.md
        output-schemas.md
        neis-closing.md
      assets/
        project-template/
  examples/
    dummy-project/
```

## 직접 설치

`skills/school-incident-records/` 폴더를 Codex skills 폴더에 복사한 뒤 새 대화에서 다음처럼 호출합니다.

```text
Use $school-incident-records to set up a new school incident record project.
```

## 새 사안 작업 시작

1. `skills/school-incident-records/assets/project-template/`를 개인 작업 폴더로 복사합니다.
2. `references/immutable-manuals/`에 학교에서 사용하는 매뉴얼과 기준을 넣습니다.
3. `raw/`에 교사 메모, 녹취록, 전사본, 문서 자료를 넣습니다.
4. `request/incident-intake.md`를 작성합니다.
5. Codex에 `$school-incident-records`를 사용하라고 요청합니다.
6. `outputs/`의 결과물을 검토합니다.
7. 사안별 기록 정리가 끝나면 같은 대화창에서 `사안종료`라고 입력합니다.

## 공개 저장소 주의

이 저장소에는 빈 템플릿과 더미 예시만 포함되어야 합니다. 실제 학생 기록, 실제 학교 매뉴얼, 내부 공문, 상담 기록, 녹취록, 음성파일, NEIS 기록, 개인정보가 포함된 자료를 공개 GitHub 저장소에 올리지 마세요.

## 더미 예시

`examples/dummy-project/`에는 실제 자료가 아닌 가상 예시가 들어 있습니다. 구조와 출력 형식을 이해하기 위한 샘플이며, 실제 학생 기록이 아닙니다.
