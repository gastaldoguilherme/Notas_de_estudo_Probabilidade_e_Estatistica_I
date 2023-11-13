**Python - Estatística** 
>**Medidas de Variabilidade - Quartis**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Quartis

Os quartis são medidas estatísticas que dividem um conjunto de dados ordenados em quatro partes iguais, cada uma representando 25% dos dados. Eles são uma parte importante das medidas de variabilidade e permitem entender a distribuição dos dados, especialmente quando se trata de valores atípicos. 

**Conceitos Gerais:**
Os quartis dividem um conjunto de dados em quatro partes, sendo que cada parte contém 25% dos dados. Eles são usados para entender a distribuição dos dados, identificar valores extremos (outliers) e avaliar a variabilidade. Os três quartis mais comuns são o primeiro quartil (Q1), o segundo quartil (Q2) e o terceiro quartil (Q3).

**Definições:**
1. **Primeiro Quartil (Q1):** É o valor que separa o primeiro 25% dos dados mais baixos do restante dos dados. Em outras palavras, 25% dos dados estão abaixo de Q1.

2. **Segundo Quartil (Q2):** É o valor que divide o conjunto de dados em duas partes iguais, com 50% dos dados abaixo de Q2. O segundo quartil é, na verdade, a mediana dos dados.

3. **Terceiro Quartil (Q3):** Q3 separa o primeiro 75% dos dados do restante dos dados, com 25% dos dados acima de Q3.

**Fórmulas:**
Para calcular os quartis, primeiro é necessário ordenar o conjunto de dados em ordem crescente. Em seguida, as fórmulas para os quartis são as seguintes:

## 1. Primeiro Quartil ou Quartil Inferior (Q1) 

&nbsp;

$\displaystyle\text{Q1} = \begin{cases}
  \LARGE x_{k}, & \text{se } k \text{ inteiro} \\
  \dfrac{\LARGE x_{k} + x_{k + 1}}{2}, & \text{se } k \text{ número fracionário}
\end{cases}
\ $

&nbsp;




   - Encontre a posição (k) do valor que divide os primeiros 25% dos dados. Use a fórmula: $ \displaystyle\ k = \frac{n + 1}{4}$, onde $n$ é o tamanho do conjunto de dados.
   - Se $k$ for um número inteiro, então $Q1$ é o valor na posição $k$.
   - Se $k$ não for um número inteiro, você pode calcular $Q1$ como a média dos valores nas posições $k$ e $ \displaystyle\ k+1$.


&nbsp;


## 2. Segundo Quartil (Q2):
   - Q2 é simplesmente a mediana dos dados, que é o valor no meio do conjunto de dados quando ele está ordenado.
&nbsp;

$\displaystyle\text{md}(X) = \begin{cases}
  \LARGE x_{\frac{n + 1}{2}}, & \text{se } n \text{ ímpar} \\
  \dfrac{\LARGE x_{\frac{n}{2}} + x_{\frac{n}{2} + 1}}{2}, & \text{se } n \text{ par}
\end{cases}
\ $

&nbsp;




## 3. Terceiro Quartil ou Quartil Superior (Q3):


&nbsp;

$\displaystyle\text{Q3} = \begin{cases}
  \LARGE x_{k}, & \text{se } k \text{ inteiro} \\
  \dfrac{\LARGE x_{k} + x_{k + 1}}{2}, & \text{se } k \text{ número fracionário}
\end{cases}
\ $

&nbsp;



   - Encontre a posição (k) do valor que divide os primeiros 75% dos dados. Use a fórmula: $ \displaystyle\ k = \frac{3(n + 1)}{4}$.
   - Se $k$ for um número inteiro, então $Q3$ é o valor na posição $k$.
   - Se $k$ não for um número inteiro, você pode calcular $Q3$ como a média dos valores nas posições $k$ e $ \displaystyle\ k+1$.

&nbsp;

**Exemplos:**
Considere o seguinte conjunto de dados ordenados (tamanho $n = 8$):

- 12, 15, 17, 22, 25, 29, 30, 35

1. **Primeiro Quartil (Q1):**
   - $ \displaystyle\ k = \frac{8 + 1}{4} = 2.25$
   - Como $k$ não é um número inteiro, vamos calcular a média entre o valor na posição 2° (15) e o valor na posição 3° (17).
   - $ \displaystyle\ Q1 = \frac{X_k=2 + X_k=3}{2} =  \frac{15 + 17}{2} = 16$

&nbsp;

2. **Segundo Quartil (Q2):**

   - $ \displaystyle\ Q2 =$ $\displaystyle\text{md}(X) = \begin{cases}\
  \dfrac{\LARGE x_{\frac{n}{2}} + x_{\frac{n}{2} + 1}}{2}, & \text{se } n \text{ par}
\end{cases}
\ $
  
  
  
   - $ \displaystyle\ k = \frac{n}{2} = 4$
   - $ \displaystyle\ k = \frac{n}{2} +1 = 5$ 
   - Como $n$ é um número par, vamos calcular a média entre o valor na posição 4 (22) e o valor na posição 5 (25).
   - $ \displaystyle\ Q2 =\frac{X_k=4 + X_k=5}{2} =  \frac{22 + 25}{2} = 23,5$
   - Q2 é o valor no meio dos dados, mediana, que é 23,5.
   


&nbsp;

3. **Terceiro Quartil (Q3):**

   - $ \displaystyle\ k = \frac{3(8 + 1)}{4} = 6.75$
   - Como $k$ não é um número inteiro, calculamos a média entre o valor na posição 6 (29) e o valor na posição 7 (30).
   - $ \displaystyle\ Q3 = \frac{X_k=6 + X_k=7}{2} = \frac{29 + 30}{2} = 29.5$

Os quartis são úteis para entender a distribuição dos dados, identificar valores atípicos e comparar diferentes partes de um conjunto de dados. Eles são comumente usados em estatísticas descritivas e análise de dados.



## Dados Simétricos x Dados Assimétricos

A avaliação da assimetria e dispersão de um conjunto de dados pode ser feita utilizando os quartis e outros métodos estatísticos. Vamos discutir cada um dos cenários que você mencionou:

1. Simétrico:

![Alt text](/assets/16-1.png)

   - Quando um conjunto de dados é simétrico, isso significa que a distribuição dos valores é equilibrada, ou seja, a metade esquerda dos valores é semelhante à metade direita em termos de forma e dispersão.
   - Os quartis, que dividem os dados em quatro partes iguais, devem estar aproximadamente na mesma posição ao longo da escala dos valores.
   - A mediana, que é o segundo quartil (Q2), deve estar próxima ao centro da distribuição.

2. Simétrico, com maior dispersão:


![Alt text](/assets/16-2.png)


   - Mesmo que um conjunto de dados seja simétrico, ele pode ter maior dispersão se os valores se espalharem por uma faixa maior na distribuição.
   - Isso significa que os quartis, apesar de estarem em posições simétricas, podem abranger uma maior gama de valores.
   - A dispersão pode ser avaliada considerando a amplitude interquartil (IQR), que é a diferença entre o terceiro quartil (Q3) e o primeiro quartil (Q1). Quanto maior o IQR, maior a dispersão.

3. Assimétrico para a esquerda:

![Alt text](/assets/16-3.png)

![Alt text](/assets/16-4.png)



   - Quando um conjunto de dados é assimétrico para a esquerda, isso significa que a cauda da distribuição se estende mais para a esquerda, indicando uma maior concentração de valores à direita.
   - Nesse caso, o primeiro quartil (Q1) estará mais próximo do centro da distribuição em relação ao terceiro quartil (Q3), que estará mais distante da mediana.
   - A mediana ainda estará próxima ao centro da distribuição.

4. Assimétrico para a direita:

![Alt text](/assets/16-5.png)

![Alt text](/assets/16-6.png)


   - Quando um conjunto de dados é assimétrico para a direita, a cauda da distribuição se estenderá mais para a direita, indicando uma maior concentração de valores à esquerda.
   - Nesse caso, o primeiro quartil (Q1) estará mais distante do centro da distribuição em relação ao terceiro quartil (Q3), que estará mais próximo da mediana.
   - A mediana ainda estará próxima ao centro da distribuição.

Em resumo, a avaliação da assimetria e dispersão de um conjunto de dados com base nos quartis envolve a análise da posição dos quartis e da mediana. Valores mais à esquerda indicam assimetria para a esquerda, enquanto valores mais à direita indicam assimetria para a direita. A dispersão pode ser avaliada considerando a amplitude interquartil (IQR).




## IQR (Interquartile Range)

O IQR (Interquartile Range), em português "Amplitude Interquartil", é uma medida estatística de dispersão que fornece informações sobre a extensão da dispersão dos dados em um conjunto. O IQR é calculado a partir dos quartis, especificamente o terceiro quartil (Q3) e o primeiro quartil (Q1).

A fórmula para calcular o IQR é a seguinte:

IQR = Q3 - Q1

O IQR representa a diferença entre o terceiro quartil (Q3) e o primeiro quartil (Q1). Os quartis dividem o conjunto de dados em quatro partes iguais, com Q1 representando o 25º percentil e Q3 representando o 75º percentil dos dados.

O IQR é uma medida útil para avaliar a dispersão dos dados porque ele desconsidera os valores extremos (outliers) que podem afetar outras medidas de dispersão, como a amplitude (diferença entre o valor máximo e o valor mínimo). Portanto, o IQR é menos sensível a valores extremos e fornece uma medida da variabilidade dos dados no intervalo central da distribuição.

Para identificar outliers usando o IQR, é comum utilizar a "regra dos 1,5 IQRs". Qualquer valor abaixo de Q1 - 1,5 * IQR ou acima de Q3 + 1,5 * IQR é considerado um valor atípico (outlier).

Em resumo, o IQR é uma medida estatística de dispersão que descreve a variabilidade dos dados em uma distribuição, sendo calculado a partir dos quartis Q1 e Q3. É útil para avaliar a dispersão dos dados e identificar valores extremos.


## Exemplo: calcular o IQR (Amplitude Interquartil) 

Vamos calcular o IQR (Amplitude Interquartil) a partir de um conjunto de dados fictício. Suponha que temos os seguintes valores:

10, 15, 16, 18, 20, 21, 23, 25, 27, 30

Aqui estão os passos para calcular o IQR:

1. Organize os dados em ordem crescente:

10, 15, 16, 18, 20, 21, 23, 25, 27, 30

2. Calcule o primeiro quartil (Q1), que é o valor no 25º percentil:


**Primeiro Quartil ou Quartil Inferior (Q1):**
   - $ \displaystyle\ k = \frac{10 + 1}{4} = 2.75$
   - Como $k$ não é um número inteiro, vamos calcular a média entre o valor na posição 2° (15) e o valor na posição 3° (/assets/16).
   - $ \displaystyle\ Q1 = \frac{X_k=2 + X_k=3}{2} =  \frac{15 + 16}{2} = 15,5$

Q1 = 15,5


3. Calcule o terceiro quartil (Q3), que é o valor no 75º percentil:


   - $ \displaystyle\ k = \frac{3(10 + 1)}{4} = 8,25$
   - Como $k$ não é um número inteiro, calculamos a média entre o valor na posição 8 (25) e o valor na posição 9 (27).
   - $ \displaystyle\ Q3 = \frac{X_k=6 + X_k=7}{2} = \frac{29 + 30}{2} = 26$

Q3 = 26

4. Agora, calcule o IQR usando a fórmula:

IQR = Q3 - Q1
IQR = 26 - 15,5
IQR = 10,5

O IQR é igual a 10,5 para este conjunto de dados. Isso significa que a dispersão dos valores no intervalo central da distribuição é de 10,5 unidades. Valores que estiverem a mais de 1,5 vezes o IQR acima de Q3 ou abaixo de Q1 podem ser considerados outliers, se você estiver usando essa medida para identificar valores atípicos.


## Identificar valores potencialmente atípicos (outliers)

Para identificar valores potencialmente atípicos (outliers), usaremos a regra dos 1,5 IQRs. Vamos calcular os valores limite acima e abaixo do IQR:

1. Valor Limite Acima (outlier superior):
   - Q3 + 1,5 * IQR

2. Valor Limite Abaixo (outlier inferior):
   - Q1 - 1,5 * IQR

No exemplo anterior, calculamos o IQR como sendo 10,5. Agora, usaremos esse valor para calcular os limites:

1. Valor Limite Acima (outlier superior):
   - Q3 + 1,5 * IQR
   - 26 + 1,5 * 10,5
   - 26 + 15,75
   - 41,75

2. Valor Limite Abaixo (outlier inferior):
   - Q1 - 1,5 * IQR
   - 15,5 - 1,5 * 10,5
   - 15,5 - 15,75
   - 0,25

Portanto, qualquer valor acima de 41,75 ou abaixo de 0,5 poderia ser considerado um outlier com base na regra dos 1,5 IQRs para o conjunto de dados fornecido. Isso significa que, se houver valores menores que 0,5 ou maiores que 40,5 no conjunto de dados, eles podem ser considerados outliers. No entanto, a interpretação e o tratamento de outliers dependem do contexto e do propósito da análise de dados.



## Q0 e Q4

Em estatística, Q0 e Q4 não são quartis convencionais como Q1 (primeiro quartil), Q2 (segundo quartil, que é a mediana) e Q3 (terceiro quartil). Em vez disso, eles representam quantis que dividem os dados em partes menores.

Q0 (também chamado de quartil zero) representa o valor mínimo do conjunto de dados. É o ponto que divide 0% dos dados, ou seja, nenhum dado está abaixo dele.

Q4 (também chamado de quartil quatro) representa o valor máximo do conjunto de dados. Ele divide 100% dos dados, ou seja, todos os dados estão abaixo ou iguais a ele.

Em resumo, a função de Q0 é representar o valor mínimo, e a função de Q4 é representar o valor máximo em um conjunto de dados. Eles são usados para delimitar os extremos da distribuição de dados. Estes não são comumente usados em estatísticas descritivas, mas são conceitos simples que podem ser úteis em algumas análises.





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>