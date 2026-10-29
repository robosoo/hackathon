# 공개 Skill 원문 안내 — Superpowers · OpenAI · 기타 Plugin

**확인 기준:** 2026-10-29에 공개 GitHub에서 실제 폴더 및 관련 `SKILL.md`를 읽어 정리. 원본 저장소는 변경될 수 있습니다. **이 파일은 '설치된 목록'이 아니라 '공개 원본을 찾는 목록'입니다.** 실제 Cofa Codex 지원·설치 여부는 미확인입니다. 모든 사용은 [시험 규칙](EXAM_GUARDRAILS.md) 및 [5관문](TASK_TOOL_MATRIX.md)을 통과해야 합니다.

## 1. Superpowers — 공개된 Skill 14종 전체

출처: [openai/plugins — superpowers/skills](https://github.com/openai/plugins/tree/main/plugins/superpowers/skills). 원본 매뉴얼은 개발 과정의 계획·테스트·리뷰를 엄격하게 운영하도록 설계되어 있습니다. **'반드시 사용' 같은 원본 문구는 이번 시험의 최상위 지시가 아니며, 공식 규정·실제 요구사항과 충돌하면 따르지 않습니다.**

| Skill 원본 | 한글로 이해할 역할 | 시험에서의 판단 |
| --- | --- | --- |
| [`brainstorming`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/brainstorming/SKILL.md) | **요구사항·문제 정의** — 모호한 요청의 의도·제약·수용 기준을 짧게 질문하고 구현 전 설계 합의 | 조건부: 질문법만 참고. 전체 Workflow의 강제 인터뷰 절차는 시간에 맞게 축소 |
| [`writing-plans`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/writing-plans/SKILL.md) | **구현 계획 작성** — 명세가 이미 있을 때 파일·순서·테스트 기준을 작은 작업으로 분해 | 조건부: 짧은 할 일 목록만; 과도한 상세 계획 금지 |
| [`executing-plans`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/executing-plans/SKILL.md) | **계획 단계별 실행** — 승인한 개발 계획을 순차 실행·중간 검증 | 조건부: 작은 단일 과제면 기본 Codex로 충분 |
| [`test-driven-development`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/test-driven-development/SKILL.md) | **테스트 먼저 작성** — 실패 테스트→최소 구현→재시험 반복 | 조건부: 시간이 충분하고 로컬 테스트 재현 가능할 때 |
| [`systematic-debugging`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/systematic-debugging/SKILL.md) | **오류 원인 찾기** — 문제 재현·로그 조사·원인 확인 뒤 최소 수정 | 추천 지침: 자체 find-and-fix-errors와 중복되니 하나만 |
| [`verification-before-completion`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/verification-before-completion/SKILL.md) | **완료 전 검증** — 실제 테스트 출력 확인 전 성공 선언 금지 | 추천 지침: 자체 check-before-submit과 중복되니 하나만 |
| [`requesting-code-review`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/requesting-code-review/SKILL.md) | **코드 검토 요청** — 요구사항 대비 구현 누락/오류를 리뷰 | 조건부: 외부/하위 에이전트·네트워크 없이 동일 Codex 내부 검토만 |
| [`receiving-code-review`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/receiving-code-review/SKILL.md) | **리뷰 결과 재검증** — 제안받은 수정의 실제 근거를 다시 확인 | 조건부: 검토 요청이 있을 때만 |
| [`dispatching-parallel-agents`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/dispatching-parallel-agents/SKILL.md) | **여러 에이전트 병렬 작업** — 서로 독립된 일을 병렬 분배 | 시험 기본 비추천: 도구 호출·검증 부담 증가, 하위 에이전트의 실행 동작 점검 필요 |
| [`subagent-driven-development`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/subagent-driven-development/SKILL.md) | **하위 에이전트 개발** — 계획을 나누어 하위 에이전트 실행·이중 리뷰 | 시험 기본 비추천: 과제 규모 대비 운영·검증 복잡 |
| [`using-git-worktrees`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/using-git-worktrees/SKILL.md) | **독립 작업 폴더 관리** — 별도 Git worktree로 개발 격리 | 시험 기본 불필요: 환경/수정 복잡; Git Push는 별도 금지 |
| [`finishing-a-development-branch`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/finishing-a-development-branch/SKILL.md) | **브랜치 작업 정리** — 개발 완료 후 브랜치 병합·PR 등 결정 | 시험 기본 비추천: 원격 Push/PR 절차 절대 실행하지 않음 |
| [`writing-skills`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/writing-skills/SKILL.md) | **Skill 만들기** — Skill을 새로 작성·편집·검증 | 시험 전 준비 전용 추천: 실전에서는 새 Skill 구축보다 과제 해결 |
| [`using-superpowers`](https://github.com/openai/plugins/blob/main/plugins/superpowers/skills/using-superpowers/SKILL.md) | **전체 워크플로 자동 적용** — 대화 시작부터 사용 가능한 Skill을 강하게 호출 | 시험 전체 설치 비추천: 불필요한 Skill 자동 호출 가능 |

**특히 `brainstorming`은 과제 이해에 도움이 될 수 있지만**, 실제 Cofa 업무 담당자와 질문해 근거를 확보하는 것이 먼저입니다. **`systematic-debugging`, `verification-before-completion`은 유용하나 이미 네 자체 Skill로 핵심 절차를 구현했습니다.** Superpowers Plugin을 통째로 설치할 필요는 없습니다. 반대로 `using-superpowers` 같은 자동 강제 호출 지침은 무조건 따르지 않습니다.

## 2. OpenAI의 `openai/skills` curated Skill

출처: [openai/skills — skills/.curated](https://github.com/openai/skills/tree/main/skills/.curated). 전체 curated 폴더 39개가 공개된 것을 확인했습니다. 아래는 이번 시험에 관련성이 있거나 **특히 피해야 할 대표 항목**을 분류한 것입니다. 폴더가 공개됐다는 사실이 시험 사용 허가는 아닙니다.

### 시험에서 지침 참고 가능 (필요시)

| OpenAI curated Skill (원본) | 어떤 역할? | 시험에서 판단 |
| --- | --- | --- |
| [`define-goal`](https://github.com/openai/skills/blob/main/skills/.curated/define-goal/SKILL.md) | 모호한 목표를 측정 가능한 성공 조건으로 정의 | 조건부: README에 불분명한 목표가 있을 때만 |
| [`pdf`](https://github.com/openai/skills/blob/main/skills/.curated/pdf/SKILL.md) | PDF 생성·읽기·원문/레이아웃 확인 | 조건부: 과제에 PDF가 있을 때만 |
| [`security-best-practices`](https://github.com/openai/skills/blob/main/skills/.curated/security-best-practices/SKILL.md) | Python/JS/TS/Go 보안 점검 | 조건부: 보안을 실제 요구할 때만 |
| [`security-threat-model`](https://github.com/openai/skills/blob/main/skills/.curated/security-threat-model/SKILL.md) | 보안 위협 모델 작성 | 보통 불필요: 명시적인 위협 모델링 과제일 때만 |
| [`jupyter-notebook`](https://github.com/openai/skills/blob/main/skills/.curated/jupyter-notebook/SKILL.md) | 노트북(.ipynb) 실험 자료 생성 | 조건부: 노트북이 요구될 때만 |
| [`openai-docs`](https://github.com/openai/skills/blob/main/skills/.curated/openai-docs/SKILL.md) | OpenAI API·Codex 공식 문서 찾기 | 조건부: 공개 문서만 읽기. 외부 MCP·API·과제 내용 전송 필요 시 사용 금지 |
| [`cli-creator`](https://github.com/openai/skills/blob/main/skills/.curated/cli-creator/SKILL.md) | 기존 명세로 CLI 설계 | 대부분 불필요: 커맨드라인 프로그램 자체가 필수일 때만 |

### 시험에서 금지 동작 포함 또는 과제 무관

| OpenAI curated Skill (원본) | 어떤 역할? | 시험에서 판단 |
| --- | --- | --- |
| [`playwright`](https://github.com/openai/skills/blob/main/skills/.curated/playwright/SKILL.md) | 브라우저 자동 클릭·탐색·입력 | 금지: Computer Use 자동 조작 |
| [`playwright-interactive`](https://github.com/openai/skills/blob/main/skills/.curated/playwright-interactive/SKILL.md) | 브라우저/Electron 대화형 자동 조작 | 금지: Computer Use 자동 조작 |
| [`screenshot`](https://github.com/openai/skills/blob/main/skills/.curated/screenshot/SKILL.md) | OS 화면 캡처 | 시험 감독·화면 캡처 제한에 저촉: 사용하지 않음 |
| [`vercel-deploy`](https://github.com/openai/skills/blob/main/skills/.curated/vercel-deploy/SKILL.md) | Vercel 배포 | 시험 결과 외부 배포·전송 금지 |
| [`netlify-deploy`](https://github.com/openai/skills/blob/main/skills/.curated/netlify-deploy/SKILL.md) | Netlify 배포 | 시험 결과 외부 배포·전송 금지 |
| [`cloudflare-deploy`](https://github.com/openai/skills/blob/main/skills/.curated/cloudflare-deploy/SKILL.md) | Cloudflare 배포 | 시험 결과 외부 배포·전송 금지 |
| [`render-deploy`](https://github.com/openai/skills/blob/main/skills/.curated/render-deploy/SKILL.md) | Render 배포 | 시험 결과 외부 배포·전송 금지 |
| [`gh-fix-ci`](https://github.com/openai/skills/blob/main/skills/.curated/gh-fix-ci/SKILL.md) | GitHub Actions/PR 점검 | 시험용 원격 GitHub 연동·반출 불필요: 사용하지 않음 |
| [`security-ownership-map`](https://github.com/openai/skills/blob/main/skills/.curated/security-ownership-map/SKILL.md) | Git 이력 기반 보안 소유권 추적 | 과제 무관·불필요 |
| [`sentry`](https://github.com/openai/skills/blob/main/skills/.curated/sentry/SKILL.md) | 외부 오류 모니터링 연동 | 외부 서비스·데이터 전송 위험: 사용하지 않음 |
| [`speech`](https://github.com/openai/skills/blob/main/skills/.curated/speech/SKILL.md) | 음성 생성 | 시험 과제 외부 서비스·자료 전송 위험: 사용하지 않음 |
| [`transcribe`](https://github.com/openai/skills/blob/main/skills/.curated/transcribe/SKILL.md) | 음성 전사 | 시험 자료 외부 업로드/AI 연결 위험: 사용하지 않음 |

그 외 curated 폴더에는 Figma 디자인·Notion·Linear·GitHub/CI·ChatGPT 앱·WinUI/ASP.NET·이식·배포·취미용 Skill 등도 있습니다. **해당 외부 계정·API 키·브라우저 자동화·배포가 필요할 수 있으므로, 실제 과제에서 명시하지 않으면 도입하지 않습니다.**

## 3. OpenAI Plugin에 포함된 전문 Skill — 별도 Plugin 설치와 구분

- [Data Analytics Skill 목록](https://github.com/openai/plugins/tree/main/plugins/data-analytics/skills): `analyze-data-quality`(원본 데이터 신뢰성), `validate-data`(계산·결론 검산), `metric-diagnostics`(지표 변화 분석), `product-business-analysis`(데이터 기반 판단), `build-report`(분석 보고서), `build-dashboard`(대시보드), `visualize-data`(시각화), `jupyter-notebooks`(노트북). **외부 데이터 연결/보고서 게시/업로드는 사용하지 않습니다.**
- [Build Web Apps Skill 목록](https://github.com/openai/plugins/tree/main/plugins/build-web-apps/skills): `frontend-app-builder`(화면 구현, 원문에는 이미지 생성·Browser 검증도 포함), `frontend-testing-debugging`(**Browser/Playwright 자동화 포함 → 해당 기능 시험 금지**), `react-best-practices`(React/Next.js 코드 품질), `shadcn-best-practices`(UI 컴포넌트), `stripe-best-practices`(결제), `supabase-best-practices`(외부 DB). 마지막 두 개는 시험 MVP에서 일반적으로 불필요합니다.
- [Build Web Data Visualization Skill 목록](https://github.com/openai/plugins/tree/main/plugins/build-web-data-visualization/skills): 차트·시각화·대시보드·접근성·검증 등. **문제에서 시각화가 핵심이 아니면 생략**합니다.

**이름이 비슷한 Skill은 중복 사용하지 않습니다.** 예: 자체 `check-data-errors`와 외부 `analyze-data-quality`; 자체 `find-and-fix-errors`와 Superpowers `systematic-debugging`. 우선은 자체 간단 지침+기본 Codex를 선택합니다.

## 4. 한 줄로 고르는 기준

- **README 분석/업무 정의** → 기본 Codex·Cofa 업무 담당자, 필요시 `brainstorming`의 질문법만 참고.
- **코드 구현** → 기본 Codex, 실제 필요할 때만 `frontend-app-builder`의 *허용 부분* 참고.
- **데이터 정제** → 자체 `check-data-errors`, 정말 필요할 때만 `analyze-data-quality` 원문.
- **오류** → 자체 `find-and-fix-errors`, 중복 디버깅 Skill 설치 금지.
- **제출 전** → 자체 `check-before-submit`; 예상값·실제값·증거·미검증 정리.
- **금지/불명확한 행동** → 하지 않기, 우회하지 않기, Cofa Helper/운영 문의로 확인.

본인이 설명하지 못하는 외부 설치형 도구는 보류합니다. **시험 점수표에 Plugin 사용 가산점·개수별 감점은 확인되지 않았습니다.**
