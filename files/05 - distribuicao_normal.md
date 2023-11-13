**Python - Estatística** 
>**Distribuição Normal - Python**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



### Distribuição Normal

Neste bloco de código, estamos explorando conceitos relacionados à distribuição normal (ou gaussiana).

## Importação da função norm

```python
from scipy.stats import norm
```

### Funções `cdf` e `sf`

As funções `cdf` (função de distribuição cumulativa) e `sf` (função de sobrevivência) são duas funções usadas na análise de probabilidade e estatística, particularmente em relação a distribuições de probabilidade contínuas, como a distribuição normal.

Diferença entre elas:

1. Função de Distribuição Cumulativa (CDF - Cumulative Distribution Function):

   - A função de distribuição cumulativa (CDF) de uma variável aleatória fornece a probabilidade acumulada de que a variável aleatória seja menor ou igual a um valor específico.
   - Matematicamente, a CDF é definida como P(X ≤ x), onde X é a variável aleatória e "x" é um valor específico.
   - A CDF fornece a probabilidade acumulada de que um valor seja menor ou igual a "x". Ela acumula as probabilidades de todos os valores menores ou iguais a "x".
   - A função `norm.cdf(x, média, desvio padrão)` em Python, por exemplo, calcula a probabilidade acumulada para uma distribuição normal. Você fornece o valor "x", a média e o desvio padrão.

2. Função de Sobrevivência (SF - Survival Function):

   - A função de sobrevivência (SF), também chamada de função complementar acumulativa, fornece a probabilidade de que a variável aleatória seja maior que um valor específico.
   - Matematicamente, a SF é definida como P(X > x) = 1 - P(X ≤ x).
   - A SF fornece a probabilidade acumulada de que um valor seja maior que "x".
   - A função `norm.sf(x, média, desvio padrão)` em Python, para uma distribuição normal, calcula a probabilidade de sobrevivência, isto é, a probabilidade de que um valor seja maior que "x".

Em resumo, a CDF fornece a probabilidade acumulada de que uma variável aleatória seja menor ou igual a um valor específico, enquanto a SF fornece a probabilidade acumulada de que a variável aleatória seja maior que um valor específico. Ambas as funções são essenciais na análise estatística e na determinação de probabilidades relacionadas a distribuições de probabilidade contínuas.

## Exemplo: Conjunto de objetos em uma cesta, a média é 8 e o desvio padrão é 2

### 1. Qual a probabilidade de tirar um objeto que pesa menos que 6 quilos?


![Alt text](/assets/5-1.png)



`cdf(6)`

```python
norm.cdf(6, 8, 2)
0.1587
```

### 2. Qual a probabilidade de tirar um objeto que pesa mais que 6 quilos?



#### Duas possibilidades de solução:

1° Solução: `sf(6)`

```python
norm.sf(6, 8, 2)
0.8413447460685429
```

2° Solução: `1 - cdf(6)`

![Alt text](/assets/5-1.png)
 
```python
1 - norm.cdf(6, 8, 2)
0.8413447460685429
```

### 3. Qual a probabilidade de tirar um objeto que pesa menos que 6 ou mais que 10 quilos?

![Alt text](/assets/5-2.png)

`cdf(6) + sf(10)`

```python
norm.cdf(6, 8, 2) + norm.sf(10, 8, 2)
0.31731050786291415
```

###  4. Qual a probabilidade de tirar um objeto que pesa menos que 10 e mais que 8 quilos?



#### Duas possibilidades de solução:

1° Solução: `cdf(10) - sf(8)`

```python
norm.cdf(10, 8, 2) - norm.sf(8, 8, 2)
0.3413447460685429
```

2° Solução: `cdf(10) - cdf(8)`

![Alt text](/assets/5-3.png)
 
```python
norm.cdf(10, 8, 2) - norm.cdf(8, 8, 2)
0.3413447460685429
```





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>