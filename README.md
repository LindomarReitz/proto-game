# Proto Jogo

Um jogo de mímica entre duas equipes: cada uma tem uma chance de fazer a mímica em um tempo, quem acerta ganha pontos.

# Pré Requisitos

* python 2.7+
* python 3 **NÃO SUPORTADO**
* virtualenv
* docker

# Para fazer o build:

``` 
virtualenv py27
. py27/bin/activate
pip install -r requirements.txt
``` 

# Para executar

```
docker run --name some-redis -d redis
python game.py
Abra a url http://localhost:5000 no seu navegador, você NÃO terá instruções ainda :)
```

# Serviços disponíveis:

Para acessar use http://localhost:5000/<serviço>

1. start/"nome_da_sala_de_jogo": inicia um novo jogo
2. games: mostra lista de jogos em execução
3. games/"nome_da_sala_de_jogo" mostra se o jogo existe e está em execução
4. games/"nome_da_sala_de_jogo"/sort_word: sorteia uma palavra para o jogo
5. games/"nome_da_sala_de_jogo"/jogador/guess/"palavra: permite arriscar uma palavra
