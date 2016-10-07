# 장과 절

GitBook 은 장과 절의 구조 정의에 `SUMMARY.md` 를 사용합니다. `SUMMARY.md` 파일은 책의 목차를 생성하는데 사용됩니다.

`SUMMARY.md` 의 형식은 단순히 링크의 목록입니다. 링크의 이름은 장의 이름으로 사용되며, 대상은 장의 파일에 대한 경로입니다.

절은 부모 장에 중첩된 목록을 추가하는 것으로 간단하게 정의됩니다.

### 간단한 예제

```
# 개요

* [1장](chapter1.md)
* [2장](chapter2.md)
* [3장](chapter3.md)
```

### *parts* 로 분리된 절의 예제

```
# 개요

* [I장](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [II장](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

