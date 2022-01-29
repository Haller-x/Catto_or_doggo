# Step-by-step

Tenha o Docker e Nvidia Docker instalados: [Link](https://www.tensorflow.org/install/docker?hl=pt-br)

Na pasta do projeto rode:

`docker build -t tensorenv .`

`docker run --gpus all -p 8888:8888 tensorenv`

Vá até a url do notebook e rode o notebook (build_model.ipynb)!


Ferramenta com deploy disponível em (muito demorado para carregar devido as limitações do heroku): [Link](http://catordogclassifier.herokuapp.com/)
Note que após clicar em predição a renderização da imagem e o resultado podem demorar alguns segundos, devido a limitação de RAM imposta pelo heroku.

Link do git do deploy: [Link](https://github.com/Haller-x/GRAD-CAM_ST) (Optei por não utilizar Docker pelo tempo demasiado para subir a imagem)


