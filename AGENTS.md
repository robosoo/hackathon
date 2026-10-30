# 작업 흐름별 참조 지도

이 파일은 **긴 시스템 프롬프트가 아니라 필요한 문서를 찾는 안내판**이다. 전체 해결 태도·역할·단계 전환은 [EXAM_WORKFLOW.md](EXAM_WORKFLOW.md)에 있고, 세부 작업은 아래 Skill에서 필요한 것만 선택한다. 시험 과제 README·최신 공식 규정이 우선이며, `SAFETY.md`는 항상 적용한다.

**시작:** 실제 과제와 참고자료의 경로를 먼저 확인한다. 참가자가 스스로 문제를 읽고 방향을 정하기 전에는 문제 풀이·코딩을 시작하지 않되, **참가자가 묻는 용어·파일·자료 설명에는 응답할 수 있다.** 진행 요청을 받으면 [EXAM_WORKFLOW.md](EXAM_WORKFLOW.md)를 읽고 **현재 상황에서 가장 필요한 작업**을 수행한다. 단계 순서·Skill 실행을 의무로 만들지 않는다. 중요한 미확정 업무 규칙만 질문 후보를 제시하고, 확정된 부분은 구현·검증한다.

| 상황 | 필요한 경우에만 읽을 자료 |
| --- | --- |
| 공통 금지행동·제한 | [SAFETY.md](SAFETY.md) |
| **참가자가 풀이 방향을 제시한 이후: 전체 문제 해결 태도·협업·단계 전환** | **[EXAM_WORKFLOW.md](EXAM_WORKFLOW.md)** |
| 참가자가 아이디어·요구사항 검토 요청 | [.agents/skills/brainstorm-requirements/SKILL.md](.agents/skills/brainstorm-requirements/SKILL.md) |
| 참가자가 구현을 지시하고 도구 선택이 필요 | [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) |
| 실제 실행 오류·테스트 실패 | [.agents/skills/find-and-fix-errors/SKILL.md](.agents/skills/find-and-fix-errors/SKILL.md) |
| CSV·데이터 결측·중복·집계 오류 | [.agents/skills/check-data-errors/SKILL.md](.agents/skills/check-data-errors/SKILL.md) |
| 참가자가 작업 현황·주요 판단·담당자 답변·검증 근거의 기록을 요청 | [.agents/skills/decision-log/SKILL.md](.agents/skills/decision-log/SKILL.md) |
| 완료 주장·제출 전 검증 | [.agents/skills/check-before-submit/SKILL.md](.agents/skills/check-before-submit/SKILL.md) |
| 외부 Skill·Plugin이 정말 필요 | [SKILLS.md](SKILLS.md), [PLUGINS.md](PLUGINS.md) |

**작업 규칙:** 우선 **실제 문제·현재 상태·다음 행동**을 판단한다. `EXAM_WORKFLOW.md`는 유연한 체크포인트로 쓰고, 세부 Skill은 현재 문제 해결에 실질적으로 도움이 되는 경우에만 해당 파일을 읽는다. 간단한 작업에는 Skill을 사용하지 않아도 된다. 필요성이 바뀌면 다른 Skill로 전환할 수 있으나 겹치는 지침을 무더기로 실행하지 않는다. 업무 담당자 AI에게는 참가자가 직접 질문하며 Codex는 질문 후보와 답변 해석만 지원한다. 외부 Plugin/MCP/별도 Harness는 기본 **0개**다. **자동 설치·연결·외부 통신·외부 스크립트 자동 실행은 하지 않는다.** 필요한 경우 과제 필수성·공식 허용 범위·데이터 이동을 참가자가 확인한 뒤에만 검토한다. 자료 링크를 읽었다고 Skill이 자동 설치된 것은 아니다. 의사결정 기록은 필요한 경우에만 **실제 과제의 허용된 로컬 작업공간**에 남기며 공개 도구함으로 전송하지 않는다. **선택한 이유를 한 줄로 보고하고**, 검증한 실행 결과와 미검증 항목을 구분한다. 참가자 승인 전 분석 금지, 자료 외부 반출 금지 등은 `START_PROMPT.md`·`SAFETY.md`를 따른다.

여기 연결된 Skill은 공개 작업 지침이며 시험 문제나 답안을 사전에 담아두지 않는다. 별도의 DB 동기화나 Git Push 절차는 포함하지 않는다.
