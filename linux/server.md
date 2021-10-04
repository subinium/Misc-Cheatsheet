## 서버 간 파일 전송하기 (`scp`)

- `-p`는 port 번호 지정
- `-r`는 디렉토리 단위일 때
- source와 target은 꼭 본인 서버가 아니어도 되므로 알고 있으면 좋음

``` sh
ssh -p <port> [-r] <source> <target>
```

## 외부 localhost 접속하기 (`ngrok`)

- 개발 단위에서는 localhost에서 특정 포트에 서버가 열림 (웹, 주피터 노트북)
- 이를 현재 개발 환경에서 열기 위해 사용하는 명령어
- vscode에서 ssh로 직접 연결하면, 이런 과정이 필요 없음

``` sh
ngrok http <port>
```

## 서버 password 변경하기 (`passwd`)

- 해당 명령어를 치면 기존 서비스와 같이 비밀번호 변경가능

```
passwd
```

## remote server의 port를 localhost에서 사용하기(`ssh -L` or `ssh -R`)

- **ssh 터널링**이라고도 함
- remote server에서 실행하는 다양한 일들(tensorboard, local 등)을 실행하고 웹서버를 localhost로 키게 될때 사용
- 원래는 remote server의 localhost였으나 local에서 열 수 있음
- `-L`은 local forwarding, `-R`은 dynamic forwarding인데, 이는 방화벽과 연결 방법에 따라 다르다.

```
ssh -L <local port>:localhost:<remote port> subinium@<remote server>
```

## 서버의 GUI를 Mac에서 연동하기 (`ssh -X` or `ssh -Y`)

- 서버의 GUI를 실행하기 위해서는 `ssh`에서 `-X`나 `-Y`를 사용하면 된다.
- 둘 다 X11 Forwarding을 사용한다.
- Mac에서는 일부 설정이 필요하다.
  - XQuartz 설치
  - ssh config 변경
- 각 모드는 [이런 차이점](https://askubuntu.com/questions/35512/what-is-the-difference-between-ssh-y-trusted-x11-forwarding-and-ssh-x-u)이 있다고 한다.

```
ssh -X
ssh -Y
```

## 서버 ssh-key로 password없이 접속하기 (`ssh-keygen`)

- ssh 접속 시에 매번 password를 적는 것보다 ssh-key를 미리 생성해두면 좋다.
- key의 종류는 다양하지만 일반적으로 rsa 4096을 많이 사용한다.
- `.pub` 파일을 접속하는 서버에 보내야 하는 데, 이때 `ssh-copy-id`를 사용한다.

```
ssh-keygen -t rsa -b 4096 
ssh-copy-id -i ~/.ssh/id_rsa_name.pub username@server -p port_num
```

## ssh config 파일 설정으로 간단하게 접속하기 (`~./ssh/config`)

- [ssh config](https://www.ssh.com/academy/ssh/config) 설정은 다양하게 할 수 있음
- `~./ssh/`에 `config`파일을 수정하여 접속을 간단하게 할 수 있음
- 다음과 같은 형태로 config에 작성 (여러 서버작성 가능)

```
Host host_name
    HostName xxx.xxx.xxx.xxx
    User username
    Port 1234
    IdentityFile ~/.ssh/id_rsa_name
```

- host_name은 자유롭게
- ssh-keygen과 함께 사용하면 더 좋음 (IdentityFile)
- 설정을 하면 다음과 같이 서버명, 유저명, 포트명, 패스워드 없이 바로 접속가능

```
ssh host_name
```