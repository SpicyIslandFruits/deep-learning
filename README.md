# Setup Deep Learning environment
```bash
sudo pacman -S docker docker-compose
```

## cpu only
```bash
docker run --name tensorflow -it -p 8888:8888 tensorflow/tensorflow:nightly-py3-jupyter
```

## with gpu support
```bash
sudo pacman -S nvidia
yay -S nvidia-docker
docker run --runtime=nvidia --rm nvidia/cuda nvidia-smi # test gpu
docker run --name tensorflow --runtime=nvidia -it -p 8888:8888 tensorflow/tensorflow:nightly-py3-jupyter
```
