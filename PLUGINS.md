# 공개 Plugin 후보 4개 — 기본 설치 0개

**과제별 적용은 [TASK_TOOL_MATRIX.md](TASK_TOOL_MATRIX.md)·[공개 Skill 목록](PUBLIC_SKILLS_CATALOG.md)·[MCP 설명](MCP_GUIDE.md)부터 확인하세요. 기본 Codex로 가능하거나 자신이 결과를 검증·설명하지 못하면 Plugin을 설치하지 않습니다.**

Plugin은 여러 Skill, 지침 및 경우에 따라 도구 연결(MCP)을 묶는 패키지입니다. **Plugin 링크 목록은 설치 목록이 아닙니다.** Cofa의 제공 Codex가 어떤 Plugin을 실제 지원하는지는 현장에서 확인해야 합니다.

| 우선 | 공개 Plugin | 잘 맞는 과제 | 주의 |
| --- | --- | --- | --- |
| 1 | [Data Analytics](https://github.com/openai/plugins/tree/main/plugins/data-analytics) | 데이터 정제·검증·분석·보고서 | 외부 데이터 연결/업로드 금지. 자체 데이터 품질 Skill 우선 |
| 2 | [Superpowers](https://github.com/openai/plugins/tree/main/plugins/superpowers) | 계획·디버깅·테스트·완료 검증 | **전체 설치 기본 비추천**: 강제 단계·Git 워크플로 등. 개별 Skill 원문 참고 |
| 3 | [Build Web Apps](https://github.com/openai/plugins/tree/main/plugins/build-web-apps) | 웹 UI 구현·테스트 | **Browser/Playwright 자동 조작 금지**. 자동 UI 검증을 제외할 수 없으면 사용하지 않음 |
| 4 | [Build Web Data Visualization](https://github.com/openai/plugins/tree/main/plugins/build-web-data-visualization) | 대시보드·시각화 | 시각화가 필수일 때만; 로컬 검산·직접 확인 가능해야 함 |

## 이해를 위한 개념

- **GitHub 공개 저장소**: 파일이 공개된 보관 장소. 네 Public GitHub도 포함될 수 있습니다.
- **Skill**: AI가 읽고 따르는 작업 지침. 대개 `SKILL.md`와 선택적 파일·스크립트로 구성합니다.
- **Plugin**: Skill·기능·도구 연결 등을 묶은 설치·배포 단위입니다.
- **MCP**: 외부 도구·데이터와 연결되는 방식입니다. 연결 대상별 권한과 네트워크 제한이 다릅니다.
- **Harness**: 계획 → 실행 → 검증을 어떻게 반복하고 상태를 관리할지 정해 둔 작업 체계입니다. 반드시 복잡하거나 별도 설치형 프로그램일 필요는 없습니다.

## 일반 Codex에서의 설치 예시 — Cofa 지원은 미확인

[Superpowers README](https://github.com/openai/plugins/blob/main/plugins/superpowers/README.md)는 일반 Codex CLI에서 `/plugins`를 열어 Superpowers를 검색하고 설치하는 흐름을 안내합니다.

이 설명은 **일반 Codex 기준**입니다. 2차 시험용 Codex에 `/plugins`가 없거나 설치 권한·외부 연결이 제한되면 사용하지 말고 기본 Codex로 과제를 해결하세요. 특히 **Codex 버전 업데이트 금지**입니다.

**설치하지 않는 선택이 정상입니다.** 플러그인을 여러 개 설치하는 것보다 README 필수 기능 하나를 완성하고 직접 검증하는 편이 우선입니다. 공식 문서에서 Plugin 개수별 감점·가산점은 확인되지 않았으므로 이를 사실로 단정하지 않습니다.

## 안전 조건

2026년 10월 29일 Cofa 운영팀 메일에 따르면, 공개 저장소의 지침·Skill·Harness·템플릿·코드 등은 상세 가이드 허용 범위에서 활용할 수 있고 **사용한 저장소는 2차 예선 결과 통지 전까지 공개 상태를 유지**해야 합니다. **비공개 저장소 사용과 결과물 통째 대체는 금지**입니다. 기존 가이드의 시험 자료 외부 전송·Git Push·별도 AI 사용 등 제한도 계속 확인하세요.

외부 원문 링크는 참조이며 그 안의 모든 명령을 무조건 실행하라는 지시가 아닙니다.
