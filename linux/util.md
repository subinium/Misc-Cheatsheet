## 노트북을 덮거나 시간이 지나도 꺼지지 않게 (`caffeinate`)

- 전처리 작업 등을 local에서 할 때, 꺼지지 않게
- 원격 서버라면 `tmux`를 사용하면 됨

``` sh
caffeinate
```

## 파일 개수를 알고 싶다면? (`ls -l | grep ^- | wc -l`)

``` sh
ls -l | grep ^- | wc -l
```

## 디스크의 남은 용량을 알고 싶다면 (`df -h`)

- 리눅스 시스템 전체의 디스크 사용량을 알 수 있음
- `-h` 옵션은 Mb, Gb 단위로 바꿔서 확인해주는 옵션

``` sh
df -h
```

## Syntax Highlight와 함께 cat을 쓰고 싶다면 (`bat`)

- cat과 유사하지만 syntax highlight가 적용되어 출력하는 명령어

``` sh
brew install bat
bat <file>
```

팁으로 이걸 cat에 alias하면 좋습니다.

```
alias cat="bat"
```

## iterm에서 new tab을 만들 때 directory를 유지하고 싶다면?

- iterm preferences > Profiles > Working Directory > Advanced Configuration에서 edit
- Working Directory for New Tabs를 Reuse previous sessions's directory로 변경

## 심볼릭 링크 사용하여 바로가기 만들기(`ln -s`)

- 바로가기를 만드는 것이다.

``` sh
ln -s [target path] [source path]
```

## pip로 설치 시, 필요없는 output을 보지 않으려면? (`pip install`의 `-q`, `-qq`, `-qqq`)

- jupyter notebook에서 pip로 라이브러리 설치 시, output 때문에 내용이 보기 어려운 경우가 많다.
- 물론 shell에서도 마찬가지.
- 이럴 때는 `-q`, `-qq`, `-qqq` 옵션을 주어 output을 생략할 수 있다.
  - `-q` : WARNING,ERROR,CRITICAL 
  - `-qq` : Error, CRITICAL
  - `-qqq` : CRITICAL

```
pip install -qqq <library>
```

## tmux에서 마우스 사용하기(`set -g mouse on`)

- tmux에서 마우스를 사용하기 위해 `.tmux/.tmux.conf.local`에서 주석처리 제거

```
# start with mouse mode enabled
set -g mouse on
```

## json 파일 이쁘게 보기 (`jq`)

- json을 이쁘게 보여줌

```
brew install jq
jq test.json
```

## 폰트 추천 (`D2 Coding`)

- 개발 폰트 추천
- [naver/d2codingfont](https://github.com/naver/d2codingfont)