# Setup Deep Learning environment
```bash
sudo pacman -S docker docker-compose
yay -S nvidia-docker
docker pull tensorflow/tensorflow:latest-gpu-jupyter
```

## with gpu support
```bash
docker run --runtime=nvidia --rm nvidia/cuda nvidia-smi
docker run --runtime=nvidia -it -p 8888:8888 tensorflow/tensorflow:nightly-py3-jupyter
```
