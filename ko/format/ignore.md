# 파일과 폴더 무시

GitBook 은 건너뛸 파일과 폴더의 목록을 얻기 위해 `.gitignore`, `.bookignore`, `.ignore` 파일을 읽을 것 입니다.

해당 파일의 내부 형식은 `.gitignore` 와 같은 규칙을 따릅니다:

```
# 주석입니다

# test.md 파일 무시
test.md

# "bin" 디렉토리의 모든 것 무시
bin/*
```