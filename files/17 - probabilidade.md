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



### Teorema de Bayes

$ P(A|B) = \displaystyle \frac{P(B|A) \cdot P(A)}{P(B)} $



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

### Teorema de Bayes

O Teorema de Bayes é uma ferramenta fundamental em teoria da probabilidade que nos permite atualizar probabilidades de hipóteses com base em novas evidências. A fórmula do Teorema de Bayes é expressa como:

$ P(A|B) = \displaystyle \frac{P(B|A) \cdot P(A)}{P(B)} $

onde:

- $ P(A|B) $ é a probabilidade condicional de A dado B.
- $ P(B|A) $ é a probabilidade condicional de B dado A.
- $ P(A) $ é a probabilidade marginal de A.
- $ P(B) $ é a probabilidade marginal de B.

A probabilidade marginal de um evento é a probabilidade desse evento ocorrer, independentemente de quaisquer outros eventos. No contexto do Teorema de Bayes, a probabilidade marginal de um evento (por exemplo, $ P(A) $) é a probabilidade desse evento ocorrer sem considerar qualquer informação adicional sobre outros eventos.

Essa fórmula é útil quando queremos inverter a condição de probabilidade condicional, ou seja, queremos calcular a probabilidade de uma hipótese dada uma evidência.








### Probabilidade Total:

A Probabilidade Total é um conceito usado para calcular a probabilidade de um evento $ B $, levando em consideração diferentes "causas" ou "condições" possíveis, geralmente expressas como eventos $ A_i $. 

Isso significa que a probabilidade total de $ B $ é a soma das probabilidades condicionais de $ B $ dado cada $ A_i $, ponderada pela probabilidade de cada $ A_i $ individualmente.






$ P(B) = \sum_{i} P(B | A_i) \cdot P(A_i) $

Onde:
- $ P(B) $ é a probabilidade do evento $ B $ ocorrer.
- $ P(B | A_i) $ é a probabilidade condicional de $ B $ dado $ A_i $, ou seja, a probabilidade de $ B $ ocorrer dado que $ A_i $ ocorreu.
- $ P(A_i) $ é a probabilidade do evento $ A_i $ ocorrer, representando as diferentes "causas" ou "condições" possíveis.

#### Exercício 10: 

Suponha que estamos interessados na probabilidade de um estudante passar em um exame ($ B $). Existem duas possíveis causas para o sucesso ou fracasso: o estudante estudou ($ A_1 $) ou o estudante não estudou ($ A_2 $). As probabilidades são as seguintes:

$ P(B | A_1) = 0.9 $ (a probabilidade de passar dado que o estudante estudou)

$ P(B | A_2) = 0.2 $ (a probabilidade de passar dado que o estudante não estudou)

$ P(A_1) = 0.6 $ (a probabilidade de o estudante estudar)

$ P(A_2) = 0.4 $ (a probabilidade de o estudante não estudar)

Agora podemos usar a fórmula da Probabilidade Total para calcular a probabilidade total de passar no exame:

$ P(B) = P(B | A_1) \cdot P(A_1) + P(B | A_2) \cdot P(A_2) $

Substituindo os valores:

$ P(B) = (0.9 \cdot 0.6) + (0.2 \cdot 0.4) $

$ P(B) = 0.54 + 0.08 $

$ P(B) = 0.62 $

Portanto, a probabilidade total de um estudante passar no exame é 0.62, considerando as diferentes condições de estudar ou não estudar.



### Probabilidade Marginal:

A Probabilidade Marginal refere-se à probabilidade de um evento específico, sem levar em consideração outros eventos. Se tivermos dois eventos $ A $ e $ B $, a probabilidade marginal de $ A $ (ou $ B $) é a probabilidade de $ A $ (ou $ B $) ocorrer, independentemente de $ B $ (ou $ A $) ocorrer ou não. A fórmula para a probabilidade marginal é expressa como:

$P(A) = \sum_{i} P(A, B_i) $

Isso implica somar as probabilidades conjuntas de $ A $ e $ B_i $ para todas as possíveis condições $ B_i $.



Onde:
- $ P(A) $ é a probabilidade do evento $ A $ ocorrer independentemente de $ B $.
- $ P(A, B_i) $ é a probabilidade conjunta de $ A $ e $ B_i $, representando a ocorrência simultânea de $ A $ e uma condição específica $ B_i $.

#### Exercício 11: 

Suponha que temos dois eventos, $ A $ e $ B $, onde $ A $ representa a ocorrência de chuva e $ B $ representa a condição de estar nublado ou ensolarado. As probabilidades são as seguintes:

$ P(A, \text{nublado}) = 0.3 $ (a probabilidade de chuva quando está nublado)
$ P(A, \text{ensolarado}) = 0.1 $ (a probabilidade de chuva quando está ensolarado)

Agora, podemos usar a fórmula da Probabilidade Marginal para calcular a probabilidade de chuva, independente de estar nublado ou ensolarado:

$ P(A) = P(A, \text{nublado}) + P(A, \text{ensolarado}) $

Substituindo os valores:

$ P(A) = 0.3 + 0.1 $

$ P(A) = 0.4 $

Portanto, a probabilidade marginal de chuva é 0.4, independente da condição de estar nublado ou ensolarado. Essa probabilidade representa a chance global de chuva, sem considerar as diferentes condições climáticas.




#### Exercício 12: Testes médicos e uma condição médica específica

Vamos considerar um exemplo clássico envolvendo testes médicos e uma condição médica específica. Suponha que uma certa condição médica é relativamente rara, afetando apenas 1% da população. Um teste médico foi desenvolvido para diagnosticar essa condição, e o teste tem uma precisão de 95% para detectar corretamente a condição quando ela está presente, mas também tem uma taxa de 2% de falsos positivos (indicando erroneamente a condição em pessoas saudáveis).

Agora, imagine que uma pessoa faz o teste e o resultado é positivo. A pergunta é: qual a probabilidade de a pessoa realmente ter a condição?

Vamos usar o Teorema de Bayes para calcular essa probabilidade.

Definindo os eventos:
- $ A $: A pessoa tem a condição médica (evento raro, com probabilidade $ P(A) = 0.01 $).
- $ B $: O teste é positivo.

Além disso, temos as probabilidades condicionais:
- $ P(B|A) $: Probabilidade de o teste ser positivo dado que a pessoa tem a condição (95% de precisão, $ P(B|A) = 0.95 $).
- $ P(B|\neg A) $: Probabilidade de o teste ser positivo dado que a pessoa não tem a condição (2% de falsos positivos, $ P(B|\neg A) = 0.02 $).

Agora, podemos usar o Teorema de Bayes para calcular a probabilidade de a pessoa ter a condição dado que o teste foi positivo:

$P(A|B) = \displaystyle\frac{P(B|A) \cdot P(A)}{P(B)} $

onde $ P(B) $ é a probabilidade marginal de o teste ser positivo, que pode ser calculada usando a lei da probabilidade total:

$P(B) = P(B|A) \cdot P(A) + P(B|\neg A) \cdot P(\neg A) $

Vamos agora calcular essas probabilidades usando o Teorema de Bayes. Em Python, podemos fazer isso da seguinte forma:

```python
# Probabilidades iniciais
P_A = 0.01  # Probabilidade de ter a condição
P_B_given_A = 0.95  # Probabilidade de teste positivo dado que tem a condição
P_B_given_not_A = 0.02  # Probabilidade de teste positivo dado que não tem a condição
P_not_A = 1 - P_A  # Probabilidade de não ter a condição

# Aplicação do Teorema de Bayes
P_B = P_B_given_A * P_A + P_B_given_not_A * P_not_A
P_A_given_B = (P_B_given_A * P_A) / P_B

print(f"A probabilidade de ter a condição dado que o teste foi positivo é: {P_A_given_B:.4f}")
```

```
A probabilidade de ter a condição dado que o teste foi positivo é: 0.3242

```

Isso significa que, mesmo com um teste positivo, a probabilidade de a pessoa realmente ter a condição é de aproximadamente 32,42%.
Esse resultado destaca como a probabilidade a priori (a probabilidade inicial de ter a condição antes de fazer o teste) e as taxas de falsos positivos do teste impactam significativamente na interpretação dos resultados.












&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>