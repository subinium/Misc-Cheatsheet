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
jq . test.json
```

## 폰트 추천 (`D2 Coding`)

- 개발 폰트 추천
- [naver/d2codingfont](https://github.com/naver/d2codingfont)

## 간략한 man 페이지 (`tldr`)

- 커뮤니티 기반의 실용적 예제 중심 man 페이지
- `man`보다 훨씬 읽기 쉬움

``` sh
brew install tldr
tldr tar
```

## 퍼지 파인더 (`fzf`)

- https://github.com/junegunn/fzf
- 파일, 명령어 히스토리 등을 대화형으로 검색
- Ctrl+R(히스토리), Ctrl+T(파일 검색) 통합

``` sh
brew install fzf
```

## 모던 ls 대체 (`eza`)

- https://github.com/eza-community/eza
- 색상, 아이콘, git 상태를 보여주는 현대적 `ls` 대체
- 아이콘 표시를 위해 [Nerd Font](https://www.nerdfonts.com/) 필요 (예: `brew install --cask font-fira-code-nerd-font`)

``` sh
brew install eza
eza -la --icons --git
```

추천 alias:

```sh
alias ls='eza --icons'
alias ll='eza -la --icons --git'
alias lt='eza --tree --level=2 --icons'
```

## 모던 find 대체 (`fd`)

- https://github.com/sharkdp/fd
- `find`보다 빠르고 직관적인 파일 검색
- `.gitignore`를 기본으로 존중

``` sh
brew install fd
fd "\.json$"          # 모든 .json 파일 찾기
fd -e py              # 모든 .py 파일 찾기
fd -H config          # 숨김 파일 포함 검색
```

## 스마트 cd (`zoxide`)

- https://github.com/ajeetdsouza/zoxide
- 자주 가는 디렉토리를 학습하고 `z` 명령으로 점프
- `cd`, `autojump`, `fasd`, `z.sh` 대체

``` sh
brew install zoxide
eval "$(zoxide init zsh)"    # .zshrc에 추가
z projects                   # "projects"와 매칭되는 가장 자주 방문한 디렉토리로 이동
zi                           # fzf를 이용한 대화형 선택
```

## git diff를 보기 좋게 (`delta`)

- https://github.com/dandavison/delta
- syntax highlighting, 줄 번호, side-by-side 뷰 지원

``` sh
brew install git-delta
```

`~/.gitconfig`에 추가:

```ini
[core]
    pager = delta
[interactive]
    diffFilter = delta --color-only
[delta]
    navigate = true
    side-by-side = true
[merge]
    conflictstyle = zdiff3
```

## 쉘 히스토리 검색 (`atuin`)

- https://github.com/atuinsh/atuin
- Ctrl+R을 대체하는 강력한 히스토리 검색 (SQLite 기반)
- 퍼지 검색, 디렉토리/세션별 필터링, 기기 간 동기화 지원

``` sh
brew install atuin
eval "$(atuin init zsh)"     # .zshrc에 추가
```

## 터미널 git UI (`lazygit`)

- https://github.com/jesseduffield/lazygit
- staging, 브랜치, rebase, stash 등을 한 화면에서 관리하는 git TUI

``` sh
brew install lazygit
lazygit
```

## 시스템 모니터 (`btop`)

- https://github.com/aristocratos/btop
- CPU, 메모리, 디스크, 네트워크, 프로세스를 한눈에 보는 TUI
- `top`, `htop` 대체

``` sh
brew install btop
btop
```

## 디스크 사용량 시각화 (`dust`)

- https://github.com/bootandy/dust
- `du`보다 직관적인 디스크 사용량 시각화

``` sh
brew install dust
dust            # 현재 디렉토리
dust /home      # 특정 경로
```