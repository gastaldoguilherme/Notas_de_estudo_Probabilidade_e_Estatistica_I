**Python - Estatística** 
>**Teorema Central do Limite**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Teorema Central do Limite 

O Teorema Central do Limite (TCL) é um resultado fundamental em estatística e probabilidade. Ele descreve o comportamento da distribuição de médias amostrais de uma população, independentemente da forma da distribuição original da população. O TCL é essencial para a inferência estatística e é frequentemente usado em análises de dados.

A declaração geral do Teorema Central do Limite é a seguinte:

Se $X_1, X_2, ..., X_n$ são variáveis aleatórias independentes e identicamente distribuídas (i.i.d.) com uma média $\mu$ e um desvio padrão $\sigma$, então, para $n$ suficientemente grande, a distribuição amostral da média $\bar{X}$ se aproxima de uma distribuição normal com média $\mu$ e desvio padrão $\frac{\sigma}{\sqrt{n}}$.

Matematicamente, isso pode ser expresso da seguinte forma:

$ \bar{X} \sim \mathcal{N} \left( \mu, \frac{\sigma}{\sqrt{n}} \right) $

onde:
- $\bar{X}$ é a média amostral,
- $\mu$ é a média populacional,
- $\sigma$ é o desvio padrão populacional,
- $n$ é o tamanho da amostra,
- $\mathcal{N}(\mu, \sigma)$ representa uma distribuição normal com média $\mu$ e desvio padrão $\sigma$.

Em termos práticos, o TCL implica que, à medida que o tamanho da amostra aumenta, a distribuição amostral da média se torna aproximadamente normal, independentemente da forma da distribuição original da população. Isso é fundamental para a inferência estatística, pois permite o uso de métodos baseados na distribuição normal, como intervalos de confiança e testes de hipóteses, mesmo para populações que podem não ser normalmente distribuídas.

A implementação prática do TCL muitas vezes envolve o uso de bibliotecas estatísticas em linguagens como Python, que fornece funções para gerar dados de amostra e realizar análises estatísticas. Aqui está um exemplo de como o TCL pode ser ilustrado em Python:

```python
import numpy as np
import matplotlib.pyplot as plt

# Parâmetros da população
media_populacional = 50
desvio_padrao_populacional = 10

# Tamanho da amostra
tamanho_amostra = 30

# Gerar várias amostras e calcular médias
medias_amostrais = [np.mean(np.random.normal(media_populacional, desvio_padrao_populacional, tamanho_amostra)) for _ in range(1000)]

# Plotar histograma das médias amostrais
plt.hist(medias_amostrais, bins=30, density=True, alpha=0.5, color='blue', label='Médias Amostrais')

# Plotar a distribuição normal teórica
dist_normal = np.random.normal(media_populacional, desvio_padrao_populacional/np.sqrt(tamanho_amostra), 1000)
plt.plot(sorted(dist_normal), 1/(desvio_padrao_populacional/np.sqrt(tamanho_amostra) * np.sqrt(2 * np.pi)) *
         np.exp(-(sorted(dist_normal) - media_populacional)**2 / (2 * (desvio_padrao_populacional/np.sqrt(tamanho_amostra))**2)),
         linewidth=2, color='red', label='Distribuição Normal Teórica')

# Adicionar legendas e título
plt.title('Teorema Central do Limite')
plt.xlabel('Média Amostral')
plt.ylabel('Densidade de Probabilidade')
plt.legend()

# Exibir o gráfico
plt.show()
```

![Alt text](/assets/26-1.png)



Neste exemplo, estamos gerando 1000 amostras de tamanho 30 de uma distribuição normal com uma média populacional de 50 e um desvio padrão populacional de 10. As médias amostrais são calculadas, e um histograma delas é plotado juntamente com a distribuição normal teórica prevista pelo Teorema Central do Limite. O gráfico deve ilustrar como as médias amostrais se aproximam de uma distribuição normal, mesmo que a distribuição original não seja normal.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>