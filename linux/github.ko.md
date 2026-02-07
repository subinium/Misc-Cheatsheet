## Github Profile Badge List

- github repo에 본인 계정명으로 repo를 만들면 프로필이 생성된다.
- 사용할 수 있는 배지 리스트 
  - 배지 사용하기 [shields.io](https://shields.io/)
  - 아이콘 사용하기 [simpleicons](https://simpleicons.org/)
  - 조회수 확인 [Hits](https://hits.seeyoufarm.com/)
  - 깃헙 통계 [github-readme-stats](https://github.com/anuraghazra/github-readme-stats)
  - daily coding [productive-box](https://github.com/maxam2017/productive-box)
  - Pinned Gist [awesome-pinned-gists](https://github.com/matchai/awesome-pinned-gists)
  - boj/solved-ac 배지 [mazassumnida](https://github.com/mazassumnida/mazassumnida)
  - kaggle 배지 [kaggle-badge](https://github.com/subinium/kaggle-badge)
  - 코드 퀄리티 [codefactor](https://www.codefactor.io/)
- 깃헙 공식 아이콘
  - github topic에서 아이콘 링크 사용 가능 [github topic](https://github.com/topics)

## 브랜치를 만들면서 바로 체크아웃하려면 (`git checkout -b`)

- 다음 과정을 한 번에 진행
  - git branch <브랜치명>
  - git checkout <브랜치명>

``` sh
git checkout -b <branch_name>
```

## 커밋 날짜 바꾸기(`git commit --amend --no-edit --date`)

- 마지막 커밋 날짜를 수정하는 가장 간단한 코드
- 오늘로 바꾸고 싶다면 날짜 텍스트 대신 `$(date)`으로 변경 가능
- 1일1커밋러에게 추천

```
git commit --amend --no-edit --date "Sat 1 Jan 2022 00:00:00 KST"
```

## 한글 에러 방지(`core.precomposeunicodem`, `core.quotepath`) 

- 깃에서 한글 작성에서 에러가 발생함을 방지하기 위한 설정
- 한글 작성 가능 + 파일명이 깨지지 않기

```
git config --global core.precomposeunicode true
git config --global core.quotepath false
```