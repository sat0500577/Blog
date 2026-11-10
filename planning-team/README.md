# 주식 블로그 기획팀

회장님과 단계적으로 대화해 블로그 방향을 정하고 실행 가능한 기획서를 만드는 독립 팀입니다. 기획팀장은 회장님께 보고하며 기획서 담당에게 작성 업무를 분배합니다.

```text
회장님
└── 기획팀장 겸 인터뷰 담당
    └── 기획서 담당
```

## 역할과 스킬

| 역할 | 담당 | 연결 |
|---|---|---|
| [기획팀장](agents/planning-lead.md) | 한 번에 1~2개 질문, 요구 확인, 위임·검수 | [stock-blog-planning](.agents/skills/stock-blog-planning/SKILL.md), [grilling](../hr-team/.agents/skills/grilling/SKILL.md) |
| [기획서 담당](agents/planning-writer.md) | 방향·주제축·연재·자료 계획·인계 작성 | stock-blog-planning, [content-strategy](../hr-team/.agents/skills/content-strategy/SKILL.md) |

[질문 가이드](.agents/skills/stock-blog-planning/references/interview-guide.md)와 [기획서 양식](.agents/skills/stock-blog-planning/references/planning-brief-template.md)을 사용합니다. 외부 스킬은 인사팀에 보관된 원본을 참조하며 복사 설치하지 않습니다.

## 진행 방식

기존 답 확인 → 선결 질문 1~2개 → 답에 맞춘 다음 질문 → 핵심 요구 요약 확인 → 기획서 담당에게 실제 위임 → 팀장 검수 → 회장님의 개별 기획 검토 순서입니다. 질문 UI와 사용자 질문은 팀장만 담당합니다. 사실은 에이전트가 조사하고 선호·목표·우선순위는 회장님이 결정합니다.

목표·독자·시장·포맷·근거 계획·운영 여력·성공 기준이 기획 가능한 수준이면 질문을 끝냅니다. 확정·제안·미정을 구분해 작성하며, 기획팀 구성 승인이 개별 기획의 최종 승인을 대신하지 않습니다. 이미 확인된 답과 승인된 내용을 반복 확인하지 않습니다.

외부 grilling의 전체 질문 방식보다 한 번에 1~2개 질문을 우선합니다. content-strategy의 B2B 구매 전환·고정 비율·성과 수치를 그대로 가져오지 않고 독자 교육·구독·신뢰라는 실제 목적에 맞춰 적용합니다.

## 기존 팀과의 경계

- [편집장](../agents/editor.md)은 글별 상세 브리프·집필·원고 검수를 계속 책임집니다. 기획팀은 방향·연재·자료 계획을 인계합니다.
- [비서실](../executive-office/README.md)은 요청된 결정 기록·Notion 저장에 재사용합니다.
- [stock-editorial](../.agents/skills/stock-editorial/SKILL.md), [stock-research](../.agents/skills/stock-research/SKILL.md), [stock-fact-check](../.agents/skills/stock-fact-check/SKILL.md)는 기존 기능을 참조합니다.
- [실적 전망](references/financial/earnings-preview.md)과 [산업 개요](references/financial/sector-overview.md)는 금융 질문 프레임용 참고자료입니다. 실행 스킬이나 최신 데이터로 취급하지 않습니다.

차트 분석은 이미지·시계열·지표 계산·백테스트를 구분하고 필요한 스킬과 데이터 조건을 확인합니다. 개발 요구는 별도 범위·인수 기준으로 정리하며 자동 개발·GitHub 이슈 게시를 하지 않습니다. 라이브 데이터·금융 API·Notion 연결을 임의로 설치하지 않습니다.

## 사용 상태

역할과 맞춤 스킬을 구성해 형식·참조·메타데이터 검증 후 요청 시 사용합니다. 실제 회장님 인터뷰부터 기획서 작성까지의 전체 실행은 아직 검증하지 않았습니다. 파일 저장은 전역 등록·상시 실행·모든 채팅의 자동 연결을 의미하지 않습니다. 스킬이 자동 발견되지 않으면 위 경로를 직접 읽습니다.

2026-11-10 검증: 신규 스킬 3개 형식 검사, 원본·라이선스 11개 파일의 고정 Git blob 및 SHA-256 대조, 로컬 참조 검사를 통과했습니다. 가상 입력으로 질문 2개 제한과 기존 답 재사용을 확인했고, 실제 기획서 담당 서브 에이전트에게 순차 위임해 자료·반론·갱신 계획과 확정·제안·미정 구분을 검수했습니다. 테스트 입력과 결과는 실제 블로그 운영 결정으로 저장하지 않았습니다. 실제 사용자 인터뷰, 외부 데이터 분석, Notion 저장·발행은 이 검증에 포함하지 않았습니다.

예시: “기획팀장, 미국 주식 입문자를 위한 블로그를 기획하고 싶어. 필요한 것부터 하나씩 물어봐.”
