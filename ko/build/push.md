# GIT 을 이용한 책 갱신

**gitbook.com** 에서 책을 만들 때, 몇가지 컨텐츠를 밀어넣을 필요가 있습니다. 이렇게 하려면, 웹 편집기 또는 명령줄을 사용할 수 있습니다.

명령줄에서 책을 갱신하려면, [GIT](http://git-scm.com) 을 사용해 컨텐트를 밀어넣을 수 있습니다:

### GIT 주소

각 책은 Git HTTPS 주소로 연결됩니다. GitBook 의 git 서버에서 ssh 규약은 아직 지원되지 않습니다.

git 주소 형식은 다음과 같습니다:

```
https://git.gitbook.com/{{UserName}}/{{Book}}.git
```

### 인증

git 서버는 인증에 기본 GitBook 로그인을 사용하고 있습니다. 메세지가 ㅍ시되면 GitBook 사용자명과 암호를 입력하세요 (API 토큰을 사용할 수 있습니다).

### 자격 증명 저장

매번 암호를 입력하지 않으려면, `~/.netrc` 파일에 GitBook 자격 증명을 추가할 수 있습니다. `~/.netrc` 파일을 생성하거나 기존파일에 다음을 추가하세요:

```
machine git.gitbook.com
  login USERNAME-or-EMAIL
  password API-TOKEN-or-PASSWORD
```

보안상의 이유로 **API 토큰**을 사용하는 것이 좋습니다. ["API"의 설정에서](https://www.gitbook.com/settings#api) 찾을 수 있습니다.

### 명령줄에서 새 저장소 만들기

```
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```

### 기존 저장소에 밀어넣기

```
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master
```
