# 일반적인 오류

일반적인 빌드 오류와 관련 수정 사항의 목록입니다.

---------

```
Error loading plugins: plugin1, ...
```

GitBook 이 플러그인을 확인할 수 없기 때문에 발생합니다 (또는 플러그인이 잘못된 경우).
외부 플러그인은 `gitbook install` 을 사용하여 설치해야합니다.

몇몇 플러그인은 다른 버전의 GitBook 을 필요로 하기 때문에 로드할 수 없을 수 있습니다. 이경우, 사용중인 GitBook 버전을 지원하는 플러그인 버전을 찾아서 `book.json` 에 정의해야 합니다.

```
{
    "plugins": ["myPlugin@1.2.3"]
}
```

---------

```
Need to install ebook-convert from Calibre
```


프로젝트를 PDF, ePub, mobi 전자책으로 빌드하는동안 오류를 극복하려면, [Calibre](http://calibre-ebook.com) 전자책 리더/관리자와 명령줄 도구가 설치되있어야 합니다.

MAC 버전에서 Calibre 명령줄 도구를 설치하기 위해, 메뉴에서 선택하세요: **calibre - Preferences - Miscellaneous - Install command line tools**

완료되면, 전자책 빌드는 성공할 것 입니다.

---------
