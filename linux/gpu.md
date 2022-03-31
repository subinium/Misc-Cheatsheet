## 사용 GPU 지정 Python (`CUDA_VISIBLE_DEVICES`)

- 파이썬 실행 시 GPU를 지정하는 방법
- N개를 지정하고 싶다면 `,`로 구분

``` sh
CUDA_VISIBLE_DEVICES=1 python hello.py
CUDA_VISIBLE_DEVICES=1,3 python hello.py
```

## CUDA 버전 확인하기 (`nvcc`)

- CUDA 및 GPU 확인을 위한 기본적인 명령어
- 이게 실행안되면 path 설정 issue
- 아래의 nvidia-smi랑 종종 다른 버전을 말하는 경우가 있는데 보통은 path 문제

``` sh
nvcc --version
```

## GPU 사용량 확인하기 (`nvidia-smi`)

- 기본적으로는 `nvidia-smi`를 사용해서 보면 된다.
- 주기적으로 gpu 사용량을 확인하고 싶다면 아래를 사용하자.

``` sh
nvdia-smi
watch -n 1 nvidia-smi
```

- GPU를 안쓰는 데, 사용량이 많다면 `top`, `ps` 등의 명령어로 process를 찾아 `kill`할 것 

## GPU 사용량 확인하기 2 (`nvtop`)

- https://github.com/Syllo/nvtop
- 위 보다 조금 더 간지나는(?) GPU 모니터링 툴

``` sh
nvtop
```

## GPU 사용량 확인하기 3 (`nvitop`)

- https://github.com/XuehaiPan/nvitop
- 위 보다 조금 더 간지나는(??) GPU 모니터링 툴

``` sh
nvitop
```