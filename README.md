# 논문·연구보고서 통합 리뷰

원고를 다섯 역할에서 검토하고, 독자가 배포본만 읽고 내린 판단을 담은 저자용 심사평을 작성하는 Codex 스킬 묶음입니다.

## 다른 PC에서 설치

1. ZIP을 임시 폴더에 풉니다. 프로젝트 저장소에서 내려받았다면 `skills`와 이 README가 있는 폴더를 엽니다.
2. 대상 PC의 Codex에서 이미 사용하는 개인 스킬 하나의 `SKILL.md` 경로를 확인합니다. 예를 들어 경로 끝이 `skills/기존스킬/SKILL.md`라면, 복사할 위치는 그 상위 `skills` 폴더입니다. 첫 설치라면 사용자 홈의 `.agents/skills` 폴더를 만듭니다.
3. 배포본 `skills` 안에 있는 `integrated-paper-review`, `paper-review-panel`, `scientific-critical-thinking`, `peer-review` 폴더를 그 위치에 나란히 복사합니다. 이름이 같은 폴더가 이미 있으면 내용을 먼저 비교합니다. 다른 버전을 교체할 때는 기존 폴더를 스킬 검색 경로 밖에 백업한 뒤 교체합니다.
4. 함께 제공한 K-Dense 고지를 보존합니다. 두 K-Dense 스킬을 개별로 복사하거나 재배포할 때는 각각에 [MIT 원문](licenses/K-Dense/LICENSE.md)을 함께 둡니다.
5. Codex에서 새 채팅을 열고 원고와 함께 아래처럼 요청합니다.

```text
$integrated-paper-review 첨부한 원고와 부록을 검토해 줘. 독자가 최종 파일만으로 내릴 수 있는 판단을 포함해 저자용 심사평을 작성해 줘.
```

다섯 역할을 독립적으로 실행하려면 하위 에이전트를 지원하는 환경이 필요합니다. `peer-review`의 선택적 점검 스크립트를 사용할 때는 Python 3.11 이상이 필요합니다.

## 버전 이력

| 버전 | 변경 내용 |
| --- | --- |
| `v2026.11.27` | 문단 논리 검토와 랩미팅 예상 질문·답변 준비를 각각 단독으로 요청할 수 있습니다. 통합 리뷰도 요청하면 독립 패널 검토와 독자 실습을 먼저 진행합니다. |
| [v2026.11.25](https://github.com/ZellKim/paper-review-ms/tree/192f99c94763a36e5634543f9511ab56879c9ce0) | 전체 재검토와 변경 사항 확인의 범위를 구분하고, 기존 검증을 재사용했을 때 심사평에 밝히도록 했습니다. |

배포 버전은 스킬을 갱신한 날짜로 `vYYYY.MM.DD`를 붙입니다. 같은 날 다시 배포하면 `.2`, `.3`을 차례로 붙입니다. 새 버전을 배포할 때는 변경한 스킬과 이 표를 함께 커밋하고, 커밋 제목에 버전을 적습니다. [배포 커밋 이력](https://github.com/ZellKim/paper-review-ms/commits/main/)

## 구성과 출처

| 스킬 | 출처와 버전 | 용도 |
| --- | --- | --- |
| `integrated-paper-review` | 이 묶음의 자체 스킬, v2026.11.27 | 검토 절차, 독자 판단 실습, 필수 보완 판정, 재검토 종료·재개 기준과 심사평 종합 |
| `paper-review-panel` | 이 묶음의 자체 스킬, 2026-11-23 배포본 | 방법론·통계, 비교 공정성, 도메인, 회의적 독자, 글쓰기·표현의 다섯 역할 |
| `scientific-critical-thinking` | K-Dense Inc., 1.5, MIT | 과학적 주장과 근거 평가 |
| `peer-review` | K-Dense Inc., 2.4, MIT | 근거를 명시한 심사평과 점검 양식 |

K-Dense 두 폴더의 33개 파일은 공식 저장소의 지정 커밋과 파일별 해시가 일치합니다. MIT 라이선스는 위 표의 K-Dense 두 스킬에 적용됩니다. 보안 고지 발췌문의 상대 링크는 원본 저장소를 기준으로 합니다. [원본 커밋](https://github.com/K-Dense-AI/scientific-agent-skills/tree/ec59a29a03d5c40f73ab40878df04860bc00e876) · [MIT 원문](licenses/K-Dense/LICENSE.md) · [K-Dense 보안 고지](licenses/K-Dense/security_disclaimer_20261123.txt)

