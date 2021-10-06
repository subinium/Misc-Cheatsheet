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