#  GitBook 검색

GitBook 의 수천권의 책 중 원하는 것을 찾기 위해 [우리의 강력한 검색 도구](https://www.gitbook.com/search)를 사용할 수 있습니다.

GitBook 을 검색할 때, 특정 숫자와 단어에 일치하는 쿼리를 구성할 수 있습니다.


### 텍스트 검색

기본적으로, GitBook 은 쿼리의 키워드와 관련된 책을 찾습니다. 예를 들어 `javascript angular` 는 "javascript" 와 "angular" 를 포함하는 책을 반환합니다.

### 특정 단어가 포함 된 결과 제외

`NOT` 구문으로 단어를 제외하여 결과를 좁힐 수 있습니다. `Hello` 검색은 많은 수의 "Hello World" 프로젝트를 반환합니다. 그러나 `hello NOT world` 로 검색을 변경하면 적은 결과를 반환합니다.

### 특정 필드 값에 대한 쿼리

특정 필드 값을 가진 책을 걸러낼 수 있습니다. 예를 들어: [license:apache-2](https://www.gitbook.com/search?q=license%3A%22apache-2%22) 는 Apache 2 라이센스를 가지는 책의 목록을 반환합니다.

### 다른 값보다 작은/큰 값에 대한 쿼리

"초과" 와 "이상" 을 나타내기 위해 각각 `>` 과 `>=` 를 사용할 수 있습니다. 예를 들어, 다음 검색 쿼리는 동일합니다: `cats stars:">10"` 과 `cats stars:">= 11"`

"미만" 과 "이하" 를 나타내기 위해 각각 `<` 과 `<=` 을 사용할 수 있습니다.





