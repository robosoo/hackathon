# 공개 Skill 추천 목록

**Skill = AI에게 특정 업무를 수행하는 방법을 알려주는 매뉴얼.** 아래는 원본 저장소의 출처 링크입니다. **목록을 저장한 것만으로 설치되지 않습니다.** 공개된 Skill이라고 해서 Cofa의 모든 사용 방법이 승인되는 것도 아닙니다.

## 추천 7개 — 문제를 보고 필요한 것만 선택

| 우선 | Skill · 원본 | 사용 상황 | 사용 전 확인 |
| --- | --- | --- | --- |
| 1 | [verification-before-completion](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/verification-before-completion/SKILL.md) | 완료 전 실행·테스트 결과 확인 | 최신 실행 증거 없으면 완료 주장 금지 |
| 2 | [systematic-debugging](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/systematic-debugging/SKILL.md) | 코드 오류·테스트 실패 원인 분석 | 원인 확인 없이 수정 반복 금지 |
| 3 | [analyze-data-quality](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/analyze-data-quality/SKILL.md) | CSV/표/수치 분석에서 누락·중복·스키마 오류 | 파일과 데이터의 출처·유효성 확인 |
| 4 | [validate-data](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/validate-data/SKILL.md) | 계산·비율·보고서 검증 | 자료와 계산식 독립 점검 |
| 5 | [security-best-practices](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md) | 입력 검증, 코드 보안, 노출 위험 | 과제 언어·범위를 충족할 때만 |
| 6 | [pdf](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) | PDF 읽기·편집·보고서 작업 | 과제에 PDF가 있을 때만 |
| 7 | [frontend-testing-debugging](https://github.com/openai/plugins/blob/main/plugins/build-web-apps/skills/frontend-testing-debugging/SKILL.md) | 웹 앱 화면·버튼·실행 오류 점검 | **Browser/Playwright 자동 조작 절차는 시험 금지. 내장 Browser에서 직접 확인** |

첫 선택은 **완료 검증**, 오류가 나면 **디버깅**, 데이터 과제일 때 **데이터 품질**입니다. 나머지는 실제 과제에 필요할 때만.

전체 Superpowers·OpenAI Skill 후보와 제외 이유는 [PUBLIC_SKILLS_CATALOG.md](PUBLIC_SKILLS_CATALOG.md)에 있습니다. 과제별 선택은 [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md)에서 확인하세요.

사용 조건을 더 자세하게 정리한 [**한글 Skill 선택 지도(SKILL_TREE.md)**](SKILL_TREE.md)를 함께 읽으세요.

## 이 저장소에 직접 작성한 경량 Skill 3개

외부 원문을 그대로 복사하지 않고, 누구나 읽을 수 있는 한국어 작업 지침으로 직접 구성한 학습용 파일입니다.

- [제출 전 최종 검증 · check-before-submit](.agents/skills/check-before-submit/SKILL.md) — 완료 전 실제 실행 결과 확인
- [오류 원인 분석 및 수정 · find-and-fix-errors](.agents/skills/find-and-fix-errors/SKILL.md) — 오류 재현·원인 추적·재검증
- [데이터 오류·누락·중복 검증 · check-data-errors](.agents/skills/check-data-errors/SKILL.md) — 데이터 누락·중복·분모·경계값 검사

모두 `SKILL.md` 형식을 따르지만, **Cofa Codex가 이 저장소의 Skill을 자동 탐색한다는 보장은 없습니다.** 지원하지 않는 환경이면 [START_PROMPT.md](START_PROMPT.md)를 자연어로 입력해 같은 원칙을 적용하세요.

## 외부 Skill과 출처

- [OpenAI Plugins 저장소](https://github.com/openai/plugins) — 여러 제작자의 Plugin과 Skill을 제공하는 공개 배포 장소입니다. 저장소에 있다고 해서 OpenAI 직접 제작이라는 뜻은 아닙니다.
- [OpenAI 기존 Skills 저장소](https://github.com/openai/skills) — 기존 curated Skill 원문입니다. 해당 프로젝트의 현재 안내·유지보수 상태를 별도 확인하세요.
- 각 Skill의 실행 스크립트나 연계 MCP가 별도 서비스·API 키·네트워크·브라우저 자동화를 요구하면 **시험 상세 규정을 먼저 확인**하세요.

**주의:** 공개 저장소의 원본을 참고한다고 시험 문제·제출 결과물을 GitHub에 보낼 수 있는 것은 아닙니다.
