### ebook-convert 설치

ebook-convert 는 전자책을 생성할 때 필요합니다 (epub, mobi, pdf).

#### Mac

[Calibre 앱](http://calibre-ebook.com/download) 다운로드. `calibre.app` 를 Applications 폴더로 이동한 후에 `ebook-convert` 도구의 심볼릭 링크를 생성하세요:

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

`/usr/bin` 을 `$PATH` 에 있는 디렉토리로 바꿀 수 있습니다.