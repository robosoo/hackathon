# 작업 흐름별 참조 지도

이 파일은 **긴 시스템 프롬프트가 아니라 필요한 문서를 찾는 안내판**이다. 시험 과제 README·최신 공식 규정이 우선이며, `SAFETY.md`는 항상 적용한다.

**시작:** 실제 시험 README·자료는 Codex가 직접 읽되, 참가자가 스스로 이해하고 방향을 제시할 때까지 **해석·브레인스토밍·코딩하지 않는다.** 사용자의 진행 요청 이후에만 해당 경로를 선택한다.

| 상황 | 필요한 경우에만 읽을 자료 |
| --- | --- |
| 공통 금지행동·제한 | [SAFETY.md](SAFETY.md) |
| 참가자가 아이디어·요구사항 검토 요청 | [.agents/skills/brainstorm-requirements/SKILL.md](.agents/skills/brainstorm-requirements/SKILL.md) |
| 참가자가 구현을 지시하고 도구 선택이 필요 | [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) |
| 실제 실행 오류·테스트 실패 | [.agents/skills/find-and-fix-errors/SKILL.md](.agents/skills/find-and-fix-errors/SKILL.md) |
| CSV·데이터 결측·중복·집계 오류 | [.agents/skills/check-data-errors/SKILL.md](.agents/skills/check-data-errors/SKILL.md) |
| 완료 주장·제출 전 검증 | [.agents/skills/check-before-submit/SKILL.md](.agents/skills/check-before-submit/SKILL.md) |
| 외부 Skill·Plugin이 정말 필요 | [SKILLS.md](SKILLS.md), [PLUGINS.md](PLUGINS.md) |

**작업 규칙:** 필요한 행의 파일만 열고, 서로 겹치는 Skill을 동시에 사용하지 않는다. 외부 Plugin/MCP/별도 Harness는 기본 **0개**다. 자료 링크를 읽었다고 Skill이 자동 설치된 것은 아니다. **선택한 이유를 한 줄로 보고하고**, 검증한 실행 결과와 미검증 항목을 구분한다. 참가자 승인 전 분석 금지, 자료 외부 반출 금지 등은 `START_PROMPT.md`·`SAFETY.md`를 따른다.

여기 연결된 Skill은 공개 작업 지침이며 시험 문제나 답안을 사전에 담아두지 않는다. 별도의 DB 동기화나 Git Push 절차는 포함하지 않는다.
