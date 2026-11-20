# 한 권으로 읽는 한국사

선사 시대부터 현대까지 한국사의 큰 흐름을 15개 장과 부록으로 정리한 입문서입니다.
원고는 장마다 Markdown 파일 하나로 되어 있어 **MkDocs(GitHub Pages)** 와 **위키독스** 양쪽에 그대로 옮길 수 있습니다.

## 폴더 구조

```
korean-history-book/
├── mkdocs.yml                  # 사이트 설정과 목차(nav)
├── requirements.txt            # mkdocs, mkdocs-material 버전 고정
├── .github/workflows/deploy.yml# main에 푸시하면 GitHub Pages로 자동 배포
└── docs/
    ├── index.md                # 머리말
    ├── 01-prehistory.md … 15-today.md
    ├── appendix-timeline.md    # 한국사 연표
    └── appendix-references.md  # 참고 문헌
```

## 로컬에서 미리 보기

```bash
pip install -r requirements.txt
mkdocs serve        # http://127.0.0.1:8000
```

## GitHub Pages로 발행하기

1. 이 폴더를 새 GitHub 저장소의 `main` 브랜치에 올립니다.
2. Actions가 `mkdocs gh-deploy`를 실행해 `gh-pages` 브랜치를 만듭니다.
3. 저장소 **Settings → Pages** 에서 소스를 `gh-pages` 브랜치로 지정합니다.

## 위키독스로 옮기기

- 위키독스에서 책을 만든 뒤, `mkdocs.yml`의 `nav` 순서대로 "부(部)"는 상위 페이지, "장"은 하위 페이지로 만듭니다.
- 각 파일 맨 위의 `---`로 둘러싸인 머리말(front matter)은 MkDocs용 메타데이터이므로, 위키독스에 붙여 넣을 때는 **이 부분을 빼고** 본문만 붙여 넣으세요. 페이지 제목은 front matter의 `title` 값을 쓰면 됩니다.
- `!!! note` 형태의 상자(admonition)는 위키독스에서 일반 문단으로 보입니다. 필요하면 인용문(`>`)으로 바꿔도 됩니다.

## 사진에 대하여

- 본문의 사진 23장은 위키미디어 공용의 자유 이용 저작물이며, 이미지 주소(`Special:FilePath`)로 바로 불러옵니다. 그래서 별도 파일 없이 GitHub Pages와 위키독스 양쪽에서 그대로 보입니다.
- 사진마다 캡션에 출처 링크가 있고, 전체 목록은 `docs/appendix-image-credits.md`(사진 출처)에 있습니다. 각 파일의 저작자와 라이선스는 링크된 파일 페이지에서 확인하세요.
- 외부 링크가 끊기는 것이 걱정되면 이미지를 내려받아 `docs/images/`에 두고 주소를 바꾸면 됩니다. 위키독스에서는 편집기의 이미지 업로드 기능을 쓰면 됩니다.
