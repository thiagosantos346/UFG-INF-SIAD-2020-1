# O Mundo de Wumpus - Modelo em Lógica de Primeira Ordem

## Comandos

- ```Wumpus(x)``` : O variável x guarda a posição onde se encontra o wumpus.
- ```Poço(p)```   :  Ao consultar este predicado passando como parâmetro uma sala ele retorna.
verdadeiro se lá existe um poço, caso contrário retorna falso.
- ```∃x Ação(x,5).``` : Indica se existe uma ação dado uma posição.
- ```∀ t Brilho ⇒ Ação(Pegar, t)```: Sempre que haver ouro, pegue-o.

## Sentenças

1. A sentença indica um estado do ambiente que é o fato do agente perceber
brisa na sala atual, ou seja, a sala que se encontra no instante t.

   -  ```∀ t, f, b, o, m, c Percepção([f, b, o, m, c],t) ⇒ Brisa(t).```

1. Essa sentença representa o estado do ambiente no qual o agente percebe o brilho do
ouro na sala em que ele está no instante t.

   - ```∀ t, f, b, o, m, c Percepção([f, b, o, m, c],t) ⇒ Brilho(t).```

1. É possível ainda, utilizar sentenças de implicação quantificadas, simulando um
comportamento reativo simples. Por exemplo:
   - ```∀ t Brilho ⇒ Ação(Pegar, t).```

   - A sentença é semelhante a uma regra de condição-ação do agente reativo
simples, sua condição é a percepção do brilho do ouro e sua reação é a ação de pegar o
ouro.

1. A relação de adjacência entre as salas pode ser representada como:
   - ```∀ x, y, a, b Adjacente([x, y], [a, b]) ⇔ [a, b] ∈ {[x+1, y], [x-1, y], [x, y+1], [x, y-1]}.```

1. Se o agente estiver em uma sala e perceber brisa, então essa sala é arejada:
   - ```∀s, Em(Agente, s, t) ∧ Brisa(t) ⇒ Arejado(s)```
   - A variável t serve para indicar o instante.

### Regras de Diagnóstico

1. Se uma sala é arejada, alguma sala adjacente contém um poço:
   - ```∀s Arejado(s) ⇒ ∃r Adjacente(r, s) ∧ Poço(r)```
2. Se uma sala não é arejada, nenhuma sala adjacente contém um
poço:
   - ```∀s ¬Arejado(s) ⇒ ¬∃r Adjacente(r, s) ∧ Poço(r)```

1. Se combinar as duas anteriores, forma-se a sentença bicondicional:
   - ```∀s Arejado(s) ⇔ ∃r Adjacente(r, s) ∧ Poço(r)```

### Regras Causais

1. Um poço é a causa de salas adjacentes serem arejadas:

   - ```∀r Poço(r) ⇒ [∀r Adjacente(r, s) ⇒ Arejado(s)]```

1. Se todas as salas adjacentes a uma dada sala não contiverem poços, a sala não
será arejada:
   - ```∀s [∀r Adjacente(r, s) ⇒ ¬Poço(r) ]⇒ ¬Arejado(s)]```

---
