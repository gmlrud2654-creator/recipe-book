# 나빈님 전용 레시피북 🍳

재료·분류로 찾는 가족 레시피 노트.

- 주소: https://gmlrud2654-creator.github.io/recipe-book/
- 앱 파일: `index.html` (한 파일로 동작)
- 테스트: `node core.test.js`

## 저장 방식
- 로그인하지 않아도 이 기기 브라우저에 저장됩니다. (localStorage)
- 로그인하면 Firestore `families/{uid}/shared/recipeBook` 문서에 저장되어 폰·태블릿이 같은 목록으로 맞춰집니다.
  - 가족 대시보드(`shared/dashboard`), 후기관리(`shared/reviewCalendar`)와는 다른 문서라 기존 데이터는 건드리지 않습니다.
  - 여러 기기가 동시에 고쳐도 3-way 병합으로 서로의 변경을 지우지 않습니다.
  - 기기별 최근 5개 자동 백업 + `💾 백업에서 되돌리기`.
