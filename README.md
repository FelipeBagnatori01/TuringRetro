<img src="https://media1.giphy.com/media/70JLXQ1K9ViyKUcBxd/giphy.gif" width="40%" align="right"/>

# 🎮 TuringRetro

O **TuringRetro** é o projeto de Aprendizado por Reforço do Turing USP que desenvolve agentes que aprendem sozinhos a jogar jogos retrô!

## 📑 Índice

 - [Como rodar o TuringRetro](#Como-rodar-o-TuringRetro)
   - [🕹️ Rodar um agente treinado](#🕹️-Rodar-um-agente-treinado)
   - [🏋️‍♂️ Treinar um agente](#🏋️‍♂️-Treinar-um-agente)
 - [Sobre o Projeto](#Sobre-o-projeto)
 - [Guia de Instalação](#Guia-de-Instalação)

## Como rodar o TuringRetro

### 🕹️ Rodar um agente treinado

Para rodar o TuringRetro com um agente pré-treinado, deve-se rodar o arquivo _run_rllib.py_, indicando:

 - o nome do jogo: `game`
 - o estado do jogo: `state`
 - o agente salvo: `checkpoint`
 - a quantidade de episódios: `numero_de_episodios`

```bash
python run_rllib.py game state -c checkpoint -e numero_de_episodios
```

Por exemplo, para rodar 1 episódio de um agente de *Super Mario Kart* treinado na pista *Rainbow Road*, basta rodar o seguinte comando:

```bash
python run_rllib.py SuperMarioKart-Snes rainbow_road_yoshi.state -c trained_models/SuperMarioKart-Snes/rainbow_road/model -e 1
```

### 🏋️‍♂️ Treinar um agente

Caso deseje treinar um novo agente, deve-se rodar o arquivo _run_rllib.py_, indicando:

 - o nome do jogo: `game`
 - o estado do jogo: `state`
 - a flag de treino: `-t`

```bash
python run_rllib.py game state -t 
```

Por exemplo, para treinar um agente de *Mega Man 2* contra o boss *Airman*, basta rodar o seguinte comando:

```bash
python run_rllib.py MegaMan2-Nes Normal.Airman.Fight.state -t
```

## Sobre o Projeto

O objetivo do TuringRetro é testar algoritmos de Aprendizado por Reforço Profundo em diferentes ambientes de jogos retrô, como Mega Man e Super Mario Kart. Para isso, foram treinados algoritmos tanto disponibilizados na biblioteca RLLib quanto programados pelo próprio grupo Turing USP, encontrados na pasta _agents_. 

### Ambientes

#### Mega Man 2

<p align="center">
 
  <img src="https://media3.giphy.com/media/K1E9tAtqvn78Wsze6V/giphy.gif" width="200"/>
  <img src="https://media4.giphy.com/media/fIDmLfkDkGiDy2GrP5/giphy.gif" width="200"/>
  <img src="https://media1.giphy.com/media/70JLXQ1K9ViyKUcBxd/giphy.gif" width="200"/> </br>
  <img src="https://media1.giphy.com/media/PZpjN2f6nR0qlpUfOh/giphy.gif" width="200"/>
  <img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/e3831030-47af-4f65-b849-5330fe69ce85/d4xhejk-ccbc3f91-4802-4dc8-a549-f32febbc71a0.png/v1/fill/w_900,h_887,q_75,strp/dr__wily_logo_by_callmemra-d4xhejk.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwic3ViIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl0sIm9iaiI6W1t7InBhdGgiOiIvZi9lMzgzMTAzMC00N2FmLTRmNjUtYjg0OS01MzMwZmU2OWNlODUvZDR4aGVqay1jY2JjM2Y5MS00ODAyLTRkYzgtYTU0OS1mMzJmZWJiYzcxYTAucG5nIiwid2lkdGgiOiI8PTkwMCIsImhlaWdodCI6Ijw9ODg3In1dXX0.x7B-G0R0Xd0_uOU9kiSalO0tOFnbO_-aI5DOpkPM-LQ" width="200"/>
  <img src="https://media1.giphy.com/media/577nRf3KtclHIpHkCN/giphy.gif" width="200"/> </br>
  <img src="https://media2.giphy.com/media/cJOJBT6iBgPlMTeNuV/giphy.gif" width="200"/>
  <img src="https://media4.giphy.com/media/Nv5PW31wt9jYbHmrt4/giphy.gif" width="200"/>
  <img src="https://media3.giphy.com/media/DWcx4fQNJFT9WuqAsI/giphy.gif" width="200"/>
</p>

#### Super Mario Kart

<p align="center">
  <img src="https://i.imgur.com/iabhOlt.jpg" width="60%"/> </br>
  <img src="https://media.giphy.com/media/UoLwsojXMylYBNmrBD/source.gif" width="30%"/>
  <img src="https://media.giphy.com/media/qZCpDFlATEbX6O7N9K/source.gif" width="30%"/> </br>
  <img src="https://media.giphy.com/media/bp6nKQXRZDzZVf9v7F/source.gif" width="30%"/>
  <img src="https://media.giphy.com/media/yKawloD7Osk4ZUYHok/source.gif" width="30%"/>
</p>

## Guia de Instalação

### 🐋 Docker

Este repositório é acompanhado de uma _Dockerfile_, que faz todo o trabalho de instalação necessário para rodar o projeto de maneira fácil e automática. Para rodar o projeto com o Docker, basta rodar o seguinte comando na raiz do repositório:

```bash
docker build -t turing-retro .
```

Em seguida, para rodar a imagem baixada com o conteúdo deste projeto, é necessário usar o comando:

```bash
docker run --rm -it -v $PWD:/turing-retro turing-retro
```

Caso esteja usando o Docker no Windows, basta trocar o comando ```$PWD``` por ```%cd%```.

### Bibliotecas necessárias

-  [RLlib](https://github.com/ray-project/ray) - Biblioteca que utilizamos para usar os algoritmos de RL

-  [Gym-retro](https://github.com/openai/retro) - Biblioteca que utilizamos para emular os jogos e treiná-los

-  [Tensorflow](https://github.com/tensorflow/tensorflow) - Framework para criação e utilização de redes neurais

- você também pode usar o [Pytorch](https://github.com/pytorch/pytorch), mas em nossos testes Tensorflow funciona melhor com o RLlib.

Em seu terminal com Python execute os seguintes comandos para instalar as bibliotecas necessárias:


```bash
pip install tensorflow
pip install ray[rllib]
pip install gym-retro
```

### Instalando jogos já integrados

> Alguns jogos já são integrados com o gym-retro, você pode olhar esta lista [aqui](https://github.com/openai/retro/tree/master/retro/data/stable)

Por questões legais não podemos passar os arquivos dos jogos no repositório, porém recomendamos que você os baixe do projeto [archive](https://archive.org/download/No-Intro-Collection_2016-01-03_Fixed).

Com as ROMs dos jogos baixadas, execute o seguinte comando para passar instalar os jogos no gym-retro:
  
```bash
python3 -m retro.import endereco/do/diretorio/das/ROMs/
```

Para jogos como o Mega Man 2, criamos uma série de estados e cenários de recompensas diferentes dos já instalados no gym-retro e colocamos na pasta _environments_. Desta forma, para instalar este ambiente e o Super Mario Kart, basta adicionar a ROM baixada do jogo na pasta referente com o nome _rom.ext_ em que _.ext_ é a extensão da ROM. (As extensões podem ser encontradas [nesta seção](https://retro.readthedocs.io/en/latest/integration.html#supported-rom-types) da documentação do gym-retro)

Caso queira integrar algum outro jogo não presente na lista do gym-retro, vá para próxima seção [Instalando jogos não instalados](#Instalando-jogos-não-integrados).

### Instalando jogos não integrados

🚧 Em Construção 🏗️
