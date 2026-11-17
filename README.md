# 쥬비랜드 (Zuviland)

Figma 디자인(`사이트 디자인_261112~261113`)을 라이브클래스 페이지 블록용 HTML로 옮긴 저장소입니다.

## 구조
- `sections/` — 라이브클래스 **텍스트 에디터 블록 → HTML 코드 보기**에 그대로 붙여 넣는 섹션 코드 (인라인 스타일)
- `assets/` — 섹션별 이미지. 라이브클래스에서는 jsDelivr로 불러옵니다:
  `https://cdn.jsdelivr.net/gh/kaniislove/jubiland@main/assets/...`
- `preview/` — 로컬 미리보기용 HTML

## 진행 상황
| 섹션 | Figma node | 상태 |
|---|---|---|
| main-section01 (PC 히어로) | 117:980 | 카니클래스 메인(초안)에서 확인 완료 |

## 라이브클래스 텍스트 에디터 주의사항 (테스트로 확인)
- 에디터(Froala)가 `<img>`의 `position`·`margin`·`display`를 지우고 `fr-dib` 여백(5px)을 넣음 → 이미지는 `div` + `background:url()`로 배치
- 사이트 CSS가 `h1~h6` 폰트를 `!important`로 Pretendard 고정 → 커스텀 폰트 제목은 `div` 사용
- `role` 등 일부 속성은 저장 시 제거됨
- 블록 안쪽 여백이 위아래 50px → 섹션 최상위에 `margin:-50px 0 -50px calc(50% - 50vw)`로 상쇄, `width:100vw`로 전체 폭
- 원주체(Wonju) 웹폰트는 아직 미적용 (현재 Pretendard로 표시)
