# school-incident-records

학교 사안 기록을 안전하게 정리하기 위한 Codex Skill입니다.

교육활동침해 의심 사안, 학교폭력 의심 사안, 생활지도·상담 사안, 보호자 민원과 연결된 학생 사안을 교사가 책임 있게 검토할 수 있도록 **개인정보 마스킹, 사실·진술·조치 분리, 매뉴얼 근거 확인, 관리자 보고 초안, 학생별 NEIS 누가기록 초안**으로 정리합니다.

이 Skill의 핵심은 “판단”이 아니라 “기록 정리”입니다. Codex가 학교폭력 여부나 교육활동침해 여부를 판단하지 않습니다. 가해·피해를 단정하지 않고, 징계나 조치를 결정하지 않으며, NEIS나 외부 기관에 자동 입력·발송하지 않습니다.

## 한 줄 요약

교사가 사안 자료를 넣으면 Codex가 원본을 보존하고 개인정보를 가린 뒤, 사실·진술·조치·미확인 사항을 분리해 보고서 초안과 NEIS 누가기록 초안으로 정리하는 Skill입니다.

## 누구를 위한 Skill인가

- 담임교사
- 생활지도 담당 교사
- 학교폭력 업무 담당 교사
- 교육활동보호 업무 담당 교사
- 상담 기록이나 사안 보고 초안을 정리해야 하는 교사
- 사안 기록을 누락 없이 정리하고 싶지만 AI가 임의 판단하는 것은 피하고 싶은 교사

## 어떤 상황에서 쓰는가

다음처럼 기록은 필요하지만 결론을 내리기 조심스러운 상황에 맞습니다.

- 교사가 사안을 인지했지만 사실, 진술, 조치, 미확인 사항이 섞여 있는 경우
- 교육활동침해 사안인지, 학교폭력 사안인지 아직 확정되지 않은 초기 상황
- 학생 진술, 보호자 상담, 교사 관찰, 관리자 보고 메모가 여러 곳에 흩어져 있는 경우
- 녹취록이나 음성 전사본을 근거 자료로 정리해야 하는 경우
- 관리자에게 보고할 초안을 만들되 단정적 판단문은 피해야 하는 경우
- 사안 정리 후 학생별 NEIS 누가기록 문구를 날짜와 시간대별로 나눠야 하는 경우

## 이 Skill이 하는 일

```text
입력 자료
  교사 메모, 상담 기록, 학생 진술, 보호자 상담 메모, 음성파일, 녹취록, 문서

처리 과정
  원본 보관
  개인정보 마스킹
  사실·진술·조치·미확인 사항 분리
  참고 매뉴얼 대조
  타임라인과 시각화 작성
  관리자 보고 초안 작성
  후속 확인 목록 작성

종료 단계
  교사가 "사안종료"라고 말하면
  학생별·날짜별·시간대별 NEIS 누가기록 초안 작성
```

## 이 Skill이 하지 않는 일

이 Skill은 다음 작업을 하지 않도록 설계되어 있습니다.

- 학교폭력 여부 판단
- 교육활동침해 여부 판단
- 가해·피해, 고의성, 책임 소재 단정
- 징계, 선도, 보호 조치 결정
- 법률 판단
- 보호자 자동 연락
- 외부 기관 자동 신고
- 위원회 개최 여부 결정
- 공문 자동 발송
- NEIS 자동 입력
- 학교 내부 시스템 자동 로그인

Codex는 교사의 책임을 대신하지 않습니다. 교사가 검토하고 학교 절차에 따라 직접 처리할 수 있도록 정리된 초안을 제공합니다.

## 가장 쉬운 사용법

아래 문장을 Codex에 붙여넣고 `[repository-url]`을 이 저장소 주소로 바꾸세요.

```text
다음 GitHub 저장소의 school-incident-records Skill을 설치하고 사용 준비를 도와줘.

[repository-url]

설치한 뒤 project-template을 복사해 새 작업 폴더를 만들고,
references/immutable-manuals/에 학교 매뉴얼과 참고자료를 넣을 수 있게 안내해줘.

그 다음 내가 사안 내용, 문서, 음성파일, 녹취록을 넣으면
개인정보를 마스킹하고 원본을 보관한 뒤,
학교 기준을 확인하면서 타임라인, 시각화, 관리자 보고 초안, 후속 확인 목록을 만들어줘.

내가 같은 대화창에서 사안종료라고 말하면
학생별·날짜별·시간대별 NEIS 누가기록 초안을 정리해줘.
```

## 먼저 준비해야 할 것

이 Skill은 사안을 임의로 처리하지 않기 위해 먼저 참고자료 폴더를 요구합니다.

새 작업을 시작하기 전에 개인 작업 폴더 안에 다음 폴더를 준비합니다.

```text
references/immutable-manuals/
```

이 폴더에는 학교 또는 교육청에서 사용하는 기준 자료를 넣습니다.

```text
references/immutable-manuals/
  education-activity-protection-manual.*
  school-violence-or-student-guidance-manual.*
  internal-reporting-procedure.*
  neis-cumulative-record-guideline.*
  local-report-template-or-style-sample.*
```

권장 자료:

- 교육활동보호 관련 매뉴얼
- 학교폭력 또는 학생 생활지도 관련 매뉴얼
- 학교 내부 사안 보고 절차
- NEIS 상담·생활지도 누가기록 기준
- 학교에서 실제 사용하는 보고서 양식 또는 문체 예시

`immutable-manuals`는 수정하지 않는 참고자료 폴더입니다. Codex는 이 폴더를 원본 기준으로 읽고, 내용을 바꾸거나 삭제하지 않아야 합니다. 자료가 부족하면 보고서 작성을 진행하지 않고 필요한 자료 목록을 먼저 요청합니다.

## 입력할 수 있는 자료

- 교사가 직접 쓴 사안 설명
- 교사 관찰 메모
- 학생 진술 메모
- 보호자 상담 메모
- 관리자 보고용 메모
- 상담 기록
- 문서 파일
- 음성파일
- 녹취록 또는 전사본
- 사진·스캔 자료에서 추출한 텍스트

음성파일은 로컬에서 전사할 수 있을 때만 전사합니다. 외부 서비스에 음성이나 문서를 업로드해야 하는 경우에는 교사의 명시적 허락이 필요합니다.

## 기본 작업 폴더 구조

Skill은 다음과 같은 작업 폴더 구조를 전제로 합니다.

```text
incident-workspace/
  request/
    incident-intake.md
  raw/
    README.md
  references/
    immutable-manuals/
      README.md
  data/
    README.md
  outputs/
    README.md
```

각 폴더의 역할은 다음과 같습니다.

| 폴더 | 역할 |
|---|---|
| `request/` | 교사가 사안 개요와 요청 산출물을 적는 곳 |
| `raw/` | 원본 자료를 보관하는 곳 |
| `references/immutable-manuals/` | 수정하지 않는 매뉴얼과 기준 자료 폴더 |
| `data/` | 마스킹 대응표, 비식별 기록, 참고자료 목록 등 중간 작업 파일 |
| `outputs/` | 타임라인, 보고서 초안, NEIS 초안 등 교사가 검토할 산출물 |

## 처리 흐름

```text
1. 참고자료 확인
   Codex가 references/immutable-manuals/를 확인합니다.
   자료가 부족하면 outputs/needed-reference-materials.md를 만들고 멈춥니다.

2. 원본 보관
   교사가 제공한 사안 자료를 raw/에 보관합니다.
   원본은 수정하지 않습니다.

3. 개인정보 마스킹
   실제 학생명, 보호자명, 교직원명, 학교명, 연락처, 학번 등을 학생A, 보호자A처럼 바꿉니다.
   마스킹 대응표는 data/masking-map.teacher-only.md에만 둡니다.

4. 비식별 사안 기록 작성
   data/deidentified-incident-record.md를 만듭니다.
   이후 공유 산출물은 이 비식별 기록을 기준으로 작성합니다.

5. 사실·진술·조치 분리
   관찰된 사실, 학생·보호자 진술, 교사가 이미 한 조치, 미확인 사항, 후속 확인을 분리합니다.

6. 매뉴얼 대조
   참고자료에 근거가 있는 절차만 후보로 정리합니다.
   근거가 없거나 불명확하면 확인 필요로 남깁니다.

7. 보고 산출물 작성
   타임라인, 시각화, 후속 확인 체크리스트, 관리자 보고 초안을 만듭니다.

8. 사안종료
   교사가 사안종료라고 말하면 학생별 NEIS 누가기록 초안으로 전환합니다.
```

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

각 파일의 역할은 다음과 같습니다.

| 파일 | 역할 |
|---|---|
| `fact-statement-action-table.md` | 사실, 진술, 교사 조치, 미확인 사항을 표로 분리 |
| `incident-timeline.md` | 날짜와 시간대 기준 사안 흐름 정리 |
| `incident-timeline-visual.md` | Mermaid 형식의 시각화 |
| `follow-up-checklist.md` | 교사가 추가 확인해야 할 목록 |
| `admin-report-draft.md` | 관리자 보고용 초안 |
| `teacher-review-checklist.md` | 공유·보고 전 교사 검토 체크리스트 |

교사가 `사안종료`라고 말하면 NEIS 정리 단계로 전환해 다음 파일을 만듭니다.

```text
neis-student-log-draft.md
neis-entry-review-checklist.md
```

NEIS 초안은 다음 기준으로 정리됩니다.

- 학생별로 분리
- 날짜별로 분리
- 시간대별로 분리
- 다른 학생의 불필요한 민감 진술 제거
- 사실, 진술, 교사 조치, 확인 필요 사항 구분
- NEIS 자동 입력 금지

## `사안종료`의 의미

`사안종료`는 법적·행정적 종결을 뜻하지 않습니다.

이 Skill에서 `사안종료`는 다음 뜻입니다.

> 지금까지 이 대화창과 작업 폴더에 정리된 자료를 바탕으로, 교사가 NEIS에 직접 입력하기 쉽게 학생별 누가기록 초안을 만들어 달라는 작업 전환 신호

따라서 `사안종료` 이후에도 교사는 학교 기준, 관리자 확인, NEIS 기재 기준에 따라 문구를 검토해야 합니다.

## 예시 결과물

NEIS 누가기록 초안은 다음과 같은 형식으로 만들어집니다.

```md
# NEIS Student Log Draft

## 학생A

| Date | Time | Record Type | Draft Text | Source | Review Needed |
|---|---|---|---|---|---|
| 더미일자1 | 2교시 후 | 상담·생활지도 | 복도에서 학생B와 말다툼이 있었다는 교사 관찰 기록이 있어 학생A의 진술을 분리해 청취함. 학생A는 상대가 먼저 놀렸다고 진술함. 추가 확인 필요. | raw/dummy-note.md | NEIS 기재 기준과 관리자 확인 필요 |
```

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

이 저장소에는 빈 템플릿과 더미 예시만 포함되어야 합니다.

공개 GitHub 저장소에 올리면 안 되는 자료:

- 실제 학생 기록
- 실제 학교 매뉴얼 중 재배포가 허용되지 않은 파일
- 내부 공문
- 상담 기록
- 녹취록
- 음성파일
- NEIS 기록
- 이름, 연락처, 학번, 주소, 학교명 등 개인정보

## 더미 예시

`examples/dummy-project/`에는 실제 자료가 아닌 가상 예시가 들어 있습니다. 구조와 출력 형식을 이해하기 위한 샘플이며, 실제 학생 기록이 아닙니다.

## 라이선스

MIT License.
