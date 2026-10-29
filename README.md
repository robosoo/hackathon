# AI 과제 해결용 공개 도구함

응시자가 **직접 README를 읽고 문제를 먼저 이해한 다음**, 필요한 Skill만 선택하여 결과를 재현·검증하기 위한 공개 학습용 지침입니다. 공식 대회 지침·기출·완성 답안은 아닙니다.

## 시작하기 — 아래 두 문장만 입력

```text
실제 시험 과제의 README 위치를 알려줘. 내가 먼저 직접 읽고 이해할 때까지 문제 해석·Skill 실행·코딩은 시작하지 마.

공개 GitHub 저장소 https://github.com/robosoo/hackathon 에 허용된 방법으로 접근하여 START_PROMPT.md를 실제로 읽어. 내가 문제를 이해하고 진행하라고 말한 뒤에만 그 지침에 따라 분석·구현·검증을 도와줘.
```

**중요:** Codex가 실제로 `START_PROMPT.md`를 읽어야 지침을 적용할 수 있습니다. URL만 전달해서 Skill이나 Plugin이 자동 설치되는 것은 아닙니다. 접근할 수 없으면 그 사실을 보고해야 합니다. **참가자가 문제를 직접 읽고 진행하라고 말하기 전에는 어떤 분석·Skill·코딩도 시작하지 않습니다.**

## 구성

| 파일 | 목적 |
| --- | --- |
| [START_PROMPT.md](START_PROMPT.md) | **참가자 먼저 문제 이해 → 참가자의 진행 지시 → 필요시 브레인스토밍 → 구현·검증** |
| [SKILLS.md](SKILLS.md) | 겹치지 않는 자체 Skill 4개와 공개 Skill 원본 참고 |
| [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) | 실제 요구에 따라 도구를 최소 선택 |
| [PLUGINS.md](PLUGINS.md) | 설치 없이도 가능한 작업과 Plugin 후보 비교 |
| [SAFETY.md](SAFETY.md) | 핵심 금지행동·자료 보호·우선순위 |
| [AGENTS.md](AGENTS.md) | 이 저장소를 읽은 에이전트용 간단 안내 |
| [.agents/skills](.agents/skills) | 이 저장소에서 직접 작성한 Skill 4개 |

**사용자 판단 우선:** AI는 과제 README의 위치만 알려주고 대기합니다. 참가자가 문제를 직접 해석하고 자신의 목표·중요 조건·예외를 제시한 뒤, 필요한 검토와 구현을 지시합니다. 도구 사용량이나 단독 판단에 따른 공식 가산점·감점 배점은 확인되지 않았습니다.

**Superpowers 활용:** 공개 [`brainstorming` 원본](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md)의 **문제 맥락 확인·대안 비교·성공 기준 정의**를 참고하여 [시험용 경량 브레인스토밍 Skill](.agents/skills/brainstorm-requirements/SKILL.md)을 별도로 작성했습니다. 원본을 그대로 복사하거나 공식 Superpowers Skill을 설치한 것은 아닙니다. 원본의 강제 승인·자동 브라우저 보조·Git 커밋 절차는 가져오지 않았습니다.

**터미널 ≠ AI 채팅:** 터미널은 명령어를 실행하는 창입니다. `node --version`은 설치된 Node.js 버전을 확인하는 예시 명령으로, 설치·업데이트 명령이 아닙니다. 새 터미널을 연다고 AI 채팅이 새로 시작되지는 않습니다.

추가 Plugin·MCP·외부 Harness는 **기본 0개**입니다. 실제 과제가 필요로 하고, 허용되며, 사용자도 검증할 수 있을 때만 검토합니다.

> 자료 조회 자체가 외부 도구 사용 허가나 시험 규정 준수를 보장하지 않습니다. 최신 공식 지시와 실제 과제 README가 우선입니다.
