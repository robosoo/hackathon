# Skill 지도 — 겹치지 않게 사용하기

**우선순위: 참가자가 시험 과제 README를 직접 읽고 이해하기 전에는 어떤 Skill도 실행하지 않습니다.** 참가자가 이해·진행 의사를 밝힌 뒤에만 필요한 Skill을 선택합니다.

이 저장소의 **자체 Skill 4개**는 각기 다른 일을 담당합니다. `SKILL.md`를 실제 읽어야 작동 방식을 참고할 수 있고, 시험 Codex의 자동 탐색 기능은 보장되지 않습니다.

| 상황 | 실제로 저장한 Skill | 담당 |
| --- | --- | --- |
| **참가자가 먼저 읽고 요청한 뒤** 요구를 해석하거나 설계 선택이 필요할 때 | [`brainstorm-requirements`](.agents/skills/brainstorm-requirements/SKILL.md) | **목표·업무 규칙·대안·성공 조건**을 정리 |
| 오류·테스트 실패가 발생했을 때 | [`find-and-fix-errors`](.agents/skills/find-and-fix-errors/SKILL.md) | 실패 재현 → 원인 확인 → 최소 수정 |
| CSV·표·집계가 있을 때 | [`check-data-errors`](.agents/skills/check-data-errors/SKILL.md) | 중복·결측·형식·단위·경계값 검증 |
| 완료를 말하거나 제출물을 확인할 때 | [`check-before-submit`](.agents/skills/check-before-submit/SKILL.md) | 실제 출력·테스트 근거로 PASS/FAIL/미검증 구분 |

## Superpowers와 OpenAI의 공개 지침 활용

- **[Superpowers `brainstorming`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md)**: 유용한 문제 정의 방식. 원본의 **모든 작업 전 강제 승인**, Git 커밋, Browser 시각 보조 등은 이번 실전 기본 흐름에서 실행하지 않습니다. [자체 경량 변형](.agents/skills/brainstorm-requirements/SKILL.md)은 그중 **맥락 파악·핵심 질문·대안·성공 기준**만 반영했으며 **공식 원본 설치본이 아닙니다**.
- [Superpowers `writing-plans`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/writing-plans/SKILL.md): 복잡한 요구를 작업 단위로 나눌 때만. 간단한 작업은 Codex 기본 계획으로 충분합니다.
- [Superpowers `test-driven-development`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/test-driven-development/SKILL.md): 과제에 로컬 재현 테스트를 만들 필요가 있을 때만.
- [Data Analytics `validate-data`](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/validate-data/SKILL.md): **데이터 자체 품질**이 아닌 계산·지표·결론 검산이 필요한 경우.
- [OpenAI `pdf`](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md): PDF가 실제 입력·제출물일 때만.
- [`react-best-practices`](https://github.com/openai/plugins/blob/main/plugins/build-web-apps/skills/react-best-practices/SKILL.md): 실제 구현이 React/Next.js일 때만.

**중복 제외:** Superpowers `systematic-debugging` ↔ 자체 `find-and-fix-errors`; `verification-before-completion` ↔ `check-before-submit`; Data Analytics `analyze-data-quality` ↔ `check-data-errors`. 기능이 겹치면 둘을 동시에 가져오지 않습니다.

**주의:** 위 외부 링크는 원본 참고용입니다. Plugin이나 외부 Skill을 모두 설치하라는 권고가 아니며, 원문에 포함된 자동 브라우저 조작·외부 AI·Git Push 등의 금지 동작은 실행하지 않습니다.
