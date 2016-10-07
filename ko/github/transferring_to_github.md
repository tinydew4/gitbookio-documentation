# GitHub 로 콘텐츠 전송

GitBook 에서 책 쓰기를 시작하였고 이제 그 소스를 GitHub 에서 유지하길 원한다면, 걱정하지 마세요. 간단합니다.

#### GitHub 가져오기 도구 사용

1. GitHub 의 **가져오기 도구** 사용:  [import.github.com/new](https://import.github.com/new)
2. GitBook git 주소 입력. 예: `https://git.gitbook.com/MyName/MyBook.git` (이 주소는 책 설정에서 찾을 수 있습니다).
3. GitHub 저장소 이름 입력
4. 메세지가 표시되면 GitBook 자격 증명 입력 (암호 대신 API 토큰을 사용할 수 있습니다).
5. 완료!

콘텐트가 GitHub 로 전송이 완료되면, GitBook 이 GitHub 를 통해 계속 책을 빌드할 수 있도록 통합을 설정할 수 있습니다: [GitHub 통합](./README.md)


#### 명령줄 사용하기

GitHub 의 저장소를 생성한 후에 다음을 수행합니다.

**주의:** 이 작업은 git 히스토리를 덮어쓸 것 입니다.

```
# GitBook 저장소 복제 (사용자명과 암호를 입력해야할 것 입니다)
$ git clone https://git.gitbook.com/MyName/MyBook.git ./mybook

# 복제된 책으로 들어가기
cd ./mybook

# Github 에 밀어넣기
$ git push https://github.com/username/repo.git master --force
```