## scp로 서버 간 파일 전송하기

- `-p`는 port 번호 지정
- `-r`는 디렉토리 단위일 때
- source와 target은 꼭 본인 서버가 아니어도 되므로 알고 있으면 좋음

``` sh
ssh -p <port> [-r] source target
```

## 외부 localhost 접속하기 (ngrok)

- 개발 단위에서는 localhost에서 특정 포트에 서버가 열림 (웹, 주피터 노트북)
- 이를 현재 개발 환경에서 열기 위해 사용하는 명령어
- vscode에서 ssh로 직접 연결하면, 이런 과정이 필요 없음

``` sh
ngrok http <port>
```

## 서버 password 변경하기 (passwd)

- 해당 명령어를 치면 기존 서비스와 같이 비밀번호 변경가능

```
passwd
```