# hynix-r2-skillset

제공된 Codex에서 사용하는 해커톤 작업 가이드다. 공통 규칙은 AGENTS.md에, 단계별 절차는 스킬에 둔다. 추가 API 키나 MCP는 필요하지 않다.

## 가져오기

제공 웹 IDE의 Linux 터미널에서 실행한다. 경로가 이미 있으면 기존 파일을 확인해 재사용한다.

```bash
git clone --depth 1 https://github.com/hephee/hynix-r2-skillset.git /tmp/hynix-r2-skillset
```

Codex에 전달할 요청:

```text
지금은 제출 확정 전 구현 단계야.
과제 루트는 [경로], 플랫폼 과제 남은 시간은 [시간]이야.
/tmp/hynix-r2-skillset/AGENTS.md를 읽고 연결된 공통 문서도 확인해줘.
공식 안내와 기존 과제 지침을 우선하고 충돌은 알려줘.
기존 README·AGENTS.md·AGENTS.override.md·MY.md는 수정하지 마.
가이드 폴더의 .agents/skills/r2-*를 과제 루트의 .agents/skills로 복사하되
같은 이름이 있으면 비교하고 덮어쓰지 마.
전역·플랫폼 설정은 바꾸지 마.
스킬이 목록에 없으면 해당 SKILL.md를 직접 읽어 사용해줘.
먼저 r2-scope로 목표와 완료 기준을 정리해줘.
```

작업 지침이 과제 폴더에 자동 적용된다고 가정하지 않고 직접 읽도록 요청한다.

## 문서

| 파일 | 용도 |
| --- | --- |
| [AGENTS.md](AGENTS.md) | 작업·소통·PRD 기록·검증 원칙 |
| [CONTEXT.md](CONTEXT.md) | 시간·환경·제출 절차·필수 규정 |
| [PRD 양식](templates/PRD.md) | 실제 과제에서 시작할 빈 구조 |

```text
hynix-r2-skillset/
├─ README.md          사용법·문서 목록·출처
├─ AGENTS.md          공통 작업 지침·PRD 기록 기준
├─ CONTEXT.md         시험 맥락·필수 규정
├─ PRD.md             현재 작업 기록
├─ templates/PRD.md   빈 과제 기록 양식
└─ .agents/
   ├─ README.md       스킬 통합 안내
   └─ skills/         스킬 8개와 각각의 SKILL.md
```

실제 과제의 PRD에는 수정 이력과 함께 두 요약을 남긴다: **무엇을 어떻게 만들었는지**, **어떤 AI 도구·스킬을 쓰고 무엇으로 검증했는지**. `MY.md`는 사용자 개인 메모다.

## 스킬

사용 시점과 요청 예시는 [스킬 통합 안내](.agents/README.md)에서 확인한다.

필요한 것만 호출한다. 예: `$r2-build 핵심 흐름을 구현해줘.`

| 이름 | 역할 |
| --- | --- |
| [r2-scope](.agents/skills/r2-scope/SKILL.md) | 요구·완료 조건 |
| [r2-questions](.agents/skills/r2-questions/SKILL.md) | 담당자 확인 질문 |
| [r2-build](.agents/skills/r2-build/SKILL.md) | 핵심 구현 |
| [r2-debug](.agents/skills/r2-debug/SKILL.md) | 오류 재현·수정 |
| [r2-verify](.agents/skills/r2-verify/SKILL.md) | 검증·제출 점검 |
| [r2-handoff](.agents/skills/r2-handoff/SKILL.md) | 세션 인수인계 |
| [r2-explain](.agents/skills/r2-explain/SKILL.md) | 제출 확정 전 설명 복습 |
| [r2-data](.agents/skills/r2-data/SKILL.md) | 데이터 분석 점검 |

시험 자료·답안·작업물을 이 공개 저장소에 올리지 않는다. 제출 확정 후에는 제공된 스킬을 통한 AI 지원을 중단한다.

## 출처

공식 인증을 받은 문서가 아닌 사용자 준비 자료다. 작성 기준일은 2026-10-31이다.

사용자가 제공한 PDF를 참고했다. 원본·전체 추출문은 이 저장소에 재배포하지 않는다.

- 시험 필수확인사항 브리프 1쪽: 일정·도구·유출·자동 조작·서술형 제한.
- Proctor 설치 및 촬영 가이드 1쪽: 장비·설치·신분증·촬영.
- 사전 체험 및 응시환경 상세 가이드 1~5쪽: 작업 환경·저장·제출·규칙·장애 대응.

참고 저장소:


문장과 스킬 본문은 사용자 작업 방식에 맞춰 재작성했다. 타인의 개인 특성·후기·점수·미확인 실행 설정은 공통 사실로 채택하지 않았다. 승인·샌드박스 해제 안내도 제외했다.
