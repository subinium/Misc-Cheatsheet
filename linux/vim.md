##  (vimrc) 문서 형식 파악 및 문법 하이라이트(`syntax on`, `filetype indent plugin on`)

- 별도 플러그인 없이 기본 문법 하이라이트

```
syntax on
filetype indent plugin on
```

##  (vimrc) 검색, 괄호 등 정보 하이라이트(`hlsearch`, `ruler`, `showmatch`)

- `hlsearch` : 검색 시, 결과 하이라이트
- `ruler` : 현재 작성 줄 정보 표기
- `showmatch` : 매칭되는 괄호 표시

```
set hlsearch
set ruler
set showmatch
```

## (vimrc) Python 문서 작성에 편리한 모드(tab 사이즈, indentation)

- 기본 tab size 조정
- auto indentation과 indent 조정

```
set tabstop=4
set softtabstop=4
set shiftwidth=4
set autoindent
```

## (vimrc) 라인 번호 표기

- line number 표기

```
set number  "line number
```

## (vimrc) 모드별 커서 모양 변경

```
" cursor shap
let &t_SI = "\<Esc>]50;CursorShape=1\x7" " Vertical bar in insert mode
let &t_EI = "\<Esc>]50;CursorShape=0\x7" " Block in normal mode
let &t_SR = "\<esc>]50;CursorShape=2\x7" " Underline in replace mode
```

## vim에서 여러 줄 주석 처리 (`norm i#`, `norm 1x`)

- visual mode에서 원하는 부분 선택
- 이후 norm을 사용하여 `#`을 줄 맨 앞에 삽입
- 언어에 따라 `#` 외의 표현 사용 가능

```
:norm i#
```

- 주석 삭제는 다음과 같이 문장의 첫 단어 삭제
- 1 대신 다른 숫자를 넣어 n개의 문자 삭제 가능

```
:norm 1x
```

## vim에서 sudo로 저장하기 (`w sudo! tee %`)

- vi로 켰는데 갑작스럽게 권한이 없어서 저장이 어렵다면?
- 각 명령어 설명
  - `w` : 쓰기
  - `!sudo` : 루트 권한
  - `tee` : stdin으로 전달
  - `%` : 현재 파일명 대체

```
:w sudo! tee %
```