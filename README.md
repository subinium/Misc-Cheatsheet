# Misc Cheatsheet

연구실 생활을 하다보면 나만 모르고 있는 것 같은 컴퓨터 코드를 모아두는 작고 소중한 저장소입니다.

## Linux 

### [Server](linux/server.md)

- 서버 간 파일 전송하기 (`scp`)
- 외부 localhost 접속하기 (`ngrok`)
- 서버 password 변경하기 (`passwd`)
- 서버의 GUI를 로컬에서 사용하기 (`ssh -X` or `ssh -Y`)
- 서버 ssh-key로 password없이 접속하기 (`ssh-keygen`)
- ssh config로 접속 명령어 간단하게 하기 (`~./ssh/config`)

### [GPU](linux/gpu.md)

- 사용 GPU 지정 Python (`CUDA_VISIBLE_DEVICES`)
- CUDA 버전 확인하기 (`nvcc`)
- GPU 사용량 확인하기 (`nvidia-smi`)
- GPU 사용량 확인하기 2 (`nvtop`)

### [Util](linux/util.md)

- 노트북을 덮거나 시간이 지나도 꺼지지 않게 (`caffeinate`)
- 파일 개수를 알고 싶다면? (`ls -l | grep ^- | wc -l`)
- 디스크의 남은 용량을 알고 싶다면 (`df -h`)
- Syntax Highlight와 함께 cat을 쓰고 싶다면 (`bat`)
- iterm에서 new tab을 만들 때 directory를 유지하고 싶다면?

## Web Programming

### [Flask](web_programming/flask.md)

- Flask에 캐시가 쌓여 새로고침이 안된다면?

## Tool

### Website

- [Thesaurus.com](https://www.thesaurus.com/) : 유의어 사전

### Extension

- [Arxive](https://chrome.google.com/webstore/detail/arxive/hkoblclipggkhhbllgefhnbjdcajmelh/related?hl=ko) : Arxiv 논문 제목을 연도가 아닌 제목-저자 형식으로 바꿔주는 툴
- [Google Scholar Button](https://chrome.google.com/webstore/detail/google-scholar-button/ldipcbpaocekfooobnbcddclnhejkcpn?hl=en) : google scholar 검색을 extension 상에서 할 수 있음.

### Application

- [Mathpix Snip](https://mathpix.com/) : 수식 스크린샷을 LaTex으로 바꿔주는 툴

## Article

> 대학원 생활에 도움이 되는 글들.

- [오욱환, 학문을 직업으로 삼으려는 젊은 학자들을 위하여](http://home.ewha.ac.kr/~oookwhan/essay/essay2-toyoung.htm)

---

## Reference

- [Modern Unix](https://github.com/ibraheemdev/modern-unix)
  - 짱짱 멋진 command 명령어 모음
