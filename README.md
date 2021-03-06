# Step-by-step
Como o modelo foi construído utilizando GPU é necessário que a máquina que for rodar o projeto contenha GPU (nvidia) e o driver instalado.
Tenha o Docker e Nvidia Docker instalados: [Link](https://www.tensorflow.org/install/docker?hl=pt-br)


Na pasta do projeto rode:

`docker build -t tensorenv .`

`docker run --gpus all -p 8888:8888 tensorenv`

Pode-se adicionar a flag `--rm` ao comando docker run para manter o host limpo de contêineres parados e não utilizados.

Vá até a url do notebook e rode o notebook (build_model.ipynb)!

Ferramenta com deploy disponível em (muito demorado para carregar devido as limitações do heroku): [Link](https://catordogclassifierdocker.herokuapp.com/)

Note que após clicar em predição a renderização da imagem e o resultado podem demorar alguns segundos, devido a limitação de RAM imposta pelo heroku.

Link do git do deploy: [Link](https://github.com/Haller-x/Docker_ST) 

OBS: O notebook conta com um wget para baixar as imagens - infelizmente o host da url conta com alguma instabilidade então pode haver uma enorme variação no tempo de download (também está comentado no notebook)

OBS²: Infelizmente a imagem do Tensorflow e download do modelo base (EfficientNetB3) podem contar com um erro 104 (connection reset by peer), nesse caso basta tentar novamente em alguns segundos para construir o container, e rodar novamente a célula no notebook.

OBS³: Caso rode em um ambiente sem GPU utilize tensorflow/tensorflow:nightly-jupyter em vez de tensorflow/tensorflow:nightly-gpu-jupyter no Dockerfile e utilize no lugar do segundo comando docker: `docker run -p 8888:8888 tensorenv` Caso queira que as mudanças sejam feitas em tempo real no notebook utilize
`docker run --gpus all -v "$(pwd)":/code -p 8888:8888 tensorenv` 
