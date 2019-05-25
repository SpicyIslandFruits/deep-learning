# Setup Deep Learning environment
```bash
sudo pacman -S docker docker-compose
```

## cpu only
```bash
docker pull tensorflow/tensorflow
docker run -it -p 8888:8888 tensorflow/tensorflow:nightly-py3-jupyter
```

## with gpu support
```bash
docker pull tensorflow/tensorflow:latest-gpu-jupyter
sudo pacman -S nvidia
yay -S nvidia-docker
docker run --runtime=nvidia --rm nvidia/cuda nvidia-smi
docker run --runtime=nvidia -it -p 8888:8888 tensorflow/tensorflow:nightly-py3-jupyter
```
