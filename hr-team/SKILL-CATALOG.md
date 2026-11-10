# 인사팀 스킬 도입 목록

2026년 11월 10일 기준. 인사팀에 필요한 검색, 스킬 제작·검증, 설치 기능을 보완하기 위해 외부 스킬 3개를 선정했습니다. 모두 hr-team/.agents/skills 아래에 저장하고, 기존 인사팀 역할에 연결합니다.

## 선정 결과

| 도입 스킬 | 출처 | 저장소 스타 | 담당과 사용 상황 | 라이선스 |
|---|---|---:|---|---|
| [find-skills](.agents/skills/find-skills/SKILL.md) | [vercel-labs/skills](https://github.com/vercel-labs/skills/tree/4e121e6e96c382d8c368a39d24ae272a32746224/skills/find-skills) | 38,777 | 탐색 담당이 새로운 기능에 맞는 생태계 스킬을 찾을 때 | MIT |
| [skill-creator](.agents/skills/skill-creator/SKILL.md) | [openai/skills](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-creator) | 28,633 | 제작 담당이 SKILL.md와 보조 파일을 생성·개선·형식 검증할 때 | Apache-2.0 |
| [skill-installer](.agents/skills/skill-installer/SKILL.md) | [openai/skills](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-installer) | 28,633 | 제작 담당이 선정된 GitHub 스킬을 커밋과 경로를 지정해 가져올 때 | Apache-2.0 |

스타 수는 위 날짜에 GitHub API로 확인한 저장소 전체 수치이며 개별 스킬의 설치 수가 아닙니다. 개별 설치 수는 확인하지 않았습니다. OpenAI 두 스킬은 현재 Codex 환경에 맞는 형식과 Python 도구를 제공한다는 점을 우선했습니다.

원본 전체 폴더와 라이선스를 보존하고, Vercel 스킬에는 저장소 루트의 MIT LICENSE를 함께 보관합니다. 정확한 버전과 파일별 해시는 [skill-sources.json](skill-sources.json)에 기록합니다.

## 상황별 사용 조합

| 요청 | 사용할 스킬 |
|---|---|
| 필요한 스킬을 찾아줘 | find-skills로 후보 탐색 → skill-discovery로 적합성·중복 평가 |
| 이 GitHub 스킬을 가져와줘 | skill-discovery로 원문·조건 확인 → skill-installer로 지정 폴더에 설치 |
| 우리 방식에 맞는 스킬을 만들어줘 | skill-creator로 생성·검증 → 팀장이 실제 사용 결과 확인 |
| 보유 스킬로 에이전트를 만들어줘 | agent-building으로 역할·프롬프트 구성, 스킬 수정이 필요할 때만 skill-creator 사용 |
| 스킬 탐색부터 에이전트 제작까지 해줘 | agent-skill-management로 분배 → 탐색 → 선정 → 설치·제작 → 팀장 검수 |

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

## 원본 업데이트

업데이트할 때 원문과 라이선스, 스크립트 변경을 다시 확인하고 버전·해시 기록을 갱신합니다. 현재 프로젝트 지침과 실제 실행 조건은 외부 예시의 기본값보다 우선합니다.

## 도입 검증 결과

- 가져온 17개 파일을 지정 커밋의 원본 및 보존한 라이선스와 대조했습니다.
- quick_validate.py로 신규 스킬 3개의 형식 검증을 통과했습니다.
- init_skill.py로 임시 폴더에 샘플 스킬을 만들고 형식·메타데이터 생성을 확인했습니다.
- 설치 스크립트의 --help 실행을 확인했습니다. 실제 네트워크 다운로드 설치와 Skills CLI의 온라인 검색은 실행 검증하지 않았습니다.
- PyYAML 6.0.3을 사용했습니다. 이번 검증은 형식과 대표 생성 동작에 대한 확인이며, 향후 제작할 모든 스킬의 업무 품질을 보장하지 않습니다.
