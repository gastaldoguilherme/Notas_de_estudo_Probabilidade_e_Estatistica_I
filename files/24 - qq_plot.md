**Python - Estatística** 
>**Q-Q plot (Quantile-Quantile plot)**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Q-Q plot (Quantile-Quantile plot)

O Q-Q plot (Quantile-Quantile plot), que significa gráfico quantil-quantil, é uma ferramenta gráfica utilizada para avaliar se um conjunto de dados segue uma distribuição teórica esperada, frequentemente a distribuição normal. Este gráfico compara os quantis empíricos dos dados com os quantis teóricos da distribuição de referência.

Aqui está uma descrição básica do processo de criação de um Q-Q plot e como interpretá-lo:

1. **Ordenação dos dados:** Primeiro, os dados são ordenados em ordem crescente.

2. **Cálculo dos quantis empíricos:** Os quantis empíricos são calculados com base nos dados ordenados. Cada ponto de dados obtém um quantil empírico associado, indicando a proporção de dados abaixo desse ponto.

3. **Cálculo dos quantis teóricos:** Para a distribuição teórica escolhida (por exemplo, a distribuição normal), os quantis teóricos correspondentes aos quantis empíricos são calculados.

4. **Construção do Q-Q plot:** Os pares de pontos (quantis empíricos, quantis teóricos) são plotados em um gráfico. Se os dados seguirem perfeitamente a distribuição teórica, os pontos se alinharão aproximadamente ao longo de uma linha diagonal.

A interpretação do Q-Q plot envolve comparar a forma da distribuição dos dados com a distribuição teórica. Se os pontos se alinharem razoavelmente bem com a linha diagonal, isso sugere que os dados seguem a distribuição teórica. Desvios significativos da linha diagonal podem indicar desvios da normalidade.

Para o caso específico de uma distribuição normal, um Q-Q plot bem ajustado terá os pontos seguindo aproximadamente uma linha reta. Desvios nas extremidades do gráfico podem indicar caudas mais pesadas ou mais leves do que o esperado.

Você pode criar um Q-Q plot em Python usando bibliotecas como `scipy.stats` ou `statsmodels`. Aqui está um exemplo simples usando `matplotlib` e `scipy.stats`:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import probplot

# Dados de exemplo
dados = np.random.normal(size=100)

# Criação do Q-Q plot
probplot(dados, plot=plt)
plt.title("Q-Q Plot")
plt.show()
```

![Alt text](/assets/24-1.png)




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>