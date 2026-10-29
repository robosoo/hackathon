# SK하이닉스 AI 해커톤 · 공개 AI 도구함

**이 저장소는 시험 전에 준비하는 공개 학습용 자료 모음입니다.** 2026년 SK하이닉스 AI 해커톤 2차 예선의 공식 시스템·문제·답안이 아닙니다.

> 핵심 원칙: **최신 Cofa 규정 준수** → 실제 과제 README 확인 → 필요한 Skill만 선택 → 구현 → 실제 검증 → 미검증 항목 보고.

## 처음 시작하는 사람을 위한 3단계

1. [START_PROMPT.md](START_PROMPT.md)의 **시작 프롬프트**를 읽습니다. Codex에 입력하는 자연어 지시문입니다.
2. [SKILL_TREE.md](SKILL_TREE.md)에서 한글 목적·사용 조건을 확인하고 [SKILLS.md](SKILLS.md)에서 필요한 Skill 하나를 찾습니다. `Plugin`과 `Skill`의 차이는 [PLUGINS.md](PLUGINS.md)에 있습니다.
3. [WORKFLOW.md](WORKFLOW.md)를 따라 문제를 해결하고 [CHECKLIST.md](CHECKLIST.md)로 결과를 검증합니다.

## 파일 안내

| 파일 | 무슨 역할? |
| --- | --- |
| [START_PROMPT.md](START_PROMPT.md) | **최신 시험 금지사항을 포함한** Codex 시작 프롬프트 |\n| [EXAM_GUARDRAILS.md](EXAM_GUARDRAILS.md) | **외부 전송·Computer Use·외부 AI·보안 우회 금지** 및 매 실행 전 안전 점검 규칙 |
| [SKILL_TREE.md](SKILL_TREE.md) | **한글 Skill 선택 지도**: 자체 3개·외부 7개·Plugin 4개의 목적·사용 조건·규칙상 주의사항 |\n| [SKILLS.md](SKILLS.md) | 추천 공개 Skill 7개의 원본 링크와 자체 Skill 3개의 선택 기준 |
| [PLUGINS.md](PLUGINS.md) | 추천 공개 Plugin 4개와 설치·사용의 한계 |
| [WORKFLOW.md](WORKFLOW.md) | Plan → Prompt → Probe → Protect 실전 작업 절차 |
| [CHECKLIST.md](CHECKLIST.md) | 규정·예외조건·테스트·제출 전 확인표 |
| [AGENTS.md](AGENTS.md) | 이 저장소 안에서 Codex가 작업할 경우의 짧은 안내문 |
| [`.agents/skills/`](.agents/skills) | **이 저장소에서 직접 작성한** 경량 Skill 3개. 외부 Skill을 복사한 파일이 아닙니다 |

## 가장 쉽게 쓰는 방법

시험 환경의 Codex가 공개 GitHub 접근을 지원하고 허용하는 경우에 한해, 시작 프롬프트에서 이 주소를 알려주세요.

```text
https://github.com/robosoo/hackathon
```

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
