# 문서 가져오기

GitBook 에 기존 문서를 쉽게 가져올 수 있습니다. 책을 만들때 `Import` 탭에서 업로드하세요.

### 허용 형식

| 형식 | 확장자 |
| ---- | ------ |
| Microsoft 워드 문서 | `.docx` |
| DocBook v5.x | `.xml` |
| HTML 파일 | `.html` |

이 기능을 최대한 사용하려면, 다음을 권장합니다:
* Microsoft 워드 2007 이상 문서
* DocBook v5.x 문서

4 버전의 DocBook 를 가지고 있다면, 최적의 호환성을 위해 5 버전으로 [자동 변환](http://doccookbook.sourceforge.net/html/en/dbc.structure.db4-to-db5.html)을 고려하세요.

### 변환

가져오기 기능은 [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) CLI 유틸리티를 사용합니다. 이 모듈은 `SUMMARY.md` 의 생성과 함께 원본 문서를 마크다운 파일로 변환하는 것의 모든 측면을 담당합니다.

[gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 는 문서의 구조를 기반으로 큰 문서를 장과 절로 나눕니다. 그러므로, 각 원본 문서의 첫번째 단계의 헤더는 장으로 변환됩니다. 장이 두번째 단계의 헤더를 가지고 있으면, 이 장을 위해 파일 대신 폴더가 생성됩니다. 이 폴더는 각 절을 포함합니다.

장의 폴더에서, 장 서문을 가지는 `README.md` 파일이 생성됩니다. 처음으로 오는 두번째 단계의 헤더 이전의 내용은 장 서문으로 간주됩니다. 동일한 규칙으로 처음으로 오는 첫번째 단계의 헤더 이전의 내용은 책의 서문으로 사용됩니다.

`.docx` 문서를 위해, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 는 모든 포함된 이미지를 `assets/` 폴더로 내보냅니다.

더 많은 유연성을 필요로하면, [gitbook-convert](https://github.com/GitbookIO/gitbook-convert) 을 로컬에서 사용하는 을 고려해보세요. 저장소를 생성하고 Git 또는 GitHub 를 통해 가져오세요.

### 문제 해결

우리는 당신의 책이나 다른 질문들에 대해 기꺼이 돕겠습니다. [github.com/GitbookIO/gitbook-convert](https://github.com/GitbookIO/gitbook-convert/issues) 으로 질문이나 이슈를 보낼 수 있습니다.
