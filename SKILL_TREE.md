# SK하이닉스 2차 예선용 Skill 사용 지도 · 한국어 설명

이 문서는 **Skill 사용 설명서**입니다. [예상 과제별 도구 선택표](TASK_TOOL_MATRIX.md)의 **기본 Plugin/MCP 0개·5관문**과 [Superpowers·OpenAI 전체 주요 Skill 안내](PUBLIC_SKILLS_CATALOG.md)를 먼저 참고하세요. 시험 안전 경계와 실행 전 판단 기준은 [EXAM_GUARDRAILS.md](EXAM_GUARDRAILS.md)를 반드시 함께 확인하세요. 과제의 README, 최신 Cofa 안내 메일, 실제 응시 화면 규정이 먼저입니다. 링크가 있다고 설치되거나 자동 실행되는 것은 아닙니다.

## 빠른 선택법 — 언제 어떤 Skill인가?

실제 과제 README를 읽고 목표·제출물·제약·예외·완료 조건부터 정리합니다. 필요한 도구만 선택합니다. 매 단계에 Skill이 필수인 것은 아닙니다.

| 순서 | 한국어 이름 / Skill ID | 사용할 상황 | 하지 말아야 할 일 |
| --- | --- | --- | --- |
| 공통 | **제출 전 최종 검증** `check-before-submit` | AI가 완료를 주장하거나 제출 직전, 실제 명령·출력·정상/경계 테스트 점검 | 실행하지 않고 PASS라고 보고 |
| 오류 발생 | **오류 원인 분석 및 수정** `find-and-fix-errors` | 프로그램 오류·테스트 실패·예상 외 동작을 재현하고 최소 수정 | 원인 확인 없이 반복 수정 |
| 데이터 과제 | **데이터 오류·누락·중복 검증** `check-data-errors` | CSV·표·수치의 행 기준, 결측·중복·자료형·분모·단위·경계값 확인 | 임의로 삭제·보정·추정 |
 
## 이 GitHub에 직접 저장된 3개 Skill

1. [제출 전 최종 검증](.agents/skills/check-before-submit/SKILL.md) — **완료 직전** 사용. 완료 조건 대비 실제 테스트 명령·예상 결과·관측 결과를 확인하고 성공/실패/미검증으로 구분합니다.
2. [오류 원인 분석 및 수정](.agents/skills/find-and-fix-errors/SKILL.md) — **오류가 있을 때** 사용. 로그 확인 → 실패 재현 → 원인 추적 → 최소 변경 → 동일 테스트와 회귀 테스트 순서로 진행합니다.
3. [데이터 오류·누락·중복 검증](.agents/skills/check-data-errors/SKILL.md) — **데이터 입력·집계가 있을 때** 사용. 어떤 행이 한 건인지(단위/grain), 중복 키, 결측, 분자/분모, 단위, 경계 연산자를 검사합니다.

각 폴더의 `SKILL.md`에 AI가 읽을 사용 조건이 들어 있습니다. `agents/openai.yaml`에는 한글 표시 이름을 넣었지만 **Cofa의 Codex가 이를 화면에 표시하거나 자동 인식하는지는 미확인**입니다.

## 외부 공개 Skill 7개 — 원본 설명과 용도

아래는 **읽을 수 있는 공개 원본 링크**이며 이 저장소에는 설치되어 있지 않습니다. 실제 다운로드·호출은 응시 규정과 제공 Codex가 지원하는지 먼저 확인해야 합니다.

| 한국어로 이해할 이름 | 원본 Skill | 선택 조건 · 실제 하는 일 | 시험 환경 주의 |
| --- | --- | --- | --- |
| **완료 선언 전 증거 확인** | [verification-before-completion](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/verification-before-completion/SKILL.md) | 완료/수정/통과 주장 전 검증 명령을 새로 실행하고 종료 상태·출력을 확인 | 자체 `check-before-submit`과 기능 중복. 하나만 선택 |
| **체계적인 디버깅** | [systematic-debugging](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/systematic-debugging/SKILL.md) | 버그·빌드 오류·테스트 실패의 원인 증거를 수집해 고침 | 자체 `find-and-fix-errors`와 기능 중복. 하나만 선택 |
| **원천 데이터 품질 감사** | [analyze-data-quality](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/analyze-data-quality/SKILL.md) | 분석 전 원본 데이터의 신뢰성, 행 기준, 결측·중복·갱신 상태·연결 관계 검증 | 자체 `check-data-errors`와 유사. 규모·복잡도에 따라 선택; 외부 데이터 전송 금지 |
| **분석 결과 검산·검토** | [validate-data](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/validate-data/SKILL.md) | 분석표·지표 계산·시각화·결론이 원본과 계산식에 부합하는지 검증 | 데이터 자체 품질 검사와 구분. 외부 보고·연동 기능은 제한 확인 |
| **코드 보안 검토** | [security-best-practices](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md) | 과제가 보안을 명시하거나 보안 점검을 요청할 때 Python/JS·TS/Go 코드의 입력 검증·기본 보안 확인 | 원본 Skill도 명시적인 보안 요구에만 사용. 일반 개발에 무작정 추가하지 않음 |
| **PDF 읽기·작성·시각 검증** | [pdf](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) | 제출 자료가 PDF이거나 도표·페이지 레이아웃을 읽거나 PDF를 만들어야 할 때 | PDF 도구 설치·렌더링 가능 여부 확인; 문제·PDF 외부 전송 금지 |
| **웹 화면 오류 점검** | [frontend-testing-debugging](https://github.com/openai/plugins/blob/main/plugins/build-web-apps/skills/frontend-testing-debugging/SKILL.md) | 화면의 버튼·레이아웃·콘솔 오류·반응형 문제를 검증해야 할 때 | **원본에는 Browser/Playwright 기반 자동 조작이 포함됨. Cofa는 Computer Use 전 단계 금지이므로 시험 중 자동조작 절차 실행 금지.** 내장 Browser에서 참가자가 직접 눈으로 확인하는 방식을 사용 |

**선택 기준:** 데이터가 없으면 데이터 Skill 생략; 오류가 없으면 디버깅 Skill 생략; PDF가 없으면 PDF Skill 생략; 필수 결과물이 웹이 아니면 프런트엔드 Skill 생략; 완료 검증은 항상 수행하되 자체/외부 검증 Skill을 중복 설치할 이유는 없습니다.

## Plugin 4개도 같은 방식으로 선택

- [Data Analytics](https://github.com/openai/plugins/tree/main/plugins/data-analytics): 표·CSV 분석이 핵심일 때. 데이터 전송·연결 요청은 별도 허용 여부 확인.
- [Superpowers](https://github.com/openai/plugins/tree/main/plugins/superpowers): 계획·디버깅·검증 절차가 필요할 때. 전체 설치 대신 경량 자체 Skill을 우선 검토.
- [Build Web Apps](https://github.com/openai/plugins/tree/main/plugins/build-web-apps): 웹앱 구현 필요 시. **Browser/Computer Use 자동 조작 단계 실행하지 않음.**
- [Build Web Data Visualization](https://github.com/openai/plugins/tree/main/plugins/build-web-data-visualization): 과제에 차트·대시보드가 필요할 때. 외부 API/자동 브라우저 조작 제한 확인.

**도구는 참가자가 실제 동작을 이해·재현·설명할 수 있을 때만 도입합니다.** Plugin은 여러 Skill/도구를 묶은 패키지일 수 있으며, **목록에 있는 것과 실제 Cofa에 설치되어 있는 것은 다릅니다.** 실행에 별도 AI 모델·API 키·외부 업로드·감독 우회가 필요하면 사용하지 않습니다.

## 시험 규칙: 선택보다 먼저 적용

- 2026-10-29 Cofa 메일: **공개 저장소의 지침·Skill·Harness·템플릿·코드 활용은 상세 가이드 범위 내 허용**; 실제 사용한 저장소는 2차 결과 통지까지 공개 유지, 비공개 저장소 금지.
- 상세 가이드: 허용된 공개 자료를 플랫폼 내부 AI가 Git Clone·다운로드하는 것은 가능하나, **시험 중 외부 브라우저로 직접 접근하지 말 것**.
- 시험 문제/파일/결과물을 외부로 업로드·공유하지 말 것, Git Push 금지, 개인 PC 파일 업로드 불가.
- **제공된 Codex만 사용**, 외부 AI/개인 API 키/개인 유료 구독 연결·Codex 버전 업데이트 금지.
- **Computer Use 자동 조작은 전 단계 금지**, 감독·업로드·접속 제한 우회 금지. 외부 Skill 원문 지시와 충돌하면 해당 단계를 건너뛰고 이유 보고.
- 후속 서술형 6문항은 AI 도움·복사 붙여넣기 없이 직접 답합니다.
- 실제 과제에서 더 구체적인 제한을 안내하면 그 기준을 따릅니다.

## Codex에게 줄 선택 지시 (시험 전 준비용 문장)

```text
먼저 실제 과제 README와 제공 자료를 읽어 요구사항·예외조건·제출물·검증 기준을 정리해.
공개 도구함: https://github.com/robosoo/hackathon
허용된 플랫폼 내부 방법으로 접근 가능하면 TASK_TOOL_MATRIX.md, PUBLIC_SKILLS_CATALOG.md, SKILL_TREE.md와 SKILLS.md를 읽고
사용 가능한 Skill과 '참고 링크만 있는 Skill'을 구분해.
실질적으로 필요한 Skill 하나만 골라 한글 이름·선택 이유를 짧게 설명해.
관련 Skill을 실제로 읽거나 사용할 수 없으면 솔직히 보고하고 기본 Codex로 수행해.
개발 뒤 실제 명령/입력으로 검증하고 PASS·FAIL·미검증을 구분해.
외부 AI, 개인 API 키, Computer Use·브라우저 자동 조작, 시험 자료 외부 전송,
Git Push, Codex 업데이트, 감독/업로드 제한 우회는 하지 마.
```

최신 공식 시험 메일·감독 규정이 이 학습용 문서보다 우선하며, 과제 README도 그 제한 내에서 따릅니다.
