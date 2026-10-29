# SK하이닉스 AI 해커톤 · 공개 AI 도구함

**이 저장소는 시험 전에 준비하는 공개 학습용 자료 모음입니다.** 2026년 SK하이닉스 AI 해커톤 2차 예선의 공식 시스템·문제·답안이 아닙니다.

> 핵심 원칙: **최신 Cofa 규정 준수** → 실제 과제 README → 도구 기본 0개 → 필요한 지침만 선택 → 구현 → **내가 직접 검증하고 설명** → 미검증 항목 보고.

## 시험장에서 입력할 문구 — 딱 두 문장

```text
실제 시험 과제의 README를 먼저 읽고 요구사항과 제한사항을 확인해.

그다음 공개 GitHub 저장소 https://github.com/robosoo/hackathon 에 허용된 방법으로 접근하여 START_PROMPT.md를 실제로 읽고, 해당 지침에 따라 과제 분석부터 구현·검증까지 진행해.
```

위 두 문장으로 `START_PROMPT.md`를 실제로 읽을 수 있다면, 그 아래 **Codex용 자체 진행 절차**가 규정 확인→필요한 Skill 선택→최소 구현→검증을 안내합니다. **별도의 긴 프롬프트를 입력할 필요는 없으며**, 읽기 실패나 권한 문제는 Codex가 직접 보고해야 합니다. 지시문은 도구 실행을 기술적으로 강제하거나 차단하지 않으므로, 필요한 수동 점검은 참가자가 합니다.

## 처음 시작하는 사람을 위한 3단계

1. [START_PROMPT.md](START_PROMPT.md)의 **두 문장 시작 문구**만 입력하고, 문서의 Codex용 지침을 실제로 읽었는지 확인합니다.
2. [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md)에서 **과제별 최소 도구·직접 검증 방법**을 확인하고, [SKILL_TREE.md](SKILL_TREE.md)에서 필요한 Skill만 고릅니다. MCP는 [MCP_GUIDE.md](MCP_GUIDE.md)에서 확인합니다. `Plugin`과 `Skill`의 차이는 [PLUGINS.md](PLUGINS.md)에 있습니다.
3. [WORKFLOW.md](WORKFLOW.md)를 따라 문제를 해결하고 [CHECKLIST.md](CHECKLIST.md)로 결과를 검증합니다.

## 파일 안내

| 파일 | 무슨 역할? |
| --- | --- |
| [START_PROMPT.md](START_PROMPT.md) | **두 문장으로 시작하여 규칙·도구 선정·구현·검증까지 이어지는 Codex 지침** |
| [EXAM_GUARDRAILS.md](EXAM_GUARDRAILS.md) | **외부 전송·Computer Use·외부 AI·보안 우회 금지** 및 매 실행 전 안전 점검 규칙 |
| [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md) | **비공식 예상 과제별 도구 선택표: Plugin/MCP 기본 0개, 검증·자기 설명 5관문** |
| [PUBLIC_SKILLS_CATALOG.md](PUBLIC_SKILLS_CATALOG.md) | **Superpowers 14개 + OpenAI curated 주요 Skill 한글 용도·시험 주의** |
| [MCP_GUIDE.md](MCP_GUIDE.md) | **Cofa MCP 탭 확인 내용·기본 0개·실제 필요시 확인 절차** |
| [SKILL_TREE.md](SKILL_TREE.md) | **한글 Skill 선택 지도**: 자체 3개·외부 7개·Plugin 4개의 목적·사용 조건·규칙상 주의사항 |
| [SKILLS.md](SKILLS.md) | 추천 공개 Skill 7개의 원본 링크와 자체 Skill 3개의 선택 기준 |
| [PLUGINS.md](PLUGINS.md) | 추천 공개 Plugin 4개와 설치·사용의 한계 |
| [WORKFLOW.md](WORKFLOW.md) | Plan → Prompt → Probe → Protect 실전 작업 절차 |
| [CHECKLIST.md](CHECKLIST.md) | 규정·예외조건·테스트·제출 전 확인표 |
| [AGENTS.md](AGENTS.md) | 이 저장소 안에서 Codex가 작업할 경우의 짧은 안내문 |
| [`.agents/skills/`](.agents/skills) | **이 저장소에서 직접 작성한** 경량 Skill 3개. 외부 Skill을 복사한 파일이 아닙니다 |

## 가장 쉽게 쓰는 방법

시험 환경에서 공개 GitHub 접근이 허용되고 실제로 작동할 때, **위 두 문장**을 Codex에 전달하세요. 주소만으로 모든 문서나 Skill이 자동으로 로드되지는 않습니다.

**중요:** 주소를 알려주는 행위만으로 Plugin이 설치되거나 Skill이 자동 인식되지는 않습니다. Codex가 실제로 파일을 읽었는지 확인해야 합니다. 저장소를 Clone하거나 등록할 수 있는지도 Cofa 환경과 상세 규정을 우선 확인해야 합니다. 이 저장소 안의 `.agents/skills/`는 일반적인 repo-local Skill 구조를 따르며 각 `agents/openai.yaml`의 한글 표시도 Cofa 지원이 검증되지 않았습니다. 따라서, **Cofa에서 자동 탐색/호출된다는 보장은 없습니다.**

## 2026-10-29 Cofa 공식 메일에 따른 주의

- 공개 저장소의 지침·Skill·Harness·템플릿·코드 등은 **상세 가이드 허용 범위 안에서 조건부 활용 가능**합니다.
- 활용한 공개 저장소는 **2차 예선 결과 통지 전까지 공개 상태 유지**가 필요합니다. 비공개 저장소는 사용하지 않습니다.
- 공개 자료를 **가져와 참조하는 것**과 시험 문제·파일·결과물을 **외부로 내보내는 것**은 다릅니다. 시험 중 Git Push와 시험 결과물 외부 전송은 하지 않습니다.
- Codex 버전 업데이트 금지, 별도 AI 모델 연결 금지 등 제공 환경의 제한을 지킵니다.
- 후속 서술형 답변은 AI 없이 본인이 작성해야 합니다.
- 외부 저장소의 코드를 통째로 가져와 과제 결과를 대체하지 않습니다. 공개 지침을 읽어도 신뢰성·허용 범위를 확인합니다.

**개인 응시 URL, 비공개 시험 자료, API 키, 자격 증명, 시험 결과물은 여기에 저장하지 마세요.** 사용 이력·제출물·출처는 검토될 수 있습니다.

## 검증된 공개 원천

- [OpenAI Plugins 저장소](https://github.com/openai/plugins)
- [OpenAI 기존 Skills 저장소](https://github.com/openai/skills)
- [OpenAI의 repository-local Skill / AGENTS.md 활용 사례](https://developers.openai.com/blog/skills-agents-sdk)

이 저장소에 있는 Skill은 학습용 오리지널 간단 지침입니다. 외부 Plugin 또는 Skill 설치를 대신하지 않으며, 실제 실행 성공이나 시험 규정 적합성을 보장하지 않습니다.
