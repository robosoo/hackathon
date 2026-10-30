# 외부 공개 Skill 참고 목록

자체 Skill 5개의 사용 시점은 [AGENTS.md](AGENTS.md)에 있다. 이 문서는 **자체 Skill만으로 부족하고 실제 과제에 필요한 경우**에만 읽는다. 아래 링크는 참고 출처이며, 시험 Codex에 설치·활성화된 도구라는 뜻이 아니다.

| 필요한 경우 | 공개 참고 Skill |
| --- | --- |
| 복잡한 작업을 작은 단계로 나눌 필요 | [Superpowers writing-plans](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/writing-plans/SKILL.md) |
| 독립 재현 테스트 설계 | [Superpowers test-driven-development](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/test-driven-development/SKILL.md) |
| 데이터 지표·결론 검산 | [Data Analytics validate-data](https://github.com/openai/plugins/blob/main/plugins/data-analytics/skills/validate-data/SKILL.md) |
| PDF가 실제 입출력 | [OpenAI pdf](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) |
| 실제 구현이 React/Next.js | [react-best-practices](https://github.com/openai/plugins/blob/main/plugins/build-web-apps/skills/react-best-practices/SKILL.md) |

**중복 적용하지 않기:** 자체 `brainstorm-requirements`는 [Superpowers brainstorming](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md)의 접근법을 참고한 독립 경량 지침이다. 자체 `find-and-fix-errors`는 외부 systematic-debugging, `check-before-submit`은 verification-before-completion, `check-data-errors`는 analyze-data-quality와 역할이 겹친다.

`decision-log`는 [공개 Cofa Skill 예시](https://github.com/ColdTbrew/cofa-skills/blob/main/skills/decision-log/SKILL.md)의 기록 취지를 참고하되 별도로 작성했다. 원본 지침 전체를 자동 실행하지 않는다. 설치·네트워크·자동 조작 제한은 [SAFETY.md](SAFETY.md)에 따른다.
