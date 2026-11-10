# 회장님 비서실

회장님이 “비서야 이거 해줘”라고 요청하면 최고 비서가 전문 작업을 분배하고 결과를 검수·취합해 보고합니다. 인사팀과 블로그 실무팀은 별도 조직이며, 비서실은 그 팀들의 업무를 지휘하지 않습니다.

```text
회장님
└── 최고 비서
    ├── 현황·보고 담당
    ├── 기록·결정 담당
    └── Notion 구성·디자인 담당
```

## 역할과 로컬 스킬

| 역할 | 담당 업무 | 로컬 지침 |
|---|---|---|
| [최고 비서](agents/executive-secretary.md) | 접수·분배·검수·최종보고 | [executive-coordination](.agents/skills/executive-coordination/SKILL.md), 보고 검수 시 executive-reporting |
| [현황·보고 담당](agents/status-analyst.md) | 원자료 확인·팀별 상태·현황 보고 | [executive-reporting](.agents/skills/executive-reporting/SKILL.md) |
| [기록·결정 담당](agents/knowledge-curator.md) | 확정 결정·근거·후속 작업 기록 | 역할 지침과 executive-coordination의 인계·쓰기 기준 |
| [Notion 구성·디자인 담당](agents/notion-designer.md) | 페이지 구조·DB·읽기 쉬운 구성 | 역할 지침과 executive-coordination의 인계·쓰기 기준 |

[보고 양식](.agents/skills/executive-reporting/references/notion-report-template.md)과 [프로젝트 운영 지침](../AGENTS.md)을 함께 사용합니다. 로컬 스킬이 자동 발견되지 않으면 위 경로를 직접 읽습니다.

## 클라우드 Notion 스킬 연결표

클라우드 원본은 복사 설치하지 않고 필요한 작업에서 읽어 사용합니다. 세션별 별칭 대신 아래 전체 package와 resource를 연결 기준으로 사용합니다.

| 담당 | 스킬과 사용 상황 | 전체 package | 전체 resource |
|---|---|---|---|
| 현황·보고 | notion-weekly-project-digest: 주간 진행 취합 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-weekly-project-digest` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-weekly-project-digest/SKILL.md` |
| 현황·보고 | notion-research-documentation: 여러 자료의 조사·종합 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-research-documentation` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-research-documentation/SKILL.md` |
| 기록·결정 | notion-knowledge-capture: 대화·결정·후속 작업 기록 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-knowledge-capture` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-knowledge-capture/SKILL.md` |
| Notion 구성·디자인 | notion-database-designer: DB 속성·관계·뷰 설계 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-database-designer` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-database-designer/SKILL.md` |
| Notion 구성·디자인 | notion-create-my-team-handbook: 팀 문서·안내 체계 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-create-my-team-handbook` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-create-my-team-handbook/SKILL.md` |
| Notion 구성·디자인 | notion-set-up-my-project: 새 프로젝트 공간이 요청된 경우 | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-set-up-my-project` | `skill://plugin_asdk_app_69c18c28f1188191bf5b8445c4ab0a2e/notion-set-up-my-project/SKILL.md` |

읽는 방법:

1. `skills.read`에 표의 전체 package를 전달하면 SKILL.md를 읽습니다. resource를 지정할 때는 표의 전체 resource를 그대로 전달합니다. 관련 참조가 필요한 경우 해당 스킬이 반환한 정확한 resource 식별자를 사용합니다.
2. package가 없거나 사용 불가이면 `skills.list({"authority":{"kind":"cloud"}})`를 호출하고, 다음 커서가 있으면 끝까지 확인해 동일한 스킬 이름을 찾습니다. 현재 반환된 package·main_resource로 읽습니다. 파일 시스템 경로나 과거 세션의 짧은 별칭으로 변환하지 않습니다.
3. 최고 비서에게만 스킬이 보이면 직접 읽은 원문·필수 참조·실제 도구 입력조건을 담당자에게 전달합니다. 담당자는 전달받은 지침을 적용했다고 밝히며 직접 읽었다고 주장하지 않습니다.
4. 담당자에게 Notion 쓰기 도구가 없으면 초안·변경안만 반환하고, 최고 비서가 가능한 도구로 해당 대상의 단일 작성자가 됩니다. 스킬이 모두에게 없더라도 가능한 로컬 분석·초안은 진행하고 전문 기능·외부 반영의 제한을 명시합니다. 불필요한 설치 요청을 하지 않습니다.

## 실행과 인계

실질적인 전문 요청은 실제 서브 에이전트 도구로 위임하고 단순 답변은 직접 처리합니다. 기본은 단계별 소규모 실행이며 독립된 조사·설계 초안만 병렬로 수행합니다. 위임 도구가 없으면 역할별로 직접 처리하고 실제 위임하지 않았음을 보고합니다.

자료 확정 → 기록 → 최종 디자인 → 최고 비서 검수·최종보고 순서로 진행합니다. 같은 Notion 페이지·DB의 작성자는 한 명입니다. 기본은 전문 담당의 결과를 최고 비서가 통합 반영하며, 쓰기 담당을 바꿀 때는 기존 작업을 끝내고 재조회 후 인계합니다. 같은 대상에 동시 쓰기하지 않습니다.

현황에는 근거, 확인 범위, 완료·진행·대기·차단·미확인 상태와 Asia/Seoul 기준시각·마지막 확인시각을 포함합니다. 파일 존재를 실행 완료로 간주하지 않습니다. 이미 승인된 목적과 계획은 재승인 없이 수행하고, 실제 목적지가 여전히 모호한 경우 필요한 정보만 확인합니다.

예시 요청:

> 비서야, 이번 주 팀별 진행 상황과 결정사항을 정리하고 지정한 Notion 보고 공간을 보기 좋게 구성해줘.

최고 비서가 현황·보고 담당의 자료를 검수한 뒤 기록·결정 담당에게 인계하고, 기록 결과를 바탕으로 디자인 담당을 투입합니다. 마지막으로 결과와 실제 저장 상태를 확인해 회장님에게 보고합니다.

## 연결과 실행 범위

2026-11-10 설정 작업에서 Notion 연결과 비공개 문서함 생성을 확인했습니다. 연결과 스킬·도구 가용성은 세션마다 다르므로 실제 작업에서 다시 확인합니다. 개인별 목적지와 운영 가이드는 비공개 Notion에서 확인하며 공유 저장소에 개인정보를 기록하지 않습니다.

외부 반영은 실제 도구·쓰기 권한·대상을 확인하고 읽기 → 중복 확인 → 쓰기 → 재조회 검증 후 완료로 보고합니다. 오프라인이나 권한 오류이면 작성 가능한 초안과 미반영 상태를 분리해 전달합니다. 결과가 불명확한 쓰기는 먼저 재조회하고 중복 생성하지 않습니다.

역할·스킬 파일은 업무 구성 지침이며 상시 실행이나 다른 채팅의 자동 관찰을 의미하지 않습니다. 기본은 요청 시 실행이고, 정기 일정·자동화·외부 Slack·이메일 전송을 임의로 만들지 않습니다.
