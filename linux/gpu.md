## Specify GPU for Python (`CUDA_VISIBLE_DEVICES`)

- Specify which GPU to use when running Python
- Use `,` to specify multiple GPUs

``` sh
CUDA_VISIBLE_DEVICES=1 python hello.py
CUDA_VISIBLE_DEVICES=1,3 python hello.py
```

## Check CUDA version (`nvcc`)

- Basic command for checking CUDA and GPU info
- If this doesn't run, it's likely a PATH issue
- Sometimes shows a different version than `nvidia-smi`; this is usually also a PATH issue

``` sh
nvcc --version
```

## Monitor GPU usage (`nvidia-smi`)

- Use `nvidia-smi` for basic GPU monitoring
- To check GPU usage periodically, use the command below

``` sh
nvidia-smi
watch -n 1 nvidia-smi
```

- If GPU memory is occupied but not in use, find the process with `top` or `ps` and `kill` it

## Monitor GPU usage 2 (`nvtop`)

- https://github.com/Syllo/nvtop
- A fancier GPU monitoring tool with interactive UI

``` sh
nvtop
```

## Monitor GPU usage 3 (`nvitop`)

- https://github.com/XuehaiPan/nvitop
- An even fancier GPU monitoring tool with rich features

``` sh
nvitop
```

## Simpler GPU monitoring (`gpustat`)

- https://github.com/wookayin/gpustat
- Minimal and clean GPU status output, great for quick checks

``` sh
pip install gpustat
gpustat -cp
```
