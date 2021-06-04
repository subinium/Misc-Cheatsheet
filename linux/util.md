## 노트북을 덮거나 시간이 지나도 꺼지지 않게 (caffeinate)

- 전처리 작업 등을 local에서 할 때, 꺼지지 않게
- 원격 서버라면 `tmux`를 사용하면 됨

``` sh
caffeinate
```

## 파일 개수를 알고 싶다면? (`ls -l | grep ^- | wc -l`)

``` sh
ls -l | grep ^- | wc -l
```