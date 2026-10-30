# 상황별 Skill 선택 지도

**시작 방법:** [START_PROMPT.md](START_PROMPT.md) · 안전 규칙: [SAFETY.md](SAFETY.md) · 문제 해결 전체 절차: [EXAM_WORKFLOW.md](EXAM_WORKFLOW.md).

참가자의 문제 해석과 진행 요청을 받은 뒤, **실제 문제·현재 막힌 지점·다음 행동**을 기준으로 아래에서 필요한 문서만 읽는다. 단순 작업에는 Skill이 필요하지 않다. 링크를 읽었다고 Skill·Plugin이 자동 설치되거나 실행되는 것은 아니다.

| 발생한 상황 | 읽을 문서(필요한 경우만) |
| --- | --- |
| 모호한 요구·업무 질문·설계 선택 | [brainstorm-requirements](.agents/skills/brainstorm-requirements/SKILL.md) |
| CSV·데이터 품질·Join·집계 문제 | [check-data-errors](.agents/skills/check-data-errors/SKILL.md) |
| 실행 오류·테스트 실패 | [find-and-fix-errors](.agents/skills/find-and-fix-errors/SKILL.md) |
| 중요한 결정·현직자 답변·검증 기록 | [decision-log](.agents/skills/decision-log/SKILL.md) |
| 실제 결과 확인·제출 전 점검 | [check-before-submit](.agents/skills/check-before-submit/SKILL.md) |
| 구현 도구 선택이 특히 어려움 | [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) |
| 위 기능으로 해결이 안 돼 공개 참고 지침이 필요함 | [SKILLS.md](SKILLS.md) · [PLUGINS.md](PLUGINS.md) |

업무 규칙에 답이 없으면 Codex가 질문을 **제안**하고 참가자가 현직자 AI에게 확인한다. **과설계 없이 최소한으로 구현하고, 확인한 실행 결과를 짧게 보고**한다. 작업·외부 연결 제한은 `SAFETY.md`를 따른다.
