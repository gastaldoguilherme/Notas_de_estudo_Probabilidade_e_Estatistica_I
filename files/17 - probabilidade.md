**Python - Estatística** 
>**Probabilidade - Teoria**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Probabilidade

A **probabilidade** é uma medida quantitativa da incerteza associada a eventos aleatórios. Ela desempenha um papel fundamental em estatística, ciência de dados e muitas outras áreas. Aqui estão alguns conceitos e fórmulas importantes relacionados à probabilidade.

## Conceitos Gerais

- **Espaço Amostral $(S$)**: O conjunto de todos os resultados possíveis de um experimento aleatório.
- **Evento $(A$)**: Um subconjunto do espaço amostral.
- **Probabilidade de um Evento $P(A)$**: A medida da chance de um evento ocorrer, variando de 0 (evento impossível) a 1 (evento certo).
- **Complemento de um Evento $(A'$)**: Todos os resultados que não estão em $A$.
- **União de Eventos $(A \cup B$)**: A ocorrência de pelo menos um dos eventos $A$ ou $B$.
- **Interseção de Eventos $(A \cap B$)**: A ocorrência simultânea dos eventos $A$ e $B$.

## Fórmulas

### Probabilidade de um Evento
$\displaystyle P(A) = \frac{\text{número de resultados favoráveis a } A}{\text{número total de resultados no espaço amostral}}$

### Regra da Adição
$\displaystyle P(A \cup B) = P(A) + P(B) - P(A \cap B)$


### Probabilidade Condicional
$\displaystyle P(A|B) = \frac{P(A \cap B)}{P(B)}$



### Regra da Multiplicação
$\displaystyle P(A \cap B) = P(A|B) \cdot P(B)$

---


## Eventos Complementares


**Eventos Complementares** são um conceito fundamental na teoria da probabilidade. 

Se temos um evento A, o evento complementar de A (geralmente denotado por A' ou $A^c$ ) é o evento que ocorre sempre que A não ocorre. Em outras palavras, A' representa todos os resultados possíveis que não estão em A.

A fórmula para calcular a probabilidade de um evento complementar é bastante simples:

```
P(A') = 1 - P(A)

Onde:
- P(A) é a probabilidade do evento A ocorrer
- P(A') é a probabilidade do evento complementar de A (ou seja, A não ocorrer)
```

Essa fórmula é baseada no fato de que a soma das probabilidades de um evento e seu complemento deve ser igual a 1, pois um desses eventos deve ocorrer. 


#### Exercício 1:

Suponha que você queira calcular a probabilidade de chover no final de semana. Aqui estão alguns dados que você pode usar:

- Evento A (Probabilidade de chover): P(A) = **0,30**
```
O evento complementar de A é a probabilidade de não chover, que é calculada pela fórmula:

P(A') = 1 - P(A)

Substituindo os valores na fórmula, temos:

P(A') = 1 - 0,30 = **0,70**
```
---

## Eventos Excludentes X Não Excludentes



## Eventos Excludentes
Eventos excludentes, também conhecidos como eventos **mutuamente exclusivos**, são eventos que **não podem ocorrer ao mesmo tempo**. Em outras palavras, a ocorrência de um evento impede automaticamente a ocorrência do outro. Por Exercício, jogar uma moeda e obter cara ou coroa são eventos excludentes, porque não podemos obter ambos ao mesmo tempo.

A fórmula para a probabilidade de eventos mutuamente exclusivos é simplesmente a soma das probabilidades dos eventos individuais, pois não há sobreposição entre os eventos. Se A e B são eventos mutuamente exclusivos, então a probabilidade de A ou B é dada por:

$ P(A \cup B) = P(A) + P(B) $

$A \cap B = Ø$ e $P(A \cap B) = 0$


#### Exercício 2:


Considere os seguintes conjuntos de eventos:

1. A = {cara} ; B= {coroa}, no lançamento de uma moeda.
2. A = {carta com naipe vermelho}; B={carta com naipe preto}, na retirada de uma carta de baralho.

Qual é a probabilidade da ocorrência simultânea desses eventos mutuamente exclusivos?

#### Solução:

A probabilidade da ocorrência simultânea de eventos mutuamente exclusivos é zero. 

Por Exercício, no lançamento de uma moeda, a probabilidade de obter tanto "cara" quanto "coroa" é zero, pois são eventos mutuamente exclusivos. Isso pode ser expresso como:

P(cara e coroa) =  P(cara ∩ coroa) = 0

Da mesma forma, na retirada de uma carta de baralho, a probabilidade de obter uma carta com naipe vermelho e uma carta com naipe preto ao mesmo tempo é zero, pois são eventos mutuamente exclusivos. Isso pode ser expresso como:

P(carta com naipe vermelho e carta com naipe preto) =  P(carta com naipe vermelho ∩ carta com naipe preto) = 0



#### Exercício 3:

Suponha que você jogue um dado. Considere os seguintes eventos:

- Evento A: Obter um número par
- Evento B: Obter um número ímpar

#### Solução:

Os eventos A e B são mutuamente excludentes, pois um número não pode ser par e ímpar ao mesmo tempo. Portanto, a probabilidade de obter um número par ou ímpar é igual à soma das probabilidades de obter um número par e ímpar, respectivamente. Em outras palavras:

$P(A \cup B) = P(A) + P(B)$

Como os eventos A e B são mutuamente excludentes, temos:

$P(A \cup B) = P(A) + P(B) = \frac{3}{6} + \frac{3}{6} = \frac{1}{2}$

Portanto, a probabilidade de obter um número par ou ímpar é de **50%**.




## Eventos Não Excludentes
Eventos não excludentes, por outro lado, são eventos que **podem ocorrer ao mesmo tempo**. Estes são também conhecidos como eventos **não mutuamente exclusivos**. Por Exercício, se tirarmos uma carta de um baralho, os eventos "tirar um ás" e "tirar uma carta de espadas" não são mutuamente exclusivos, porque a carta pode ser um ás de espadas.

A fórmula para a probabilidade de eventos não mutuamente exclusivos leva em conta a sobreposição entre os eventos. Se A e B são eventos que podem ocorrer simultaneamente, então a probabilidade de A ou B é dada por:

$ P(A \cup B) = P(A) + P(B) - P(A \cap B) $

$P(A \cap B) > 0$

Aqui, $ P(A \cap B) $ representa a probabilidade de ambos os eventos A e B ocorrerem.

#### Exercício 4: 


Considere um baralho padrão de 52 cartas, onde há 4 naipes (copas, ouros, paus e espadas) e 13 cartas por naipe. As cartas de copas e ouros são vermelhas, e há 4 áses no baralho (um para cada naipe).

 Qual é a probabilidade de tirar uma carta que seja de um naipe vermelho ou um ás?

#### Solução:

A probabilidade de tirar uma carta que seja de um naipe vermelho ou um ás é dada pela soma das probabilidades individuais, subtraindo a probabilidade de ocorrência conjunta (para evitar a contagem dupla). Isso pode ser expresso pela seguinte fórmula:

```
P(naipe $\cup$ ou ás) = P(naipe vermelho) + P(ás) – P(naipe vermelho $\cap$ ás)


Substituindo os valores conhecidos na fórmula, temos:


P(naipe vermelho $\cup$  ás) = (26/52) + (4/52) – (2/52) = 28/52 = 0,538

```
Portanto, a probabilidade de tirar uma carta que seja de um naipe vermelho ou um ás é aproximadamente 0,538 ou 53,8%.



#### Exercício 5: 

Considere o seguinte Exercício:

Temos duas categorias de famílias na região metropolitana de São Paulo:

1. Famílias que possuem um computador de uma determinada marca em casa.
2. Famílias que possuem um Mac em casa.

Você precisa calcular a probabilidade de uma família ter um PC ou um Mac. Aqui estão alguns dados que você pode usar:

- Probabilidade de ter PC (P(PC)): 0,86
- Probabilidade de ter Mac (P(Mac)): 0,35
- Probabilidade de ter PC e Mac (P(PC ∩ Mac)): 0,29

#### Solução:
```
A probabilidade de ter PC ou Mac é calculada pela fórmula:

P(PC ∪ Mac) = P(PC) + P(Mac) - P(PC ∩ Mac)

Substituindo os valores na fórmula, temos:

P(PC ∪ Mac) = 0,86 + 0,35 - 0,29 = 0,92 ou 92%
```

--- 


## Eventos: Independentes x Dependentes e Probabilidade Condicional

&nbsp;


**Eventos independentes** são aqueles cuja ocorrência não afeta a probabilidade de ocorrência de outros eventos. Por Exercício, se você jogar uma moeda, o resultado de uma jogada não afeta o resultado da próxima. A probabilidade de obter cara ou coroa é sempre 50%, não importa o que aconteceu antes. Matematicamente, para dois eventos independentes A e B, a probabilidade de ambos ocorrerem é o produto de suas probabilidades individuais:


$P(A \cap B) = P(A) \cdot P(B)$


#### Exercício 6: Lançamento de moeda

Você está jogando uma moeda e deseja calcular a probabilidade de obter 2 Caras em dois lançamentos consecutivos. Considere os seguintes eventos:

- Evento A: Cara no lançamento da moeda
- Evento B: Coroa no lançamento da moeda

#### Solução:

Primeiro lançamento: P(A) = 1/2; P(B) = 1/2
Segundo lançamento: P(A) = 1/2; P(B) = 1/2

A probabilidade de obter duas Caras consecutivas é calculada multiplicando as probabilidades de cada evento:

P(A) * P(A) = (1/2) * (1/2) = 1/4

**Conclusão:** Evento A (Cara) é independente do Evento B (Coroa) neste caso.


**Eventos dependentes**, por outro lado, são eventos cuja ocorrência é afetada por outros eventos. Por Exercício, se você retirar uma carta de um baralho e não a colocar de volta, a probabilidade de retirar uma segunda carta específica é afetada pela primeira retirada. Matematicamente, para dois eventos dependentes A e B, a probabilidade de ambos ocorrerem é a probabilidade do primeiro evento multiplicada pela probabilidade do segundo evento, dado que o primeiro evento ocorreu:

$P(A \cap B) = P(B) \cdot P(A|B)$

Onde `P(A|B)` é a probabilidade condicional de A dado que B ocorreu.


#### Exercício 7: Urna com esferas

Em uma urna, há 3 esferas vermelhas e 5 esferas azuis. Qual é a probabilidade de selecionar 2 esferas vermelhas sem reposição? Considere os seguintes eventos:

- Evento A: Selecionar uma esfera vermelha na primeira retirada
- Evento B: Selecionar uma esfera vermelha na segunda retirada

#### Solução:

Primeira retirada: P(B) = 3/8
Segunda retirada: P(A|B) = 2/7 (já que uma esfera vermelha foi retirada anteriormente)

P(B): Isso representa a probabilidade do evento B ocorrer.

P(A|B): Isso representa a probabilidade condicional do evento A ocorrer dado que o evento B já ocorreu. Em outras palavras, é a probabilidade de A acontecer considerando que B já aconteceu.


A probabilidade de selecionar 2 esferas vermelhas é calculada multiplicando as probabilidades de cada evento:

$P(A \cap B) = P(B) \cdot P(A|B)$

$P(A \cap B) = (3/8) * (2/7)$

**Conclusão:** A ocorrência de esfera vermelha na primeira retirada afeta a probabilidade de sair uma esfera vermelha na segunda retirada devido à falta de reposição.




**Probabilidade condicional** é a probabilidade de um evento ocorrer, dado que outro evento já ocorreu. Se os eventos são independentes, então a probabilidade condicional é simplesmente a probabilidade do evento ocorrer. Se os eventos são dependentes, a probabilidade condicional é calculada de forma diferente. 

#### Probabilidade condicional: Evento Independente

$P(A|B) = P(A)$

Onde:
- `P(A|B)` é a probabilidade do evento A ocorrer dado que o evento B já ocorreu.
- `P(A)` e `P(B)` são independentes.


#### Probabilidade condicional: Evento Dependente

$P(A|B) = \frac{P(A \cap B)}{P(B)}$


Onde:
- `P(A|B)` é a probabilidade do evento A ocorrer dado que o evento B já ocorreu.
- `P(A e B)` é a probabilidade de ambos os eventos A e B ocorrerem.
- `P(B)` é a probabilidade do evento B ocorrer.


#### Exercício 8: Vagas de emprego

Suponha que existam 90 candidatos a vagas de emprego, com as seguintes características:

|               | Com Curso Superior | Sem Curso Superior |
|---------------|--------------------|--------------------|
| Menor de 3 anos  | 18                 | 9                  | 27                 |
| Maior que 3 anos | 36                 | 27                | 63                 |
| Total         | 54                 | 36                 |                    |


#### Solução:

a) Probabilidade de um candidato ter curso superior, dado que tenha mais de 3 anos de experiência (P(CS | + 3 anos)).
```
P(CS | + 3 anos) = P(CS ∩ + 3 anos) / P(+ 3 anos)

P(CS ∩ + 3 anos) = 36/90
P(+ 3 anos) = 63/90

Calcule: P(CS | + 3 anos) = (36/90) / (63/90)

```

b) Probabilidade de um candidato ter menos de 3 anos de experiência, dado que não tenha curso superior (P(- 3 anos | NCS)).


```
P(- 3 anos | NCS) = P(- 3 anos ∩ NCS) / P(NCS)

P(- 3 anos ∩ NCS) = 9/90
P(NCS) = 36/90

Calcule: P(- 3 anos | NCS) = (9/90) / (36/90)

```


#### Exercício 9: Carro e motorista

Considere carros e motoristas em um determinado dia, com as seguintes informações:

- Probabilidade de escolher um carro amarelo (ca) = 3/100
- Probabilidade de escolher um motorista loiro (ml) = 1/5
- Probabilidade de escolher um carro amarelo e um motorista loiro (ca ∩ ml) = 1/50

Calcule a probabilidade de escolher um motorista loiro, dado que o carro é amarelo (P(ml | ca)).

#### Solução:

```
P(ml | ca) = P(ml ∩ ca) / P(ca)

Calcule: P(ml | ca) = (1/50) / (3/100)

```



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>