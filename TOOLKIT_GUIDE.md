# AI 과제 해결용 공개 도구함

참가자가 **먼저 실제 과제를 이해하고 해결 방향을 정한 다음**, Codex가 전체 문제 해결 흐름을 따라 필요한 Skill만 선택해 구현·검증하도록 돕는 비공식 공개 학습 자료입니다. 전체 작업 태도·역할 분담·절차는 [EXAM_WORKFLOW.md](EXAM_WORKFLOW.md)에 정리했습니다.

## 사용

시험장 Codex에 **이 저장소의 [START_PROMPT.md](START_PROMPT.md)를 읽으라고 지시**합니다. **실제 시험 과제의 `README.md`와 이 도구함의 `TOOLKIT_GUIDE.md`는 서로 다른 파일입니다.** 실제 과제 지시서를 먼저 확인합니다.

1. Codex가 **실제 과제 README와 제공 자료를 직접 읽음**.
2. 참가자가 직접 문제를 파악하고 해결 방향을 정할 동안 Codex는 **문제 풀이를 시작하지 않고 대기**.
3. 참가자가 자신의 문제 이해·풀이 방향을 밝히고 진행을 요청하면 Codex는 **[EXAM_WORKFLOW.md](EXAM_WORKFLOW.md)를 읽어 Understand → Analyze → Clarify → Plan → Build → Verify → Deliver 흐름을 적용**하고, 필요한 Skill만 선택해 분석·구현·테스트하며 선택 이유와 확인된 증거를 보고.
4. 중요한 판단·수동 화면 확인·최종 제출은 참가자가 직접 수행.

## 적은 컨텍스트로 사용하기

| 문서 | 역할 |
| --- | --- |
| [START_PROMPT.md](START_PROMPT.md) | **짧은 시작 지침** |
| [AGENTS.md](AGENTS.md) | **작업별 참고자료 안내판** |
| [EXAM_WORKFLOW.md](EXAM_WORKFLOW.md) | **참가자 주도 문제 해결 원칙·역할·7단계 흐름·예시 프롬프트** — 참가자가 문제를 이해한 이후 참조 |
| [SAFETY.md](SAFETY.md) | 공통 시험 안전 제한 |
| [COFA_EVIDENCE_PLAYBOOK.md](COFA_EVIDENCE_PLAYBOOK.md) | **선택적 참고:** Cofa 인터뷰·자체 교재·공개 GitHub를 교차 검토한 실전 교훈과 근거 |
| [SKILLS.md](SKILLS.md) / [PLUGINS.md](PLUGINS.md) | 외부 도구가 정말 필요할 때만 |
| [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) | 작업 유형별 도구 판단이 필요할 때만 |
| [.agents/skills](.agents/skills) | 자체 Skill 5개: 요구사항, 데이터 검증, 디버깅, 결정 기록, 제출 전 점검 |

기본적으로 **START_PROMPT → AGENTS + SAFETY까지만 읽고**, 참가자가 스스로 이해하고 진행을 요청하면 **EXAM_WORKFLOW**를 읽습니다. **필수 요구사항을 만족하는 단순한 구현을 우선하며 과설계를 피합니다.** 이후 세부 Skill은 실제 작업에 해당할 때만 읽습니다. 여러 문서를 한 번에 주입하거나, 공개 Skill·Plugin을 무조건 설치하지 않습니다. **판단 근거 기록용 `decision-log`는 선택 사항**이며, 실제 과제의 로컬 작업공간에서만 기록하고 공개 저장소에는 시험 자료·기록을 올리지 않습니다. 외부 Plugin/MCP/별도 Harness는 **기본 0개**입니다.

기존 자체 브레인스토밍 Skill은 [Superpowers `brainstorming` 원본](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md)에서 문제 정의의 기본 접근을 참고한 **별도 경량 지침**이며, 원본 전체 도구가 설치된 것은 아닙니다.

`.gitignore`는 파일을 새로 추적하지 않게 하는 Git 설정일 뿐 AI의 파일 읽기를 막지 않습니다. **공개 시험용 도구함에서는 `AGENTS.md`를 계속 공개·관리**합니다. 시험 자료·응시 결과는 이 저장소에 올리지 않습니다.

**시험 당일 추가 공지·최신 운영팀 메일·실제 과제 README·공식 가이드가 이 도구함보다 우선**이며, 문서나 Skill 사용 자체의 가점·감점은 보장되지 않습니다. 사용한 공개 저장소는 2차 예선 결과 통지 전까지 공개로 유지하고, 시험 자료·코드·결과의 외부 전송과 Git Push는 하지 않습니다.
