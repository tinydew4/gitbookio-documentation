# 환경 설정

모든 환경 설정은 `book.json` 이름의 파일안에 JSON 으로 저장됩니다.

[jsonlint.com](http://jsonlint.com) 에 `book.json` 을 붙여넣기하여 JSON 구문의 유효성 검사를 할 수 있습니다.

모든 필드는 선택항목이거나 일부 추출된 값을 기본으로 합니다.


## 필드

#### gitbook

```js
{ "gitbook": "2.x.x" }
```

이 옵션은 책 생성에 사용될 GitBook 의 버전을 찾는데 사용됩니다.
형식은 [SEMVER](http://semver.org) 조건을 따릅니다.

#### title

```js
{ "title": "내 멋진 책" }
```

이 옵션은 책의 제목을 정의합니다. 기본적으로 이 값은 **README** 에서 추출됩니다 (첫 제목).

**gitbook.com** 에서, 이 값은 플랫폼에서 입력된 제목으로 정의됩니다.

#### description

```js
{ "description": "이것은 좋은 책입니다!" }
```

이 옵션은 책의 설명을 정의합니다. 기본적으로 이 값은 **README** 에서 추출됩니다 (첫번째 단락).

**gitbook.com** 에서, 이 값은 플랫폼에서 입력된 설명으로 정의됩니다.

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

이 옵션은 책과 연관된 ISBN 을 정의합니다.

#### language

```js
{ "language": "fr" }
```

이 옵션은 책의 언어를 정의합니다. 기본값은 `en` 입니다.

이 옵션은 국제화와 지역화에 사용되며, 웹사이트에서 텍스트를 변경합니다.

**gitbook.com** 에서, 이 값은 내용에서 검출되거나 설정에 명시된 언어로 정의됩니다.

#### direction

```js
{ "direction": "rtl" }
```

이 옵션은 언어의 텍스트 방향을 재정의하는데 사용됩니다.
올바른 텍스트 방향 대신에 `language` 필드에 언어를 설정하는 것이 좋습니다.

#### styles

이 옵션은 책에 사용자 정의 css 를 추가하는데 사용됩니다.

예시:

```js
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

#### plugins

```js
{ "plugins": ["mathjax"] }
```

책에서 사용되는 플러그인 목록은 `book.json` 환경 설정에 정의되어 있습니다.

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

이 옵션은 모든 플러그인의 특정 환경 설정을 포함합니다.

#### 구조

이 옵션은 GitBook 에서 사용하는 파일 경로를 재정의합니다.

`README.md` 대신 `INTRO.md` 를 사용하는 예시입니다:

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

구조의 유형은 `readme`, `langs`, `summary`, `glossary` 가 있습니다.

#### 변수

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

이 옵션은 [템플릿](./templating.md)에서 사용되는 변수 값을 정의합니다.

#### pdf

PDF 명시 옵션은 헤더, 푸터 등등의 사용자 정의를 허용합니다.

```js
{
    "pdf": {
        "headerTemplate": "Header of the PDF with _TITLE_",
        "footerTemplate": "Footer HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_."
    }
}
```
