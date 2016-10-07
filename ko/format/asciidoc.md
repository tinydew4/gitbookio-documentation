# AsciiDoc

`2.0.0` 버전 이후, GitBook 은 입력 형식으로 AsciiDoc 을 받아들일 수 있습니다.

형식에 대한 자세한 정보는 [AsciiDoc 구문 빠른 참조](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)를 참조하세요.

마크다운처럼, GitBook 은 구조를 추출하기 위해 특별한 파일을 사용합니다: `README.adoc`, `SUMMARY.adoc`, `LANGS.adoc`, `GLOSSARY.adoc`.

### README.adoc

책의 주요 항목 입니다: 소개. 이 파일은 **선택적이지 않습니다**.

### SUMMARY.adoc

이 파일은 장과 절의 목록을 정의합니다. [마크다운](./chapters.md)처럼, `SUMMARY.adoc` 의 형식은 단순히 링크의 목록입니다. 링크의 이름은 장의 이름으로 사용되며, 대상은 장의 파일에 대한 경로입니다.

절은 부모장에 포함된 목록을 추가하는 것으로 간단하게 정의합니다.

```
= 요약

. link:chapter-1/README.adoc[1장]
.. link:chapter-1/ARTICLE1.adoc[1절]
.. link:chapter-1/ARTICLE2.adoc[2절]
... link:chapter-1/ARTICLE-1-2-1.adoc[1.2.1절]
. link:chapter-2/README.adoc[2장]
. link:chapter-3/README.adoc[3장]
. link:chapter-4/README.adoc[4장]
.. Unfinished article
. Unfinished Chapter
```

### LANGS.adoc

[다국어](./languages.md) 책을 위해, 이 파일은 다르게 지원되는 언어와 번역에 대한 정의에 사용됩니다.

이 파일은 `SUMMARY.adoc` 와 같은 구문을 따릅니다:

```
= 언어

. link:en/[English]
. link:fr/[French]
```

### GLOSSARY.adoc

이 파일은 용어 사전 정의를 위해 사용됩니다. [용어 사전 부분을 보세요](./glossary.md).

```
= 용어

== Magic
Sufficiently advanced technology, beyond the understanding of the observer producing a sense of wonder.

== PHP
대중적은 웹 프로그래밍 언어로, 페이스북같은 큰 웹사이트에 많이 사용됩니다. 1994년에 Rasmus Lerdorf 가 그의 개인 홈페이지를 위해 PHP 를 만들었습니다 (PHP 는 원래 개인 홈 페이지를 상징하지만 지금은 "PHP: 하이퍼텍스트 전처리기" 의 약자입니다).
```



