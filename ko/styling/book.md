# 웹사이트와 전자책 스타일 확장

`styles` 디렉토리에 파일을 생성하여 전자책과 웹사이트에 사용된 css 를 확장할 수 있습니다:

| 형식 | 파일 |
| ---- | ---- |
| `website` | `styles/website.css` |
| `pdf` | `styles/pdf.css` |
| `epub` | `styles/epub.css` |
| `mobi` | `styles/mobi.css` |
| `pdf`, `epub`, `mobi` | `styles/ebook.css` |


이 경로는 `book.json` 환경설정으로 변경할 수 있습니다. 루트 폴더에서 파일을 사용하는 예입니다:

```json
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### CSS 전처리기 사용

CSS 전처리기를  쉽게 사용할 수 있게 해주는 플러그인이 있습니다:

- [styles-less](https://plugins.gitbook.com/plugin/styles-less)
- [styles-sass](https://plugins.gitbook.com/plugin/styles-sass)

