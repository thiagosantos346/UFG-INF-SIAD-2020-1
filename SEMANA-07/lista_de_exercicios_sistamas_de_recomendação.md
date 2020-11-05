```
Instituto de Informática - UFG
Disciplina: Sistemas Inteligentes de Apoio à Decisão / Tópicos 2
Professor: Vinícius Sebba Patto. Goiânia, outubro de 2020
```

Dado um serviço de streaming por assinatura, para assistir filmes e séries, considere que há disponível dados sobre:

- Usuários:
  - Idade
    - Menor que 10,
    - 10-11,
    - 12-13,
    - 14-15,
    - 16-17,
    - Maior que 18.
- Filmes/séries:
  - Título.
  - Gênero
    - Comédia
    - Drama
    - Romance
    - etc.
  - Categoria
    - Série
    - Curta
    - Longa
    - Documentários
    - Etc.
  - Ator principal
  - Ano de lançamento
  - Diretor
  
Responda às seguintes perguntas:

1) Quais técnicas você poderia usar para fazer um sistema de recomendação para esse serviço?

```
  Resposta:

  Caso 1 - Baseado em conteúdo, Aprendizado de Maquina: Podemos sugerir títulos similares com base em características dos títulos com base na features.

  Caso 2 - Baseado em colaborativo - Um caso de Recuperação de informação: Podemos também fazer sugestões de títulos com base no comportamento do grupo, a exemplo quem viu esse filme também viu esse.

```

2) Em quais casos você poderia usar uma técnica ou outra? Faça um paralelo entre estas
técnicas.

```
  Resposta:

  O Caso 2: Só seria possível se existisse dados os suficiente para montar um modelo com boa taxa de acerto.
  
  O caso 3: Seria preciso construir o modelo com o passar do tempo e a colata de dados dos usuários.

```

3) Seriam necessários outros dados para usar em uma técnica ou outra? Quais? Alguns dos dados acima seriam desnecessários?

```
  Resposta:
  
  Para o caso 2, só é possível se guardarmos estatísticas do comportamento do usuário na plataforma, pois é necessários criar cluster, relacionado os comportamento, exemplo 98% das pessoa que assistiram esse filme também viram esses, ou seja um caso de algoritmo colaborativo.
  
```

4) Quais algoritmos você poderia adotar para fazer a recomendação de acordo com as técnicas que você citou?

```
  Resposta:
    
  Caso 1 : Podemos usar um algorítmo de regressão linear simples, para achar correlações entre as features.

  Caso 2 : Podemos usar um algorítmo baseado em casos, onde os filme já assistido levaria sugestão do proxímo baseado no proximo.

```

5) Trata-se de um problema de aprendizado supervisionado ou não supervisionado? Justifique.

```
  Resposta:
  
  Para o caso 1 é seria uma técnica de algorítmo supervisionado, já que as features serviram como labels para a sugestões, como género, faixa etária, dentre outros dependendo do contexto de aplicação.

  Para o caso 2 é um algoritmos não supervisionado já que queremos é justamente encontrar as labels com base no comportamento dos usuários.

  Por fim é possível mesclar as duas abordagens. 

```

6) De qual forma poderíamos avaliar a recomendação de um filme ou série?

```
  Resposta:

  O feedback do usuário poderia ser coletado em ambos os casos, e é possível também usando dados coletados do comportamento do usuário inferir se e recomendação for valida, como tempo de retenção e etc.
  
```
