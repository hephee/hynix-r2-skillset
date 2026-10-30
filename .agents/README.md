# 스킬 사용 안내

**지금 필요한 스킬만 사용하세요.** 매번 8개를 모두 쓸 필요는 없습니다.

## 어떤 스킬을 쓰면 될까요?

| 상황 | 스킬 | Codex에 입력할 예시 |
| --- | --- | --- |
| 과제를 처음 받아 무엇부터 할지 모르겠어요 | [r2-scope](skills/r2-scope/SKILL.md) | `$r2-scope 반드시 만들 것과 완료 기준을 정리해줘.` |
| 요구가 애매해 담당자에게 확인해야 해요 | [r2-questions](skills/r2-questions/SKILL.md) | `$r2-questions 구현 전에 담당자에게 물을 질문을 만들어줘.` |
| 만들 것이 정해져 구현을 시작하려 해요 | [r2-build](skills/r2-build/SKILL.md) | `$r2-build 합의한 핵심 기능부터 만들어줘.` |
| 오류가 나거나 결과가 예상과 달라요 | [r2-debug](skills/r2-debug/SKILL.md) | `$r2-debug 원인을 찾아서 고쳐줘.` |
| 잘 동작하는지, 빠진 조건은 없는지 궁금해요 | [r2-verify](skills/r2-verify/SKILL.md) | `$r2-verify 필수 요구와 제출 파일을 확인해줘.` |
| 대화가 길어져 새 채팅에서 이어가려 해요 | [r2-handoff](skills/r2-handoff/SKILL.md) | `$r2-handoff 다음 채팅이 이어갈 현재 상태를 정리해줘.` |
| 완성한 기능과 구현 방법을 설명하기 어려워요 | [r2-explain](skills/r2-explain/SKILL.md) | `$r2-explain 구현 방법과 AI 결과를 검증한 과정을 쉽게 설명해줘.` |
| 데이터 집계·분석 결과가 맞는지 확인하려 해요 | [r2-data](skills/r2-data/SKILL.md) | `$r2-data 중복·누락·계산 기준을 확인해줘.` |

## 기본 흐름

**과제 파악 → 구현 → 검증 → 설명 복습**

`r2-scope` → `r2-build` → `r2-verify` → `r2-explain`

- 정의가 애매하면 중간에 `r2-questions`.
- 오류가 생기면 `r2-debug`.
- 실제 데이터 분석이 필요하면 `r2-data`.
- 새 채팅으로 옮기기 전에는 `r2-handoff`.

## 입력 방법

일반 터미널 명령이 아니라 **Codex 대화 입력창**에 `$스킬이름`과 요청을 적습니다. `/r2-scope`가 아닙니다.

```text
$r2-verify 지금 만든 결과물을 필수 요구사항과 비교해서 확인해줘.
```

과제 폴더의 `.agents/skills/`에 설치하고 그 폴더에서 Codex를 실행하세요. `/skills`로 인식 여부를 확인할 수 있습니다. 작업 가이드를 다른 곳에 클론한 것만으로 자동 인식된다고 가정하지 않습니다.

목록에 없으면 실제 가이드 폴더 경로를 지정해 요청할 수 있습니다.

```text
/tmp/hynix-r2-skillset/AGENTS.md와 연결된 공통 문서를 읽고,
/tmp/hynix-r2-skillset/.agents/skills/r2-scope/SKILL.md에 따라
현재 과제의 목표와 완료 기준을 정리해줘.
```

## 기록과 사용 시점

- 수정 기록은 [AGENTS.md의 PRD 기준](../AGENTS.md#prd-기록)에 따라 **작업·이유·도구·검증 결과**를 한 줄로 남깁니다.
- `r2-explain`을 포함한 복습·정리는 **제출물 확정 전**에 끝냅니다.
- 제출물 확정 후에는 제공된 스킬을 통한 AI 지원을 중단합니다. 실제 후속 서술형은 AI 없이 본인이 답변합니다.
