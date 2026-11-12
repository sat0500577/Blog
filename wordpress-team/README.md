# WordPress 전담팀

회장님 직속 팀으로 사이트 개발·분석·기술 SEO·UI 개선을 맡습니다. 개별 원고·이미지 제작과 콘텐츠 발행 조율은 편집팀, 블로그 방향은 기획팀, 전사 보고·결정 기록은 비서실이 맡습니다.

```text
회장님
└── WordPress 팀장
    ├── WordPress 개발 담당
    ├── 사이트 분석 담당
    ├── 기술 SEO 담당
    └── 사이트 UI·접근성 담당
```

## 역할과 스킬 연결

공통 진입점은 [wordpress-delivery](.agents/skills/wordpress-delivery/SKILL.md)이며 [작업 분기와 확인표](.agents/skills/wordpress-delivery/references/delivery-checklist.md)를 함께 사용합니다. 필요한 담당·스킬만 선택합니다.

| 역할 | 업무·산출물 | 선택 원문 |
|---|---|---|
| [팀장](agents/wordpress-lead.md) | 환경·범위 확인, 실제 위임, 통합 검수·보고 | [wp-project-triage](../hr-team/.agents/skills/wp-project-triage/SKILL.md) |
| [개발 담당](agents/wordpress-developer.md) | 테마·블록·플러그인 코드와 테스트·패치 | wp-project-triage, [wp-block-themes](../hr-team/.agents/skills/wp-block-themes/SKILL.md), [wp-plugin-development](../hr-team/.agents/skills/wp-plugin-development/SKILL.md) |
| [분석 담당](agents/site-analyst.md) | 구조·성능·로그 측정과 재현 근거 | wp-project-triage, [wp-performance](../hr-team/.agents/skills/wp-performance/SKILL.md) |
| [SEO 담당](agents/seo-specialist.md) | 크롤링·메타·색인·검색 데이터 진단과 수정 명세 | [seo-audit](../hr-team/.agents/skills/seo-audit/SKILL.md) |
| [UI 담당](agents/ui-designer.md) | 레이아웃·접근성·반응형 설계와 구현 검수 | [ui-ux-pro-max](../hr-team/.agents/skills/ui-ux-pro-max/SKILL.md), 블록 테마일 때 wp-block-themes |

외부 원본은 인사팀에서 중앙 관리하고 여기에 복제하지 않습니다. 원본 출처·라이선스·파일 해시는 [출처 기록](../hr-team/skill-sources.json), 적용 조건은 [카탈로그](../hr-team/SKILL-CATALOG.md)를 따릅니다.

디자인에 추가 확인이 필요하면 팀장·UI 담당이 이미 보유한 [grilling](../hr-team/.agents/skills/grilling/SKILL.md)을 재사용합니다. UI 담당은 기존 대화·Notion 확정 기획·코드로 답을 확인한 뒤 질문 초안을 만들고, 팀장이 추천 이유·선택지와 함께 한 번에 핵심 1~2개만 묻습니다. 목표 독자·느낌·참고 선호·피할 요소·한글 글꼴·홈 섹션·모바일 중 필요한 것만 확인하며 의존 질문은 순서대로 진행합니다. 사실은 직접 조사합니다.

사용자 결정이 필요한 항목은 답을 기다리고 독립 조사는 계속합니다. 필요한 합의가 되면 확정/제안/미정 디자인 브리프 → UI/UX 설계 → 구현·검수로 요청 범위에서 진행합니다. 작은 확정 수정·위임받은 선택에는 인터뷰를 강제하지 않으며 기존 답이나 최종 승인을 반복 요구하지 않습니다. 모든 분기를 끝없이 질문하지 않습니다. 새 역할·스킬 사본 없이 기존 grilling만 연결하며 frontend-design·Impeccable은 설치하지 않았습니다.

- 공식 WordPress 4개: `WordPress/agent-skills`, `7374e6f1c913b3b02b25465d266d9c0e0a04fc96`.
- SEO Audit v2.2.5: `coreyhaines31/marketingskills`, `1f837447b20bb6f0e72d87b80ece1c221c362c7d`.
- UI UX Pro Max: `nextlevelbuilder/ui-ux-pro-max-skill`, `6ae86f61f520d6ca229d2f40e070410638c908c5`.

공식 WP 원문의 최상위 `compatibility` 필드는 현재 OpenAI quick_validate 허용 필드와 달라 형식 검사를 통과하지 않습니다. 원본을 수정하지 않고 검증된 wordpress-delivery에서 직접 읽습니다. 설치 파일 존재를 자동 발견·실행 완료의 근거로 삼지 않습니다.

## 실제 작업 방식

기존 요청·접근 가능한 자료 확인 → 사이트 유형·환경 판별 → 분석·측정 → 필요한 SEO/UI 개선안 → 개발 담당 구현 → 관련 기능·검색 설정·접근성·성능 검증 → 요청 범위의 배포·결과 확인 순서입니다.

팀장은 전문 업무를 실제 서브 에이전트 도구로 위임하고 목표·입력·역할·스킬·산출물·쓰기 범위·완료 조건을 전달합니다. 단순 작업은 직접 처리합니다. 같은 파일이나 사이트 설정의 쓰기는 한 명이 담당하며 독립적인 읽기 조사만 병렬화합니다. UI 담당은 설계와 검수, 개발 담당은 코드를 맡습니다.

자식에게 도구가 없으면 팀장이 실제 원문·필수 참고·출처 있는 자료를 전달합니다. 쓰기 도구만 없으면 패치·명세를 반환받아 권한 있는 한 명이 적용·검증합니다. 아무도 접근할 수 없으면 실행 가능한 준비 작업과 필요한 접근을 보고하며 직접 조회·실행하지 않은 일을 완료로 표시하지 않습니다.

[Notion 기획 인계](../.agents/skills/stock-editorial/references/notion-planning-handoff.md)의 확인된 방향을 재사용하고 최신 사용자 지시를 우선합니다. 중요한 질문은 팀장만 취합하며 이미 알려진 답·승인을 반복 확인하지 않습니다. 전사 진행 보고는 [비서실](../executive-office/README.md)에 근거를 넘깁니다.

## 도구·환경 의존 조건

- 사이트 URL, WordPress.com/자체 호스팅, 호스트, 테마·빌더, 실제 코드·관리 권한은 아직 미정입니다. 실제 작업 시 가용 연결·자료를 먼저 확인하고 부족한 핵심만 묻습니다. 이 저장소는 팀 정의이며 운영 WordPress 사이트가 아닙니다.
- 공식 WP 스킬은 WordPress 7.0+/PHP 7.4+를 선언하므로 실제 대상 버전과 대조합니다. 블록 테마·클래식·빌더에 맞는 절차를 선택하고 새 플러그인 설치 권한을 추정하지 않습니다.
- WP 스크립트는 중앙 설치 파일의 절대 경로로 호출하고 실제 대상 저장소를 CWD로 지정합니다. Node 파일 탐지와 실제 WP-CLI 부트스트랩·DB 접근은 구분합니다. `perf_inspect.mjs`는 대상 경로·URL·권한·영향 확인 후 사용합니다. wp-performance의 backend-only 범위와 별도로 팀의 브라우저 UI·프런트 측정은 가능합니다.
- UI 검색은 설치 디렉터리의 `scripts/search.py`를 절대 경로로 호출하며 가상의 `CLAUDE_PLUGIN_ROOT`를 전제하지 않습니다. WordPress 전용 스택은 없으므로 일반 UX·스타일·색·글꼴 검색 결과를 실제 테마에 맞춥니다. React/Tailwind를 자동 적용하지 않습니다. 기본은 `--persist` 없는 조회이며 결과는 제안입니다. 저장 요청에는 지정 경로·기존 파일·고유 영문 slug를 확인하고 승인되지 않은 `--force` 덮어쓰기를 하지 않습니다.
- SEO 수치·방문자·순위·실제 색인 결과는 연결된 데이터가 있을 때만 보고합니다. 공개 HTML 점검으로 전체 검색 성과를 추정하지 않습니다. 영어 글자수 기준을 한국어에 그대로 강제하지 않고 canonical/schema의 테마·플러그인 소유와 중복을 확인합니다. 정적 fetch만으로 동적 JSON-LD 부재를 단정하지 않습니다.
- 승인된 개발·테스트를 매번 재승인받지 않습니다. 운영 변경·삭제·마이그레이션은 대상·범위·백업·복구와 기존 승인을 확인합니다. 이번 팀 구성은 실제 사이트 수정·DB 생성·WordPress 게시나 배포를 수행하는 요청이 아닙니다.

## 시작 예시

> WordPress 팀장, 접근 가능한 사이트 자료를 먼저 확인하고 모바일 가독성과 기술 SEO 개선 작업을 필요한 담당에게 나눠줘. 확인된 문제와 구현 범위, 검증 결과를 보고해줘.

역할별 시작 프롬프트는 위 역할 파일에 있습니다. URL·권한이 없으면 임의 사이트를 만들거나 속도·순위를 보고하지 않고 필요한 접근과 준비 가능한 작업을 구분합니다.

## 구성과 검증 상태

2026-11-12 KST 기준 5역할·맞춤 스킬 1개와 외부 원본 6개의 사용 연결을 준비했습니다. 스킬 초기화 도구로 맞춤 패키지를 만들었으며 자동 등록·상시 실행·사이트 연결은 설정하지 않았습니다.

외부 도입 담당의 검증: 원본 및 루트 LICENSE 121파일의 Git blob·SHA-256 대조, 공식 WP의 전체 GPL COPYING 4개 별도 보존, Node 파일 탐지 스크립트 3개의 임시 fixture 실행, UI 읽기 전용 domain 검색, SEO/UI 형식 검사 통과. 공식 WP 4개의 형식 차이는 위에 기록했습니다. 실제 WP 성능·DB·PHP 실행은 수행하지 않았습니다.

팀 구성 검증: wordpress-delivery 형식 검사, UI 메타데이터, Markdown 8개 문서의 상대 링크 45개, 미완성 표시와 공백 오류 검사를 통과했습니다. URL·권한 없음, 클래식 테마의 UI 요청, GSC 없는 색인 진단, 승인된 스테이징 코드 수정의 네 입력을 정적으로 검토해 접근 한계·분기·단일 쓰기·승인 범위가 구분되는지 확인했습니다. 이는 실제 사이트 실행 테스트가 아닙니다.

독립 담당이 WordPress.com의 요금제·권한 미확인 요청과 승인된 스테이징 본문 폭 수정 요청을 가상 입력으로 적용했습니다. 실제 근거와 미확인 상태, 필요한 담당만 선택하는 분배, 단일 코드 쓰기, 반복 승인 없이 허용 범위에서 진행하는 응답을 확인했습니다. 실제 위임·사이트 실행 결과가 아닌 문서 기반 응답 검증입니다.

실제 사이트 진단·수정·브라우저 화면 검사·배포는 사이트와 권한이 확인된 후 해당 요청에서 검증합니다.
