# Step-by-step

Tenha o Docker e Nvidia Docker instalados: [Link](https://www.tensorflow.org/install/docker?hl=pt-br)

Na pasta do projeto rode:
`docker build -t tensorenv .`
`docker run --gpus all -p 8888:8888 tensorenv`

Vá até a url do notebook e rode o notebook (build_model.ipynb)!

Ferramenta com deploy disponível em: 


