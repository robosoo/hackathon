# 비공식 예상 과제별 도구 선택표 — 검증 가능한 최소 구성

**기준:** 2026 SK하이닉스 AI 해커톤 2차 Cofa Probe 대비용 학습 자료. **실제 기출·확정 출제 유형·공식 점수/감점표가 아닙니다.** 2026-10-29 운영팀 메일·제공 가이드가 출처이며, 시험 당일 새 공지·실제 과제 README가 우선합니다.

**기본값: 제공 Codex + 필요시 자체 경량 Skill. 외부 Plugin 0개, MCP 0개, 별도 Harness 0개.** 설치는 실력의 증거가 아닙니다. 직접 테스트·설명하지 못하는 기능은 MVP 필수 흐름에 넣지 않습니다.

## 도구 도입 전 5관문 — 하나라도 아니면 생략

| 관문 | 응시자가 확인할 것 | 불통과 시 |
| --- | --- | --- |
| 규정 적합 | 최신 공식 규정상 허용? 외부 전송·외부 AI·Git Push·Computer Use·감독 우회 없음? | 해당 도구/명령 중단 |
| 필요성 | 실제 README의 필수 기능에 필요한가? 기본 Codex로 부족한가? | 기본 Codex 유지 |
| 이해 | 설치 지침·실행 동작·외부 접속·권한·비용·의존성을 파악했나? | 도입 보류 |
| 재현 검증 | 내가 **입력→예상 결과→실제 결과**를 직접 확인할 수 있나? | 필수 기능에서 제외 |
| 자기 설명 | 사후 질문에서 채택 이유·수정 범위·한계·실패 대응을 내 말로 말할 수 있나? | 더 단순한 방법으로 변경 |

**주의:** 공식 안내는 허용된 AI 활용 과정과 사용량 등을 평가에 활용할 수 있다고 설명하지만, Plugin 개수별 감점·Skill 사용 가산점·특정 개발 방식의 점수는 **공식 확인되지 않았습니다.** 설치 비용·복잡성·재검증 부담을 줄이는 것은 **우리의 리스크 관리 원칙**입니다.

## 예상 연습 과제별 추천 (기출 아님)

| 가상의 과제 유형 | 기본 Codex로 할 일 | 해당할 때만 읽을 Skill / 후보 Plugin | 내가 실제로 확인할 결과 | 생략/금지 |
| --- | --- | --- | --- | --- |
| 요구사항이 모호한 현업 요청 | Cofa **업무 담당자**에게 입력·출력·업무 규칙·완료 기준 질문 | [Superpowers brainstorming](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md) 핵심 질문법 *참고만*; 자체 `check-before-submit` | 질문/답을 근거로 필수·선택·미정 요구사항 설명 | 복잡한 자동 Harness, 무한 질문 |
| 접수·승인·수정 **업무 웹앱** | 작은 HTML/JS로 첫 핵심 흐름 구현 | 자체 `check-before-submit`; [Build Web Apps](https://github.com/openai/plugins/tree/main/plugins/build-web-apps) 중 `frontend-app-builder`는 **자동 Browser 테스트를 제거하고 수동으로 검증할 수 있을 때만 참고** | 직접 등록→수정→저장→재확인, 정상/빈 입력 | Playwright/Selenium/Browser 자동 조작, 외부 DB·배포 강제 |
| CSV/JSON/Excel 정리 | 한 행의 의미, 고유 키, 결측, 중복, 단위, 기간·분자/분모 정리 | 자체 `check-data-errors`; 복잡할 때만 [analyze-data-quality](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/analyze-data-quality/SKILL.md) | 원본 행수·중복/누락 건수, 일부 손계산 대조 | 파일 외부 전송·연결된 원격 창고 |
| 불량률·지표·수치 보고서 | 정의·계산식·필터·집계 결과 구현 | [validate-data](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/validate-data/SKILL.md) *지침 참고* | 기대값과 실제값, 분모 0·경계값·중복 사례 | 근거 없는 AI 숫자·해석 |
| 차트·대시보드 | 기본 표·필수 차트·필터만 구현 | [Build Web Data Visualization](https://github.com/openai/plugins/tree/main/plugins/build-web-data-visualization) *시각화가 진짜 필수일 때만* | 원본 집계와 차트 수치/축/단위 일치, 화면 직접 점검 | 외부 클라우드 배포, 과도한 프레임워크 |
| PDF 분석·문서 생성 | 과제에서 요구한 페이지·표·출력만 구현 | [OpenAI pdf](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) | 출력 PDF를 열어 숫자·표·레이아웃 대조 | 원본 PDF 외부 업로드 |
| 버그·빌드 실패 | 로그 읽기→같은 오류 재현→최소 수정→재실행 | 자체 `find-and-fix-errors` 또는 [systematic-debugging](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/systematic-debugging/SKILL.md) 중 **하나만** | 같은 실패가 사라지는지·기존 정상 흐름 유지 | 원인 없는 반복 수정·자동 UI 조작 |
| 사용자 입력 검증·보안 요구 | 입력·권한·오류 응답을 최소 구현 | [security-best-practices](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md) *보안 요구가 명시된 경우에만* | 잘못된 입력 차단·비밀값 비노출 | 별도 보안 서버/API 연결 |
| 단순 스크립트·파일 변환 | 파일 읽기, 작은 스크립트 작성·실행 | 보통 외부 도구 불필요, 자체 `check-before-submit` | 동일 입력 재실행 결과와 파일 위치 | 새 프레임워크/Plugin 설치 |
| 제출 후 서술형 6문항 | **AI 사용 종료**, 본인이 직접 작성 | **사용할 Skill·Plugin·MCP 없음** | 선택 이유·검증·한계를 스스로 설명 | AI 답변 생성·입력·붙여넣기 |

**Skill/Plugin 링크는 참고 출처**일 뿐 설치나 Cofa 호환을 뜻하지 않습니다. 개별 Skill 원문의 금지 동작은 따르지 않습니다. [세부 공개 Skill 목록](PUBLIC_SKILLS_CATALOG.md), [MCP 판단 기준](MCP_GUIDE.md), [규칙 보호장치](EXAM_GUARDRAILS.md)를 함께 확인합니다.

## 왜 도구를 많이 설치하지 않는가?

- 제공 Codex는 **과제 작업 공간의 파일 읽기/쓰기, 허용된 터미널 명령, 로컬 테스트·개발 서버 작업**을 수행할 수 있습니다. 외부 filesystem MCP 없이도 되는 작업을 중복 연결하지 않습니다.
- 자체 Skill 세 개는 순서/검증을 안내하는 **짧은 매뉴얼**입니다. 실제로 파일을 읽어야 적용됩니다. 링크를 붙여 넣었다고 자동 설치되지 않습니다.
- 외부 Plugin은 Browser 자동화·하위 에이전트·Git 워크플로·원격 API 등 불필요하거나 금지된 동작이 섞일 수 있습니다.
- 별도 Harness는 필수가 아닙니다. `START_PROMPT.md` + `EXAM_GUARDRAILS.md` + `WORKFLOW.md`로 **경량 규칙과 검증 흐름**을 구성합니다.
- Cofa **업무 담당자**는 업무 요구 확인, **Cofa Helper**는 시험 시스템 조작 문의, **내장 Browser**는 참가자 **직접 조작**에 사용합니다.

## Codex에 전달할 요약 지시

```text
실제 과제 README의 필수 요구·자료·예외·제출물을 먼저 확인해.
TASK_TOOL_MATRIX.md의 5관문을 적용하고 Plugin/MCP/별도 Harness 기본 설치 0개로 시작해.
필요하면 PUBLIC_SKILLS_CATALOG.md에서 관련 Skill 원문을 1개만 선택해.
내가 이해·재현·설명할 수 없거나 규정 위반 위험이 있는 도구는 쓰지 마.
최소 기능을 실행·검증하고 PASS/FAIL/미검증을 실제 근거로만 보고해.
```
