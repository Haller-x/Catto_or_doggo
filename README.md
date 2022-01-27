`docker build --tags tensorenv .`

`docker run --gpus all -v $pwd:/tf -p 8888:8888 --user $(id -u):$(id -g) tensorenv`


