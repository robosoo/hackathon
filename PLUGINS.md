# Plugin 후보 — 기본 설치 0개 / 자동 연결 금지

Plugin은 Skill·명령·도구 연결을 묶은 패키지입니다. **이 저장소의 링크는 참고 목록일 뿐 실제 설치된 기능이 아닙니다.** 제공 Codex의 지원 여부도 확인되지 않았습니다.

| 필요한 과제 | 공개 Plugin | 선택 기준 |
| --- | --- | --- |
| CSV·표·지표 분석 | [Data Analytics](https://github.com/openai/plugins/tree/main/plugins/data-analytics) | 기본 로컬 분석으로 충분하면 설치하지 않음. 원격 데이터 연결·자료 전송 금지 |
| 간단한 업무 웹앱 | [Build Web Apps](https://github.com/openai/plugins/tree/main/plugins/build-web-apps) | 허용된 UI 구현 지침만 참고. Browser/Playwright 자동 조작 제외 |
| 차트·대시보드 | [Build Web Data Visualization](https://github.com/openai/plugins/tree/main/plugins/build-web-data-visualization) | 과제 필수일 때만. 차트 값·축·필터를 직접 검산 |
| 설계·디버깅·브레인스토밍 | [Superpowers](https://github.com/openai/plugins/tree/main/plugins/superpowers) | **원본 Plugin 전체 설치보다 개별 지침 참고 우선**. [경량 브레인스토밍 Skill](.agents/skills/brainstorm-requirements/SKILL.md) 기본 제공 |

**선택 기준:** ① 과제 필수 기능인가? ② 규정상 허용되는가? ③ 실행 동작·연결 대상·권한을 이해하는가? ④ 참가자가 직접 결과를 재현하고 설명할 수 있는가?

**안전 게이트:** 공개 Plugin·Skill이라는 이유만으로 설치하거나 활성화하지 않습니다. 추가 설치·원격 연결은 기본적으로 생략하며, **실제 과제에 필수이고, 제공 환경과 공식 규정이 허용하며, 연결 대상·입출력·외부 전송 위험을 참가자가 확인한 때에만** 진행합니다. 허용 범위가 불명확하면 연결하지 않고 기본 Codex의 로컬 기능으로 해결합니다. 시험 중 외부 브라우저 직접 접근·금지된 자동 조작을 수행하지 않습니다.

**MCP:** 기본 Codex의 파일 읽기·편집·터미널 실행을 위해 GitHub/Filesystem MCP를 추가할 필요는 없습니다. 공개 저장소 접근은 허용된 방식으로 가능하면 Git Clone·다운로드로 충분합니다. 별도 MCP 설치가 필요한 과제인지 확인하기 전에는 연결을 만들지 않습니다.

**평가 참고:** 특정 Plugin 개수나 Skill 사용 여부에 따른 공식 가산점·감점표는 확인되지 않았습니다. 목적 없는 설치·불투명한 외부 전송·테스트 불가능한 기능은 실전 위험을 키울 수 있습니다.
