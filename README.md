# Misc Cheatsheet

이 레포는 다음과 같은 내용을 포함하고 있습니다.

- 연구실 생활을 하다보면 나만 모르고 있는 것 같은 코드와 다른 사람에게 추천해주고 싶은 조각 지식 모음집.
- 주니어분들에게 추천하고 싶은 자료들

## Linux 

### [Server](linux/server.md)

- 서버 간 파일 전송하기 (`scp`)
- 외부 localhost 접속하기 (`ngrok`)
- 서버 password 변경하기 (`passwd`)
- remote server의 port를 localhost에서 사용하기(`ssh -L` or `ssh -R`)
- 서버의 GUI를 로컬에서 사용하기 (`ssh -X` or `ssh -Y`)
- 서버 ssh-key로 password없이 접속하기 (`ssh-keygen`)
- ssh config 파일 설정으로 간단하게 접속하기 (`~./ssh/config`)

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
- 심볼릭 링크 사용하여 바로가기 만들기(`ln -s`)
- pip로 설치 시, 필요없는 output을 보지 않으려면? (`pip install`의 `-q`, `-qq`, `-qqq`)

### [Vim](linux/vim.md)

- **[vimrc 통합본](/linux/.vimrc)**
- (vimrc) 문서 형식 파악 및 문법 하이라이트(`syntax on`, `filetype indent plugin on`)
- (vimrc) 검색, 괄호 등 정보 하이라이트(`hlsearch`, `ruler`, `showmatch`)
- (vimrc) Python 문서 작성에 편리한 모드(종류별 tab 사이즈, `autoindent`)
- (vimrc) 라인 번호 표기(`nu` or `number`)
- (vimrc) 모드별 커서 모양 변경
- vim에서 여러 줄 주석 처리 (`norm i#`, `norm 1x`)

## Data Science

### Computer Vision

- [albumtations](https://github.com/albumentations-team/albumentations) : Image data augmentation library
- [ttach](https://github.com/qubvel/ttach) : Image Test Time Augmentation with PyTorch
- [timm](https://github.com/rwightman/pytorch-image-models) : Pytorch pre-trained SOTA image models
- [smp](https://github.com/qubvel/segmentation_models.pytorch) : Pytorch pre-trained SOTA image segmentation models

### Prototype

- [Streamlit](https://github.com/streamlit/streamlit) : ML Model을 Web-based GUI로 쉽게 보여주는 오픈소스
- [Gradio](https://github.com/gradio-app/gradio) : ML Model을 Web-based GUI로 쉽게 보여주는 오픈소스

## Web

### [Git/Github](web/github.md)

- Github Profile Badge List : 깃헙을 다양하게 꾸며봅시다.
- 브랜치를 만들면서 바로 체크아웃하려면 (`git checkout -b`)

### [Flask](web/flask.md)

- Flask에 캐시가 쌓여 새로고침이 안된다면?

### Library & Service

- [Vercel](https://vercel.com/) : 쉬운 배포 서비스
- [Tailwind UI](https://tailwindui.com/) : 유틸리티 우선 CSS Framework 
- [Headless UI](https://headlessui.dev/) : Tailwind UI와 함께 사용할 수 있는 UI Components
- [Reactour](https://github.com/elrumordelaluz/reactour) : react에서 onboarding을 도와주는 패키지
- [react-i18next](https://github.com/i18next/react-i18next) : react 다국어처리 패키지

## Tool

### Website

- [Thesaurus.com](https://www.thesaurus.com/) : 유의어 사전
- [Grammarly](https://app.grammarly.com/) : 문법 체크
- [flaticon](https://www.flaticon.com/) : 저작권 free 아이콘
- [Unsplash](https://unsplash.com/) : 저작권 free 이미지
- [dafont.com](https://www.dafont.com/) : 저작권 free 영어 폰트
- [carbon](https://carbon.now.sh/) : 코드 공유 이쁘게 만들어주는 사이트
- [2 Color Combinations](https://2colors.colorion.co/) : 시각화/UI에서 2색 조합을 살펴볼 때 유용한 사이트

### Extension

- [Arxive](https://chrome.google.com/webstore/detail/arxive/hkoblclipggkhhbllgefhnbjdcajmelh/related?hl=ko) : Arxiv 논문 제목을 연도가 아닌 제목-저자 형식으로 바꿔주는 툴
- [Google Scholar Button](https://chrome.google.com/webstore/detail/google-scholar-button/ldipcbpaocekfooobnbcddclnhejkcpn?hl=en) : google scholar 검색을 extension 상에서 할 수 있음.

### Application

- [Mathpix Snip](https://mathpix.com/) : 수식 스크린샷을 LaTex으로 바꿔주는 툴

## Articles & Repo

### Articles

- [오욱환, 학문을 직업으로 삼으려는 젊은 학자들을 위하여](http://home.ewha.ac.kr/~oookwhan/essay/essay2-toyoung.htm) : 대학원생에게 추천하는 글
- [이직초보 어느 개발자의 이력서 만들기](https://techblog.woowahan.com/2531/) : 처음 CV를 작성하는 분들에게 추천하는 글

### Repos

- [Modern Unix](https://github.com/ibraheemdev/modern-unix) : 짱짱 멋진 command 명령어 모음
- [awesome-devteam](https://github.com/leehosung/awesome-devteam) : 좋은 개발팀을 만드는데 도움이 되는 자료 (국문!)

### Books

- [소프트 스킬(존 손메즈 저), 길벗](http://www.yes24.com/Product/Goods/23161141) : 개발자에게 필요한 역량에 대한 다양한 조언을 줄 수 있는 책입니다.