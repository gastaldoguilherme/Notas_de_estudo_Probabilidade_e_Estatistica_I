**Python - Estatística** 
>**Probabilidade e Estatística Não Paramétrica**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Probabilidade Não Paramétrica:

A teoria da probabilidade não paramétrica refere-se a métodos estatísticos que não fazem suposições específicas sobre a forma ou a natureza da distribuição subjacente dos dados. Em vez de depender de parâmetros específicos, esses métodos utilizam abordagens mais flexíveis. Alguns conceitos e técnicas comuns incluem:

1. **Testes de Hipóteses Não Paramétricos:**
   - **Teste de Wilcoxon (Mann-Whitney):** Usado para comparar duas amostras independentes.
   - **Teste de Kruskal-Wallis:** Uma extensão do teste de Wilcoxon para mais de duas amostras independentes.
   - **Teste de Friedman:** Uma versão não paramétrica da Análise de Variância (ANOVA) para amostras pareadas.

2. **Correlação Não Paramétrica:**
   - **Coeficiente de Correlação de Spearman:** Avalia a relação monotônica entre duas variáveis, mesmo que a relação não seja linear.

### Estatística Não Paramétrica:

A estatística não paramétrica é uma abordagem estatística que não faz suposições sobre a forma ou parâmetros específicos da população subjacente. Ela é particularmente útil quando os dados não seguem uma distribuição normal ou quando há preocupações sobre a precisão dos parâmetros estimados. Em Python, bibliotecas como `scipy.stats` oferecem uma variedade de funções para realizar análises não paramétricas.

#### Exemplo Prático:

Vamos considerar o teste de Wilcoxon para duas amostras independentes. O código em Python usando `scipy.stats` seria algo como:

```python
from scipy.stats import mannwhitneyu

# Amostras independentes
amostra1 = [23, 28, 32, 37, 42]
amostra2 = [18, 25, 30, 35, 40]

# Teste de Wilcoxon
stat, p_valor = mannwhitneyu(amostra1, amostra2)

# Exibir resultados
print(f"Estatística de Teste: {stat}")
print(f"Valor-p: {p_valor}")

# Tomar decisão estatística
nivel_significancia = 0.05
if p_valor > nivel_significancia:
    print("Não rejeitamos a hipótese nula.")
else:
    print("Rejeitamos a hipótese nula.")
```
```
Estatística de Teste: 15.0
Valor-p: 0.6904761904761905
Não rejeitamos a hipótese nula.

```

 Por exemplo, a fórmula para o teste de Wilcoxon seria expressa como:

$H_0: \text{As amostras são iguais}$

$H_1: \text{As amostras são diferentes}$


---

#### Exemplo Prático:

### Para o coeficiente de correlação de Spearman:

$\huge\rho = 1 - \frac{6 \sum d_i^2}{n(n^2 - 1)}$



A fórmula apresenta o cálculo do Coeficiente de Correlação de Spearman ($\rho$), que é uma medida de correlação não paramétrica entre duas variáveis. Em vez de avaliar a relação linear entre as variáveis, o coeficiente de Spearman avalia a relação monotônica, o que significa que ele identifica se, à medida que uma variável aumenta, a outra também tende a aumentar (ou diminuir).

A fórmula é composta pelos seguintes elementos:

- $\rho$: Coeficiente de Correlação de Spearman.
- $d_i$: A diferença entre os postos (ordens) das observações nas duas variáveis.
- $n$: Número total de pares de observações.

A expressão $\huge\sum d_i^2$ representa a soma dos quadrados das diferenças de postos. A fórmula é normalizada usando a seguinte fórmula:

$\huge\rho = 1 - \huge\frac{6 \sum d_i^2}{n(n^2 - 1)}$

A interpretação do coeficiente de Spearman é semelhante à do coeficiente de correlação de Pearson, variando de -1 a 1. Um valor de 1 indica uma correlação perfeita monotônica positiva, -1 indica uma correlação perfeita monotônica negativa, e 0 indica ausência de correlação monotônica.

Essa fórmula é útil quando os dados não seguem uma distribuição normal ou quando a relação entre as variáveis não é estritamente linear. O coeficiente de Spearman é menos sensível a valores extremos do que o coeficiente de correlação de Pearson, tornando-o adequado para dados ordinalmente classificados.


1. **Correlação Perfeita Monotônica Positiva ( $\rho = 1$):**
   - Isso significa que, à medida que uma variável aumenta, a outra também aumenta, seguindo uma relação monotônica positiva. Por exemplo, se você tiver duas variáveis, como o tempo de estudo e as notas dos alunos, uma correlação perfeita monotônica positiva indicaria que, à medida que o tempo de estudo aumenta, as notas dos alunos sempre aumentam, sem exceção.

2. **Correlação Perfeita Monotônica Negativa ($\rho = -1$):**
   - Isso significa que, à medida que uma variável aumenta, a outra diminui, seguindo uma relação monotônica negativa. Continuando com o exemplo anterior, uma correlação perfeita monotônica negativa indicaria que, à medida que o tempo gasto assistindo TV aumenta, as notas dos alunos sempre diminuem, sem exceção.

3. **Ausência de Correlação Monotônica ($\rho = 0$):**
   - Isso significa que não há uma tendência clara de aumento ou diminuição quando você compara as duas variáveis. Em outras palavras, as variáveis não estão consistentemente relacionadas de maneira monotônica. No exemplo, um coeficiente de Spearman de 0 indicaria que o tempo de estudo não está consistentemente relacionado com as notas dos alunos.

Em resumo, o coeficiente de Spearman indica o quão bem as ordens das observações em duas variáveis estão relacionadas de maneira monotônica. Um valor de 1 ou -1 sugere uma relação perfeita, enquanto 0 sugere ausência de relação monotônica. Valores entre -1 e 1 indicam uma relação monotônica, mas podem não ser perfeitos.













&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
