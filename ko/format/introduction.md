# Readme 와 소개

책의 첫 페이지는 `README.md` 에서 가져옵니다. 이 파일이 `SUMMARY` 에 없다면, 가장 첫 엔트리로 추가될 것 입니다.

### README.md 대신 다른 파일 사용하기

GitHub 에서 호스팅되는 몇몇 책은 README.md 를 책의 소개 대신 프로젝트의 소개로 유지하기를 선호합니다.

GitBook `>2.0.0` 이후, `book.json` 에서 README 로 사용할 파일을 정의할 수 있습니다.

```js
{
    "structure": {
        "readme": "myIntro.md"
    }
}
```

**주의:** 소개 파일은 책의 루트 디렉토리에 있어야 합니다.
