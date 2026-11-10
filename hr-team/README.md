# AI 인사팀

블로그 저장소 안에서 인사팀 관련 자료를 정리하는 폴더입니다. ChatGPT의 별도 프로젝트 생성과는 구분됩니다.

## 조직

```text
회장님
└── 인사팀장
    ├── 스킬 탐색 담당
    └── 에이전트 제작 담당
```

인사팀장은 요청을 분배하고 결과를 검수해 회장님에게 보고합니다. 인사팀과 블로그 실무팀은 별도 조직입니다.

## 역할과 스킬

인사팀의 에이전트 역할 지침과 스킬 원본을 이 폴더 안에서 함께 관리합니다. 중복 사본은 만들지 않습니다.

| 역할 | 역할 지침과 시작 프롬프트 | 사용 스킬 |
|---|---|---|
| 인사팀장 | [역할 지침](agents/hr-manager.md) | [분배와 검수](.agents/skills/agent-skill-management/SKILL.md) |
| 스킬 탐색 담당 | [역할 지침](agents/skill-scout.md) | [후보 평가와 인계](.agents/skills/skill-discovery/SKILL.md), [find-skills](.agents/skills/find-skills/SKILL.md) |
| 에이전트 제작 담당 | [역할 지침](agents/agent-builder.md) | [에이전트 구성](.agents/skills/agent-building/SKILL.md), [skill-creator](.agents/skills/skill-creator/SKILL.md), [skill-installer](.agents/skills/skill-installer/SKILL.md) |

공통 운영 기준은 [AGENTS.md](../AGENTS.md)를 따릅니다.

## 이 폴더의 자료

- agents 폴더: 인사팀 에이전트 3개의 역할 지침과 시작 프롬프트
- .agents/skills 폴더: 자체 운영 스킬 3개와 중앙 관리하는 외부 스킬 5개
- [스킬 도입 목록](SKILL-CATALOG.md): 후보 비교, 추천 이유와 사용 조건
- [원본 출처 기록](skill-sources.json): 고정한 커밋, 라이선스와 파일 해시

이후 에이전트 제작 요구사항, 검증 결과와 프로젝트별 배치 기록도 이 폴더에 정리합니다.

[기획팀](../planning-team/README.md)은 이 폴더의 [grilling](.agents/skills/grilling/SKILL.md)과 [content-strategy](.agents/skills/content-strategy/SKILL.md)를 참조합니다. 외부 원본은 인사팀이 관리하고, 주식 블로그에 맞춘 질문 방식과 역할 지침은 기획팀에 둡니다.

역할 지침과 스킬 원본, 관련 조사·관리 자료를 모두 이 폴더에 모읍니다. 중첩된 스킬이 자동 발견되지 않는 환경에서는 공통 운영 지침에 명시된 경로를 직접 읽어 적용합니다.
