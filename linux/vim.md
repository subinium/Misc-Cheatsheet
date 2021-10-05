## vimrc setting

```
set number  "line number
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