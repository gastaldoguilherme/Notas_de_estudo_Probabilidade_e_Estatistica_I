**Python - Estatística** 
>**Teste de Shapiro-Wilk**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Teste de Shapiro-Wilk


O teste de Shapiro-Wilk é uma estatística de teste utilizado para verificar a normalidade de um conjunto de dados. Ele avalia se os dados seguem uma distribuição normal. A hipótese nula $(H_0$) do teste é que os dados foram retirados de uma população normalmente distribuída. A hipótese alternativa $(H_1$) é que os dados não seguem uma distribuição normal.

A estatística de teste de Shapiro-Wilk $(W$) é calculada a partir das ordenadas dos dados e é utilizada para comparar a variabilidade observada com a variabilidade que seria esperada em uma distribuição normal. Quanto mais próximo $W$ estiver de 1, mais os dados se assemelham a uma distribuição normal.

O procedimento básico do teste é o seguinte:

1. **Formulação das Hipóteses:**
   - $H_0$: Os dados seguem uma distribuição normal.
   - $H_1$: Os dados não seguem uma distribuição normal.

2. **Cálculo da Estatística de Teste $(W$):**
   - Os dados são ordenados em ordem crescente.
   - A estatística de teste $(W$) é calculada a partir dos coeficientes do vetor de pesos no teste de normalidade.

3. **Decisão Estatística:**
   - Se o valor-p associado ao $W$ for menor que o nível de significância escolhido (por exemplo, 0,05), rejeita-se a hipótese nula em favor da hipótese alternativa, indicando que os dados não seguem uma distribuição normal.

O teste de Shapiro-Wilk é sensível a amostras de tamanho moderado a grande e é frequentemente utilizado em pesquisas e análises de dados quando a suposição de normalidade é crucial.

Aqui está um exemplo de como realizar o teste de Shapiro-Wilk em Python usando a biblioteca `scipy.stats`:

```python
from scipy.stats import shapiro

# Dados de exemplo
dados = [1.2, 2.5, 3.1, 3.8, 4.2, 5.0, 5.8, 6.2, 7.0, 8.5]

# Realizar o teste de Shapiro-Wilk
stat, p_valor = shapiro(dados)

# Exibir resultados
print(f"Estatística de teste (W): {stat}")
print(f"Valor-p: {p_valor}")

# Tomar decisão estatística
nivel_significancia = 0.05
if p_valor > nivel_significancia:
    print("Não rejeitamos a hipótese nula. Os dados parecem seguir uma distribuição normal.")
else:
    print("Rejeitamos a hipótese nula. Os dados não seguem uma distribuição normal.")
```

```
Estatística de teste (W): 0.9936167597770691
Valor-p: 0.9994667768478394
Não rejeitamos a hipótese nula. Os dados parecem seguir uma distribuição normal.
```



Lembre-se de que, ao interpretar os resultados, o valor-p mais baixo que o nível de significância escolhido sugere evidências contra a hipótese nula.


### Nível de Significância

O nível de significância, muitas vezes denotado por $\alpha$, é a probabilidade de rejeitar erroneamente a hipótese nula quando ela é realmente verdadeira. Em outras palavras, é a probabilidade de cometer um erro do Tipo I. O valor padrão frequentemente escolhido para o nível de significância é $0,05$, mas outros valores como $0,01$ ou $0,10$ também podem ser usados, dependendo do contexto e dos requisitos do experimento ou análise.

A escolha do nível de significância é uma decisão do pesquisador e está relacionada ao equilíbrio entre dois tipos de erros estatísticos:

1. **Erro do Tipo I (Falso Positivo):** Rejeitar a hipótese nula quando ela é verdadeira.

2. **Erro do Tipo II (Falso Negativo):** Não rejeitar a hipótese nula quando ela é falsa.

Ao definir $\alpha = 0,05$, o pesquisador está dizendo que está disposto a aceitar um risco de $5\%$ de cometer um erro do Tipo I. Em outras palavras, se o valor-p calculado for menor que $0,05$, o pesquisador rejeitará a hipótese nula. Este é um equilíbrio comum entre sensibilidade (capacidade de detectar efeitos reais) e especificidade (capacidade de evitar conclusões falsas).

É importante notar que o valor $0,05$ não é uma regra rígida, e a escolha do nível de significância pode depender do campo de estudo, das implicações práticas dos erros e da tradição na área específica de pesquisa. Em alguns casos, os pesquisadores podem optar por níveis de significância mais conservadores ($\alpha = 0,01$) para reduzir ainda mais o risco de erro do Tipo I, enquanto em outros casos podem escolher um $\alpha$ mais alto ($\alpha = 0,10$) se forem mais tolerantes a esse tipo de erro.






&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>