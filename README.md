# AI 과제 해결용 공개 도구함

실제 과제의 요구사항을 파악하고, **필요한 Skill만 선택하여 결과를 재현·검증**하기 위한 공개 학습용 지침입니다. 공식 대회 지침·기출·완성 답안은 아닙니다.

## 시작하기 — 아래 두 문장만 입력

```text
실제 시험 과제의 README를 먼저 읽고 요구사항과 제한사항을 확인해.

그다음 공개 GitHub 저장소 https://github.com/robosoo/hackathon 에 허용된 방법으로 접근하여 START_PROMPT.md를 실제로 읽고, 해당 지침에 따라 과제 분석부터 구현·검증까지 진행해.
```

**중요:** Codex가 실제로 `START_PROMPT.md`를 읽어야 지침을 적용할 수 있습니다. URL만 전달해서 Skill이나 Plugin이 자동 설치되는 것은 아닙니다. 접근할 수 없으면 그 사실을 보고하고 실제 과제 README와 기본 Codex로 계속하도록 지시되어 있습니다.

## 구성

| 파일 | 목적 |
| --- | --- |
| [START_PROMPT.md](START_PROMPT.md) | **실전 진행:** 문제 파악 → 브레인스토밍 → 구현 → 검증 |
| [SKILLS.md](SKILLS.md) | 겹치지 않는 자체 Skill 4개와 공개 Skill 원본 참고 |
| [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) | 실제 요구에 따라 도구를 최소 선택 |
| [PLUGINS.md](PLUGINS.md) | 설치 없이도 가능한 작업과 Plugin 후보 비교 |
| [SAFETY.md](SAFETY.md) | 핵심 금지행동·자료 보호·우선순위 |
| [AGENTS.md](AGENTS.md) | 이 저장소를 읽은 에이전트용 간단 안내 |
| [.agents/skills](.agents/skills) | 이 저장소에서 직접 작성한 Skill 4개 |

**Superpowers 활용:** 공개 [`brainstorming` 원본](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md)의 **문제 맥락 확인·대안 비교·성공 기준 정의**를 참고하여 [시험용 경량 브레인스토밍 Skill](.agents/skills/brainstorm-requirements/SKILL.md)을 별도로 작성했습니다. 원본을 그대로 복사하거나 공식 Superpowers Skill을 설치한 것은 아닙니다. 원본의 강제 승인·자동 브라우저 보조·Git 커밋 절차는 가져오지 않았습니다.

추가 Plugin·MCP·외부 Harness는 **기본 0개**입니다. 실제 과제가 필요로 하고, 허용되며, 사용자도 검증할 수 있을 때만 검토합니다.

> 자료 조회 자체가 외부 도구 사용 허가나 시험 규정 준수를 보장하지 않습니다. 최신 공식 지시와 실제 과제 README가 우선입니다.
