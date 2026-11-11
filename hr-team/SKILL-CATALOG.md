# 인사팀 스킬 도입 목록

2026년 11월 12일 갱신. 외부 스킬 15개를 hr-team/.agents/skills 아래에서 중앙 관리합니다. 검색·제작·설치 스킬 3개는 인사팀, 인터뷰·콘텐츠 전략·경쟁 및 독자 조사 스킬 4개는 기획팀, 이미지 스킬 2개는 블로그팀 디자인 담당, WordPress·SEO·UI 스킬 6개는 WordPress 개발팀이 사용합니다. 중앙 저장 위치가 실제 소속·보고 대상을 바꾸지는 않습니다.

## 선정 결과

| 도입 스킬 | 출처 | 저장소 스타 | 담당과 사용 상황 | 라이선스 |
|---|---|---:|---|---|
| [find-skills](.agents/skills/find-skills/SKILL.md) | [vercel-labs/skills](https://github.com/vercel-labs/skills/tree/4e121e6e96c382d8c368a39d24ae272a32746224/skills/find-skills) | 38,777 | 탐색 담당이 새로운 기능에 맞는 생태계 스킬을 찾을 때 | MIT |
| [skill-creator](.agents/skills/skill-creator/SKILL.md) | [openai/skills](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-creator) | 28,633 | 제작 담당이 SKILL.md와 보조 파일을 생성·개선·형식 검증할 때 | Apache-2.0 |
| [skill-installer](.agents/skills/skill-installer/SKILL.md) | [openai/skills](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-installer) | 28,633 | 제작 담당이 선정된 GitHub 스킬을 커밋과 경로를 지정해 가져올 때 | Apache-2.0 |
| [grilling](.agents/skills/grilling/SKILL.md) | [mattpocock/skills](https://github.com/mattpocock/skills/tree/4ae2317ddb22b046e26455e4f9c9b3aaaf62212d/skills/productivity/grilling) | 320,040 | 기획팀이 회장님의 목표·선택·가정을 단계별 인터뷰로 구체화할 때 | MIT |
| [content-strategy](.agents/skills/content-strategy/SKILL.md) | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills/tree/9d6d7ce8d18eb155dc2f9762435f097e60cdad7c/skills/content-strategy) | 59,472 | 기획팀이 독자 질문·콘텐츠 묶음·우선순위·운영 계획을 설계할 때 | MIT |

위 표의 스타 수는 2026년 11월 10일에 GitHub API로 확인한 저장소 전체 수치이며 개별 스킬의 설치 수가 아닙니다. 위 5개의 개별 설치 수는 이 표에 기록하지 않았습니다. OpenAI 두 스킬은 현재 Codex 환경에 맞는 형식과 Python 도구를 제공한다는 점을 우선했습니다.

### 2026-11-11 추가 도입

| 도입 스킬 | 원본 버전 | 사용 상황 | 라이선스 |
|---|---|---|---|
| [competitor-profiling](.agents/skills/competitor-profiling/SKILL.md) | 2.1.8 | 기획서 담당이 경쟁 블로그의 주제·독자·설명·출처·구성을 비교해 차별화 후보를 제안 | MIT |
| [customer-research](.agents/skills/customer-research/SKILL.md) | 2.0.8 | 실제 댓글·질문·설문·인터뷰에서 독자 고민과 표현을 추출해 연재 기획의 근거로 사용 | MIT |

두 스킬은 [coreyhaines31/marketingskills 고정 커밋](https://github.com/coreyhaines31/marketingskills/tree/9d6d7ce8d18eb155dc2f9762435f097e60cdad7c/skills)에서 설치했습니다. 회장님의 방향을 묻는 grilling과 독자 증거를 분석하는 customer-research를 구분하며, 조사 결과의 주제 우선순위 결정은 기존 content-strategy가 맡습니다. 인기도 참고: 2026-11-11(한국 시간)에 확인한 skills.sh 개별 설치 표시는 [competitor-profiling](https://www.skills.sh/coreyhaines31/marketingskills/competitor-profiling) 약 10.3만, [customer-research](https://www.skills.sh/coreyhaines31/marketingskills/customer-research) 약 12.5만이며 집계 시점에 따라 변동합니다.

실제 웹·자료 접근이 필요합니다. 경쟁 분석은 유료 SEO 데이터 연결 없이 공개 페이지의 정성 분석부터 진행할 수 있으며, 방문자·검색량·순위는 데이터가 없으면 미확인으로 둡니다. 독자 조사는 실제 자료가 없으면 조사 계획까지만 만들고 가짜 발언·통계·전체 독자 성향을 생성하지 않습니다. 표본 편향과 관찰/해석/제안을 구분합니다. 외부 연락·설문 발송·사례비 지급이나 서비스 가입은 설치에 포함하지 않습니다. 원문의 raw 저장 지침은 공개 저장소에 원문·개인 정보를 복제하는 지시로 사용하지 않습니다.

Notion의 notion-meeting-prep와 notion-plan-marketing-campaigns는 이미 연결된 플러그인을 기획팀에서 조건부 재사용합니다. 회의 준비는 미결 질문·의사결정 자료에, 캘린더는 확정된 콘텐츠의 제작·발행 계획에 사용합니다. 로컬 설치 수에는 포함하지 않으며, [기획팀 안내](../planning-team/README.md)의 실행 조건과 단일 작성자 원칙을 따릅니다.

원본 전체 폴더와 라이선스를 보존하고, Vercel·Matt Pocock·Corey Haines 스킬에는 저장소 루트의 MIT LICENSE를 함께 보관합니다. 정확한 버전과 파일별 해시는 [skill-sources.json](skill-sources.json)에 기록합니다. content-strategy의 원문 버전은 2.1.8입니다.

## 상황별 사용 조합

### 디자인 담당 도입

| 원본 | 버전 | 담당 업무 |
|---|---|---|
| [baoyu-cover-image](.agents/skills/baoyu-cover-image/SKILL.md) | 1.117.5 | 원고 주제에 맞춘 대표 이미지·썸네일의 구도·색상·비율 설계 및 제작 |
| [baoyu-article-illustrator](.agents/skills/baoyu-article-illustrator/SKILL.md) | 1.117.4 | 원고를 분석해 설명이 필요한 위치에 개념 삽화·과정도 제작 |

[JimLiu/baoyu-skills의 고정 커밋](https://github.com/JimLiu/baoyu-skills/tree/ca703c2d7c2c4399a1dc0cf82224f8551e05a96d/skills)을 설치했고 MIT 원문을 각 폴더에 보존했습니다. 2026-11-11 확인 인기도는 저장소 전체 27,453 stars, skills.sh 개별 설치 표시 [cover-image](https://skills.sh/jimliu/baoyu-skills/baoyu-cover-image) 약 3.3만, [article-illustrator](https://skills.sh/jimliu/baoyu-skills/baoyu-article-illustrator) 약 3.2만입니다.

원본은 top-level `version` 필드를 사용하므로 OpenAI quick_validate에서는 두 스킬 모두 해당 필드 오류를 냅니다. 원본과 해시를 보존하고 Codex 형식에 맞는 [stock-visuals](../.agents/skills/stock-visuals/SKILL.md)를 진입점으로 사용해 직접 읽습니다. 원본의 전역 자동 발견·CLI 작동을 검증했다고 보고하지 않습니다.

현재 네이티브 image_gen 도구를 우선하므로 baoyu-image-gen·별도 API·Codex CLI 래퍼는 설치하지 않습니다. 자식에게 생성 도구가 없으면 디자인 담당이 프롬프트와 배치를 만들고 도구가 있는 편집장/상위 담당이 생성·검수하여 실제 결과를 돌려줍니다. 원문의 최초 설정·매회 확인은 프로젝트 기본값과 이미 승인된 작업 범위에 맞춰 적용하고 전역 설정을 자동 생성하지 않습니다. 결과 이미지·한글 품질은 실제 제작 때 확인합니다.

금융 숫자 차트는 두 생성 이미지 스킬로 검증된 실적처럼 그리지 않습니다. 리서처의 검증 표와 Python 등 차트 도구를 사용하고 기간·통화·단위·축·출처를 팩트체커가 검수합니다. infographic·별도 image 스킬은 일부 기능이 겹쳐 이번에는 설치하지 않았으며, matplotlib 스킬도 기존 차트 도구 재사용으로 보류했습니다. WordPress 업로드·발행은 별도 요청과 실제 연결에 따릅니다.

2026-11-11 원본 검증: installer로 설치한 스킬·참고 문서와 추가 보존 LICENSE 총 74개 파일의 Git blob SHA를 고정 트리와 대조하고 SHA-256을 기록했습니다. 원본 형식 차이는 위에 명시했습니다. 설치는 실제 이미지 생성·업로드·발행 검증을 의미하지 않습니다.

맞춤 연결 검증: stock-visuals는 init_skill.py로 생성했고 stock-editorial과 함께 quick_validate를 통과했습니다. 역할·스킬 문서의 상대 링크 21개와 메타데이터를 확인했습니다. 대표 이미지만 요청, 차트 원데이터 부재, 자식 이미지 도구 부재, 한글 오류 재생성의 네 시나리오를 정적으로 검토했습니다. 실제 이미지 생성·한글 및 모바일 화면 검수·WordPress 업로드는 아직 실행하지 않았습니다.

독립 담당의 가상 입력 적용 1회도 통과했습니다. '이익과 현금흐름' 원고와 전달받은 기획으로 대표·과정 삽화 두 개의 프롬프트·배치·alt·캡션을 제안하고, 미정 브랜드·데이터 부재·상위 담당 생성 필요·미실행 상태를 구분했습니다. 이 가상 검증의 기획과 디자인은 사용자 확정 사항으로 저장하지 않았습니다.

### WordPress 개발팀 도입 — 2026-11-12

| 도입 스킬 | 출처 | 담당·선정 이유 | 라이선스 |
|---|---|---|---|
| [wp-project-triage](.agents/skills/wp-project-triage/SKILL.md) | WordPress/agent-skills | 팀장·분석 담당: 실제 프로젝트 유형과 도구를 먼저 판별 | GPL-2.0-or-later |
| [wp-block-themes](.agents/skills/wp-block-themes/SKILL.md) | WordPress/agent-skills | 개발·UI 담당: 블록 테마, theme.json, 템플릿·패턴 | GPL-2.0-or-later |
| [wp-plugin-development](.agents/skills/wp-plugin-development/SKILL.md) | WordPress/agent-skills | 개발 담당: 플러그인 구조·권한·데이터 처리·검증 | GPL-2.0-or-later |
| [wp-performance](.agents/skills/wp-performance/SKILL.md) | WordPress/agent-skills | 분석 담당: 서버·DB 성능의 근거 기반 진단 | GPL-2.0-or-later |
| [seo-audit](.agents/skills/seo-audit/SKILL.md) | coreyhaines31/marketingskills | SEO 담당: 크롤링·색인·메타·검색 구조 점검, v2.2.5 | MIT |
| [ui-ux-pro-max](.agents/skills/ui-ux-pro-max/SKILL.md) | nextlevelbuilder/ui-ux-pro-max-skill | UI 담당: 로컬 검색 자료를 활용한 가독성·접근성·레이아웃 설계 | MIT |

고정 원본: [WordPress 공식 7374e6f](https://github.com/WordPress/agent-skills/tree/7374e6f1c913b3b02b25465d266d9c0e0a04fc96/skills), [SEO 1f83744](https://github.com/coreyhaines31/marketingskills/tree/1f837447b20bb6f0e72d87b80ece1c221c362c7d/skills/seo-audit), [UI 6ae86f6](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill/tree/6ae86f61f520d6ca229d2f40e070410638c908c5/.claude/skills/ui-ux-pro-max). 원본 전체 폴더·루트 LICENSE를 보존하고 공식 WP에는 GPL 전체 COPYING도 추가 보존했습니다. 파일별 원본·해시는 skill-sources.json에 기록했습니다.

2026-11-12 한국 시간에 확인한 저장소 전체 인기도는 WordPress/agent-skills 2,353 stars, UI UX Pro Max 148,207 stars입니다. UI의 [skills.sh 개별 설치 표시](https://skills.sh/nextlevelbuilder/ui-ux-pro-max-skill/ui-ux-pro-max)는 약 44.66만입니다. 수치는 시점에 따라 변하며 품질 보증이 아닙니다. WordPress는 공식 프로젝트 적합성, SEO는 기존 콘텐츠 전략 스킬과의 연계, UI는 검색 가능한 자료와 실제 실행 도구를 우선했습니다.

원본 WP 4개는 최상위 compatibility 필드 때문에 현재 OpenAI quick_validate를 통과하지 않습니다. 원본을 변경하지 않고 검증된 맞춤 [wordpress-delivery](../wordpress-team/.agents/skills/wordpress-delivery/SKILL.md)를 진입점으로 직접 읽습니다. 공식 원문의 WordPress 7.0+/PHP 7.4+ 선언은 실제 사이트 버전과 대조해야 합니다. 스크립트는 중앙 설치 절대 경로와 실제 대상 코드 CWD를 사용합니다. 파일 탐지와 WP-CLI·DB 부트스트랩을 구분하며, 실제 사이트 정보가 없는 이 저장소에서 성능 진단을 실행하지 않습니다.

UI는 Python 로컬 CSV 검색을 사용하며 WordPress 전용 stack은 없습니다. 일반 UX·스타일·색·타이포그래피를 확인한 테마·빌더에 맞춰 적용합니다. React/Tailwind를 자동 도입하지 않고 기본 조회에 --persist를 사용하지 않습니다. SEO는 웹 조회와 필요 시 실제 Search Console·분석 자료를 사용하며 데이터가 없는 방문자·순위·성과 수치는 미확인으로 둡니다. 실제 사이트·계정 연결이나 유료 서비스는 이번 설치에 포함하지 않습니다.

중복 비교: Vercel web-design-guidelines는 UI 검수 일부가 겹쳐 추가 설치하지 않았습니다. WordPress router와 전체 스킬 묶음도 설치하지 않고 맞춤 조율 스킬이 선택한 6개를 연결합니다. 편집팀의 대표 이미지·삽화 제작은 기존 stock-visuals가 유지하며, 기획팀의 content-strategy와 SEO 담당의 기술 진단은 별도 책임입니다. 세부 실행 조건은 [WordPress 팀 안내](../wordpress-team/README.md)를 따릅니다.

도입 검증: 원본·보존 LICENSE 121개 파일의 Git blob과 SHA-256 대조, GPL COPYING 4개 별도 해시 기록, Node 파일 탐지 3개의 임시 fixture 실행, UI 읽기 전용 UX 검색, SEO/UI와 맞춤 스킬 형식 검사를 완료했습니다. WP 원본의 형식 차이는 위와 같습니다. 독립 담당의 WordPress.com 권한 미확인·승인된 스테이징 UI 수정 두 가상 입력 검토도 통과했습니다. 전체 staged 공백 검사에서는 UI Python과 WP 참고·스크립트 원본의 후행 공백·끝 빈 줄 경고가 확인됐습니다. 원본 해시 보존을 위해 수정하지 않고 자체 작성 파일의 공백 검사를 별도로 통과시켰습니다. 이는 실제 사이트 진단·PHP/DB 실행·브라우저 측정·배포 검증이 아닙니다.

### 업무별 조합

| 요청 | 사용할 스킬 |
|---|---|
| 필요한 스킬을 찾아줘 | find-skills로 후보 탐색 → skill-discovery로 적합성·중복 평가 |
| 이 GitHub 스킬을 가져와줘 | skill-discovery로 원문·조건 확인 → skill-installer로 지정 폴더에 설치 |
| 우리 방식에 맞는 스킬을 만들어줘 | skill-creator로 생성·검증 → 팀장이 실제 사용 결과 확인 |
| 보유 스킬로 에이전트를 만들어줘 | agent-building으로 역할·프롬프트 구성, 스킬 수정이 필요할 때만 skill-creator 사용 |
| 스킬 탐색부터 에이전트 제작까지 해줘 | agent-skill-management로 분배 → 탐색 → 선정 → 설치·제작 → 팀장 검수 |
| 주식 블로그 방향을 인터뷰하고 기획해줘 | 기획팀의 로컬 조율 지침 → grilling → content-strategy → 기존 stock-editorial 브리프로 편집장 인계 |
| WordPress 사이트를 분석하고 SEO·UI를 개선해줘 | wordpress-delivery → 환경 판별 → 필요한 분석·SEO·UI 담당 → 개발·검증 → 팀장 보고 |
| 원고에 맞는 대표 이미지와 본문 삽화를 만들어줘 | 편집장 → 디자인 담당의 stock-visuals → 필요한 Baoyu 원본 → 이미지 제작·검수 → 원고와 함께 인계 |

## 중복 정리

자체 스킬 3개는 프로젝트 정책과 역할 간 인계를 담당합니다. skill-discovery는 검색 방법을 find-skills에 연결하고 비교·추천 기준에 집중합니다. agent-building은 스킬 파일 제작·설치를 외부 스킬에 연결하고 에이전트의 소속·역할·프롬프트 설계에 집중합니다. agent-skill-management는 분배·선정·검수·보고를 맡습니다. 동일한 외부 제작 스킬을 여러 개 설치하지 않습니다.

| 비교했지만 도입하지 않은 후보 | 저장소 스타 | 판단 |
|---|---:|---|
| [Anthropic skill-creator](https://github.com/anthropics/skills/tree/2c5958ecac7cee2b583967a2c4981d0f4a75c579/skills/skill-creator) | 191,294 | 평가·벤치마크에 강점이 있지만 OpenAI creator와 중복. 일부 자동 평가는 Claude CLI와 인증이 필요해 보류 |
| [Obra writing-skills](https://github.com/obra/superpowers/tree/22f0b463e7a5e579904dd6211a520321035526f7/skills/writing-skills) | 315,260 | 압박 시나리오와 반복 평가용. test-driven-development 배경 의존이 있어 평가 체계를 확장할 때 재검토 |

## 실행 조건과 프로젝트 적용

- skill-creator: Python과 PyYAML이 필요합니다. 스킬 생성·형식 검증에 모델 API 키는 필요하지 않습니다. 형식 검증은 실제 업무 정확도 검증과 별개입니다.
- skill-installer: Python, GitHub 연결이 필요하며 Git fallback을 사용할 수 있습니다. 설치 대상은 반드시 이 저장소의 hr-team/.agents/skills로 지정하고 --ref에는 검토한 커밋을 사용합니다. 기본 전역 설치 경로나 글로벌 설치 예시를 그대로 사용하지 않습니다.
- list-skills.py의 설치 여부 표시는 CODEX_HOME/skills 기준이므로 인사팀 폴더 목록과 별도로 확인합니다.
- find-skills: 가이드 파일과 Skills CLI는 별개입니다. 검토한 CLI 소스 버전은 1.7.6이며 Node 22.20.0 이상이 필요합니다. 현재 환경은 Node 24.22.1입니다. CLI 사용에는 npm과 skills.sh 네트워크 접근이 추가로 필요합니다.
- GitHub 커넥터가 검색·원문 조회를 충분히 지원하면 이를 우선 사용합니다. Skills CLI의 네트워크 오류는 빈 검색 결과로 표시될 수 있으므로 0건을 부재의 증거로 단정하지 않습니다. CLI를 사용할 때는 검토 버전을 고정하고 DISABLE_TELEMETRY=1을 적용합니다.
- 중첩 폴더의 스킬이 자동 목록에 표시되지 않아도 루트 AGENTS.md의 경로를 직접 읽어 적용합니다. 파일 저장만으로 전역 등록이나 상시 실행이 완료됐다고 표현하지 않습니다.

## 기획팀 적용 범위와 중복 방지

- grilling은 인터뷰의 핵심만 설치했습니다. 같은 기능의 진입점인 grill-me와 brainstorming은 추가 설치하지 않습니다. 원문의 모든 질문을 한꺼번에 묻는 방식보다 프로젝트 조율 지침을 우선해 한 번에 핵심 1~2개씩 묻고, 이미 확정된 답변을 재질문하지 않습니다. 승인된 내부 작업까지 재승인받는 규칙으로 확대하지 않습니다.
- content-strategy의 B2B 구매·영업·리드 전환은 이 프로젝트에서 독자의 이해·재방문·구독 목표에 맞춰 해석합니다. 주식 거래나 수익을 유도·보장하는 목표로 바꾸지 않습니다. 질문과 수치는 현재 근거에 맞추며 검색량·효과 통계·상위 검색 노출을 지어내지 않습니다.
- 원문 및 evals의 효과 배수, 채널 수명, 비율 등은 외부 저자의 주장·예시이며 이 프로젝트가 검증한 사실이 아닙니다. 60/30/10 배분이나 우선순위 점수도 고정 정책이 아니라 필요할 때 설명할 가설입니다. 외부 명령·발행·배포·이메일 실행 예시는 실행 권한이 아닙니다.
- grilling·content-strategy에는 실행 스크립트나 필수 유료 API가 없습니다. 실제 검색·경쟁 분석에는 접근 가능한 웹 도구와 자료가 필요하고, 별도 데이터 공급자의 비용·권한은 사용 전에 확인합니다. 인터뷰에서 필요한 사실 조사만 위임하며 작업량에 맞춰 모델 호출을 제한합니다.
- content-strategy가 언급하는 copywriting·social·emails·launch 등은 설치하지 않았습니다. seo-audit는 WordPress팀의 기술 SEO 진단용 중앙 원본을 재사용합니다. 관련 스킬 이름이나 CMS 가이드를 발견한 것만으로 추가 설치·웹사이트 구현·외부 발행을 시작하지 않습니다. 본문 작성과 제작 조율은 기존 블로그 실무팀, 확정 결정의 Notion 기록은 비서실로 인계합니다.
- 실적·산업 관점은 [금융 질문 참고자료](../planning-team/references/financial/README.md)에서 확인합니다. 두 문서는 활성 스킬 수에 포함하지 않으며 실제 데이터·투자 분석 실행으로 취급하지 않습니다. stock-research와 stock-fact-check의 원자료·계산·검수 기준을 재사용합니다.

## 원본 업데이트 절차

업데이트할 때 원문과 라이선스, 스크립트 변경을 다시 확인하고 버전·해시 기록을 갱신합니다. 현재 프로젝트 지침과 실제 실행 조건은 외부 예시의 기본값보다 우선합니다.

## 도입 검증 결과

아래 첫 도입 검증은 기존 인사팀 외부 스킬 3개에 대한 기록입니다.

- 가져온 17개 파일을 지정 커밋의 원본 및 보존한 라이선스와 대조했습니다.
- quick_validate.py로 신규 스킬 3개의 형식 검증을 통과했습니다.
- init_skill.py로 임시 폴더에 샘플 스킬을 만들고 형식·메타데이터 생성을 확인했습니다.
- 설치 스크립트의 --help 실행을 확인했습니다. 실제 네트워크 다운로드 설치와 Skills CLI의 온라인 검색은 실행 검증하지 않았습니다.
- PyYAML 6.0.3을 사용했습니다. 이번 검증은 형식과 대표 생성 동작에 대한 확인이며, 향후 제작할 모든 스킬의 업무 품질을 보장하지 않습니다.

기획팀 추가 도입에서는 고정 커밋과 명시적 프로젝트 경로로 installer를 실행했습니다. 신규 스킬 원본·루트 라이선스 8개 파일, 금융 참고 원문·라이선스 3개 파일의 Git blob SHA와 SHA-256을 확인했습니다. 원본 실행 스크립트나 evals는 실행하지 않았으며, 원문 메타데이터와 문서 참조를 보존합니다. 원본 보존·형식·참조 검사는 실제 인터뷰나 콘텐츠 성과 검증을 의미하지 않습니다.

2026-11-11: competitor-profiling·customer-research를 installer로 지정 폴더에 설치했습니다. 원본과 라이선스 총 10개 파일의 Git blob SHA를 고정 커밋의 트리와 대조하고 SHA-256을 기록했습니다. 두 스킬의 quick_validate 형식 검사를 통과했습니다. evals 실행·실제 독자 조사·Notion 캘린더 생성·WordPress 발행은 이번 설치 검증에 포함하지 않습니다.
