# hynix-harness-kit

SK하이닉스 AI 해커톤 2차 예선용 **작업 하네스 키트**.
과제 해답 코드는 들어 있지 않으며, 코딩 에이전트(Codex)와 일하는 **방식과 문서 양식**만 담고 있다.

## 구성
| 파일 | 용도 |
|---|---|
| `AGENTS.md` | Codex가 자동으로 읽는 작업 규칙 (단계, 보고 형식, 시험 환경 규칙) |
| `templates/AGREEMENT.md` | 합의문: 문제·성공 기준·범위·제약 |
| `templates/DECISIONS.md` | 설계 판단과 근거 |
| `templates/VERIFICATION.md` | 검증 결과, 교차 검증, 알려진 약점 |
| `templates/HANDOFF.md` | 현재 상태, 작업 목록, 실행 방법, 인수인계 |
| `templates/SELF_REVIEW.md` | 제출 직전 자기 점검: 예상 질문 6유형(A~F) 기준 요약 |
| `prompts/PROMPTS.md` | 단계별 복사용 프롬프트, 업무 담당자 인터뷰 질문, 서술형 답안 틀 |
| `scripts/init.sh` | 위 파일들을 과제 폴더에 한 번에 복사하고 첫 커밋 |

## 시험 당일 사용법
과제 폴더(작업 공간) 터미널에서 아래 3줄을 순서대로 입력한다.
```bash
git clone https://github.com/Malrangbbobbi/hynix-harness-kit
bash hynix-harness-kit/scripts/init.sh .
codex
```
- 1줄: 키트를 `hynix-harness-kit` 폴더로 받는다.
- 2줄: `AGENTS.md`와 `docs/` 양식 5개를 과제 폴더에 복사하고 첫 커밋을 한다.
- 3줄: Codex 실행 후 `/model`로 모델을 선택한다.

그다음 왼쪽 파일 탐색기에서 `hynix-harness-kit/prompts/PROMPTS.md`를 열고 **[시작]** 프롬프트부터 순서대로 사용한다.

## 시간 계획 (180분 기준)
| 경과 | 단계 |
|---|---|
| 0~15분 | 본인 확인, README 읽기, 키트 적용 (S1) |
| 15~35분 | 업무 담당자 인터뷰 → 합의문 확인 → 작업 분해 (S2~S3) |
| 35~130분 | E2E v0 → 작업 단위 구현·검증·커밋 반복 (S4~S5) |
| 130~150분 | 새 세션 교차 검증 → 수정 (S6) |
| 150~160분 | 문서 정리, 알려진 약점·신뢰 근거 작성 (S7) |
| 160~165분 | `[자기 점검]` → `docs/SELF_REVIEW.md` 작성 |
| 165~170분 | SELF_REVIEW.md 직접 읽기 (3줄 요약, D, E) |
| 170분 | **제출** |
