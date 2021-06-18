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
bat <file>
```