# 책 표지

- `cover.html`: 표지 원본 (1200×1600). 이 폴더에서 `npm i @fontsource/noto-serif-kr@5.1.1 @fontsource/noto-sans-kr@5.1.1` 로 글꼴을 받은 뒤 렌더링합니다.
- `shot.js`: Playwright로 PNG를 만듭니다. `node shot.js $PWD/cover.html $PWD/../../docs/assets/cover.png`
