**Python - Estatística** 
>**Teste distribuição normal - Python**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Teste Distribuição Normal

Neste bloco de código, estamos realizando um teste de normalidade em duas amostras de dados, uma seguindo uma distribuição normal e outra não.


### Teste de Shapiro-Wilk

O teste de Shapiro-Wilk é um teste de normalidade que avalia se uma amostra de dados segue uma distribuição normal. O teste de Shapiro-Wilk é usado para verificar a hipótese nula de que uma amostra é proveniente de uma população normalmente distribuída. Se o valor-p do teste for menor que um nível de significância escolhido (geralmente 0,05), a hipótese nula é rejeitada, indicando que os dados não seguem uma distribuição normal.

No seu exemplo, você executou o teste de Shapiro-Wilk com a seguinte linha de código:

```python
stats.shapiro(dados)
```

O resultado é uma tupla, onde o primeiro valor (statistic) é a estatística do teste de Shapiro-Wilk e o segundo valor (pvalue) é o valor-p associado ao teste. 

Para interpretar o resultado do teste de Shapiro-Wilk:

- Se o valor-p (pvalue) for maior que o seu nível de significância escolhido (por exemplo, 0,05), você não rejeita a hipótese nula. Nesse caso, você pode concluir que os dados seguem uma distribuição normal.

- Se o valor-p for menor que o seu nível de significância escolhido, você rejeita a hipótese nula. Nesse caso, você não pode considerar que os dados seguem uma distribuição normal.

Portanto, o valor-p é crucial para determinar se os dados são ou não normalmente distribuídos. Se o valor-p for maior que 0,05 (ou o nível de significância escolhido), você não rejeitaria a hipótese nula e poderia considerar os dados como normalmente distribuídos. Se o valor-p for menor que 0,05, você rejeitaria a hipótese nula e consideraria que os dados não são normalmente distribuídos.




### Importação das bibliotecas

```python
from scipy import stats
from scipy.stats import norm, skewnorm
import matplotlib.pyplot as plt
```

### Amostra de dados com distribuição normal

```python
# Criação de uma variável com dados em uma distribuição normal com a função rvs (100 elementos)
dados = norm.rvs(size=1000)
dados
```

### Histograma dos dados

```python
# Histograma
plt.hist(dados, bins=20)
plt.title('Dados')
```

![Dados](/assets/6-1.png)



### Geração de gráfico Q-Q para verificar se a distribuição é normal

```python
# Geração de gráfico para verificar se a distribuição é normal
fig, ax = plt.subplots()
stats.probplot(dados, fit=True, plot=ax)
plt.show()
```

![Gráfico Q-Q](/assets/6-2.png)

### Teste de Shapiro-Wilk para dados normais

```python
# Execução do teste de Shapiro
# Segundo argumento é o valor de p, não há como rejeitar a hipótese nula
stats.shapiro(dados)
```

Resultado do teste de Shapiro-Wilk para dados normais:

```python
- Estatística de teste (statistic): 0.9989317059516907
- Valor p (p-value): 0.8359315395355225
- Conclusão: p-value > 0,05
```

Neste caso, o valor p (p-value) é igual a 0.8359315395355225, o que é maior do que um nível de significância comum, como 0,05. Portanto, não há evidência estatística para rejeitar a hipótese nula de que os dados seguem uma distribuição normal. Isso sugere que os dados são consistentes com uma distribuição normal.


## Teste Distribuição não Normal

### Amostra de dados não normais

```python
dados2 = skewnorm.rvs(4, size=1000)
dados2
```

### Histograma dos dados não normais

```python
# Histograma
plt.hist(dados2, bins=20)
plt.title('Dados')
```

![Dados Não Normais](/assets/6-3.png)

### Geração de gráfico Q-Q para verificar se a distribuição é normal (dados não normais)

```python
fig, ax = plt.subplots()
stats.probplot(dados2, fit=True, plot=ax)
plt.show()
```

![Gráfico Q-Q para Dados Não Normais](/assets/6-4.png)

### Teste de Shapiro-Wilk para dados não normais

```python
stats.shapiro(dados2)
```

Resultado do teste de Shapiro-Wilk para dados não normais:

```python
- Estatística de teste (statistic): 0.9618684649467468
- Valor p (p-value): 1.700202648211458e-15
- Conclusão: p-value < 0,05
```

Neste caso, o valor p (p-value) é muito próximo de zero (1.700202648211458e-15), o que é muito menor do que um nível de significância comum, como 0,05. Portanto, há evidência estatística para rejeitar a hipótese nula de que os dados seguem uma distribuição normal. Isso sugere que os dados não são consistentes com uma distribuição normal.




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>