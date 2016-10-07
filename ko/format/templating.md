# 템플릿

이것은 GitBook 에서 가능한 템플릿 기능의 개요입니다. GitBook 은 [Nunjucks](https://mozilla.github.io/nunjucks/) 와 [Jinja2](http://jinja.pocoo.org/) 구문을 사용합니다..

### 탈출

특별한 템플릿 태그를 출력하고 싶다면, raw 를 사용하고 그 안에 명시하세요. 일반 텍스트로 출력될 것입니다.

```
{% raw %}
  이것은 {{ 처리되지 않을 것 }} 입니다
{% endraw %}
```

### 변수

변수는 이 책의 문맥에서 값을 찾습니다.

변수는 `book.json` 파일에 정의되어있습니다:

```json
{
    "variables": {
        "myVariable": "Hello World"
    }
}
```


#### 변수 표시

`book.json` 에 명시된 변수는 `book` 범위에서 접근할 수 있습니다:

```
{{ book.myVariable }}
```

이것은 책 변수에서 `myVariable` 을 찾고 그것을 표시합니다. 그들의 속성을 조회하기 위해 변수 이름은 점을 가질 수 있습니다. 또한 대괄호 구문을 사용할 수 있습니다.

```
{{ book.foo.bar }}
{{ book["bar"] }}
```

값이 정의되지 않았으면 아무것도 표시되지 않습니다. 다음은 `foo` 가 정의되지 않으면 아무 결과도 나타내지 않습니다: `{{ foo }}`, `{{ foo.bar }}`, `{{ foo.bar.baz }}`.


#### 문맥 변수

몇몇 변수는 현재 파일 또는 GitBook 인스턴스에 대한 정보를 얻을 수 있습니다.

| 이름 |    설명     |
| ---- | ----------- |
| `file.path` | 책과 연관된 파일의 경로 |
| `file.mtime` | 파일의 마지막 수정된 날짜 |


### 태그

태그는 템플릿의 섹션에 대한 작업을 수행하는 특별한 블록입니다.

#### If

**if** 는 조건을 확인하여 내용을 선택적으로 보여줍니다. 그것은 프로그래밍 언어의 if 와 같이 동작합니다.

````
{% if variable %}
  참입니다
{% endif %}
```

`variable` 이 정의되있고 평가가 true 이면, "참입니다" 가 표시됩니다. 그외에는 아무것도 발생하지 않습니다.

elif 와 else 를 통해 다른 조건을 명시할 수 있습니다:

```
{% if hungry %}
  나는 배가고파요
{% elif tired %}
  나는 지쳤어요
{% else %}
  난 괜찮아요!
{% endif %}
```

#### for

**for** 는 배열과 사전을 반복합니다.

`book.json` 의 변수를 살펴봅시다:
```
{
    "variables": {
        "authors": [
            { "name": "Samy" },
            { "name": "Aaron" }
        ]
    }
}
```

```
# 저자


{% for author in book.authors %}
  - {{ author.name }}
{% endfor %}
```

위의 예제는 표시 값으로 `authors` 의 각 항목의 `name` 속성을 사용하여 모든 저자를 나열합니다.

#### include

Include 는 [내용 참조](./conrefs.md) 글에 자세히 나와있습니다.
