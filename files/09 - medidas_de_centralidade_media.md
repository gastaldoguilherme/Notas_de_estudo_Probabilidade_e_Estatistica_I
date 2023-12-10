**Python - Estatística** 
>**Medidas de Centralidade - Média**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Medidas de Centralidade - Média

### Média de uma População
A média de uma população, muitas vezes denotada por μ (mu), é a média de todos os valores de uma característica em uma população completa. Para calcular a média de uma população, você soma todos os valores e divide pelo tamanho da população.

**Fórmula**:

$\huge \mu = \frac{\displaystyle\sum_{i=1}^{N} x_i}{N}$

**Onde**:
- μ é a média da população.
- N é o tamanho da população.
- $x_i$ são os valores individuais da população.

**Exemplo de Média de uma População**:
Suponha que você queira calcular a média de idade de todos os habitantes de uma cidade. Você coleta informações de todas as pessoas na cidade e, em seguida, calcula a média somando as idades de todas as pessoas e dividindo pelo número total de habitantes.

### Média de uma Amostra
A média de uma amostra, frequentemente representada por $\displaystyle\ \bar{x}$ (x-bar), é a média de um subconjunto representativo de uma população. Para calcular a média de uma amostra, você soma os valores da amostra e divide pelo tamanho da amostra.

**Fórmula**:

$\huge \bar{x} = \frac{\huge\sum_\limits{i=1}^{n} x_i}{n}$

**Onde**:
- $\displaystyle\ \bar{x}$ é a média da amostra.
- n é o tamanho da amostra.
- $x_i$ são os valores individuais da amostra.

**Exemplo de Média de uma Amostra**:
Suponha que você queira calcular a média de idade de uma amostra de 100 pessoas em uma cidade com uma população total de 10.000. Você coleta informações de 100 pessoas e calcula a média das idades dessa amostra.

Lembre-se de que a média da amostra é uma estimativa da média da população e pode variar de uma amostra para outra.

Em ambos os casos, a média é uma medida central que descreve a tendência central dos dados, mas é importante diferenciar entre a média da população e a média da amostra, pois elas podem ser diferentes e têm implicações estatísticas distintas.

### Tipos de Médias, Fórmulas, Exemplos e Usos

1. **Média Aritmética**:
   - **Fórmula**: $\displaystyle\ \text{Média} = \frac{\displaystyle\sum_{i=1}^n x_i}{n}$
   - **Exemplo**: Média de [10, 20, 30] = $\displaystyle\ \frac{10 + 20 + 30}{3} = 20$
   - **Uso**: A média aritmética é amplamente usada para calcular valores centrais e é a média mais comum usada em análises estatísticas. Exemplos de uso incluem o cálculo da média de pontuações de testes, média de idades de uma população.

2. **Média Ponderada**:
   - **Fórmula**: $\displaystyle\ \text{Média Ponderada} = \frac{\displaystyle\sum_{i=1}^n w_i \cdot x_i}{\displaystyle\sum_{i=1}^n w_i}$
   - **Exemplo**: Média ponderada de [10, 20, 30] com pesos [0.3, 0.2, 0.5] = $\displaystyle\ \frac{(10 \cdot 0.3) + (20 \cdot 0.2) + (30 \cdot 0.5)}{0.3 + 0.2 + 0.5} = 23$
   - **Uso**: A média ponderada é usada quando diferentes valores têm diferentes importâncias ou pesos. Exemplos de uso incluem a média de notas e o cálculo de índices ponderados em finanças.

3. **Média Geométrica**:
   - **Fórmula**: $\text{Média Geométrica} = \huge\sqrt[n]{x_1 \cdot x_2 \cdot \ldots \cdot x_n}$
   - **Exemplo**: Média geométrica de [2, 4, 8] = $\huge \sqrt[3]{2 \cdot 4 \cdot 8} = 4$
   - **Uso**: A média geométrica é usada para calcular médias de taxas de crescimento, taxas de retorno ou valores que se multiplicam. Exemplo de uso inclui o cálculo do retorno médio de investimentos ao longo do tempo.

4. **Média Harmônica**:
   - **Fórmula**: $\displaystyle\ \text{Média Harmônica} = \frac{n}{\displaystyle\sum_{i=1}^n \frac{1}{x_i}}$
   - **Exemplo**: Média harmônica de [2, 4, 8] = $\displaystyle\ \frac{3}{\displaystyle\frac{1}{2} + \frac{1}{4} + \frac{1}{8}} = \frac{3}{\displaystyle\frac{7}{8}} = \frac{24}{7}$
   - **Uso**: A média harmônica é usada para médias de taxas ou valores inversos, como velocidade média. Exemplo de uso inclui o cálculo da velocidade média em viagens de ida e volta.

5. **Média Quadrática (RMS - Root Mean Square)**:
   - **Fórmula**: $\displaystyle\ \text{Média Quadrática} = \sqrt{\frac{1}{n} \sum_{i=1}^n x_i^2}$
   - **Exemplo**: Média quadrática de [3, 4, 5] = $\displaystyle\ \sqrt{\frac{1}{3} \cdot (3^2 + 4^2 + 5^2)} \approx 4.18$
   - **Uso**: A média quadrática é usada para calcular a média dos quadrados dos valores e é útil para medições de amplitude, como em análises de sinais. Exemplo de uso inclui o cálculo da potência eficaz em circuitos elétricos e análise de dados de amplitude de ondas sonoras.

6. **Média Truncada**:
   - **Fórmula**: Exclua uma certa porcent

agem de valores extremos e calcule a média dos valores restantes.
   - **Exemplo**: Se temos o conjunto [5, 10, 15, 20, 1000] e excluímos 10% dos valores mais baixos e 10% dos valores mais altos, a média truncada seria a média dos valores 15 e 20, que é 17.5.
   - **Uso**: A média truncada é usada para mitigar o impacto de valores extremos em conjuntos de dados, fornecendo uma medida de tendência central mais robusta.

Cada tipo de média é aplicável em cenários específicos com base nas características dos dados e nos objetivos da análise. Os exemplos acima ilustram como cada tipo de média é usado em situações práticas.


## Exemplo Prático

1. **Média Aritmética**:
   - **Exemplo Prático**: Suponha que você tenha um conjunto de notas de um aluno em diferentes disciplinas: [85, 90, 78, 92, 88]. Para calcular a média das notas, você soma todas as notas e divide pelo número de disciplinas. A média aritmética seria $\displaystyle\ \frac{85 + 90 + 78 + 92 + 88}{5} = 86.6$. Essa média representa a pontuação média do aluno.

2. **Média Ponderada**:
   - **Exemplo Prático**: Imagine que você está calculando a média de um produto com base em suas avaliações, onde as avaliações variam de 1 a 5, e a importância de cada avaliação é diferente. Se as avaliações e seus pesos forem [4, 5, 3] e [0.2, 0.3, 0.5], respectivamente, a média ponderada seria calculada como $\displaystyle\ \frac{(4 \cdot 0.2) + (5 \cdot 0.3) + (3 \cdot 0.5)}{0.2 + 0.3 + 0.5} = 3.7$. Isso reflete a avaliação média do produto, considerando a importância das avaliações.

3. **Média Geométrica**:
   - **Exemplo Prático**: Se você investir em ações e deseja calcular o retorno médio anual ao longo de 3 anos, e os retornos anuais são 10%, 5%, e 8%, a média geométrica seria $\huge\sqrt[3]{1.10 \cdot 1.05 \cdot 1.08} \approx 7.65\%$. Isso representa o crescimento médio anual de seus investimentos.

4. **Média Harmônica**:
   - **Exemplo Prático**: Suponha que você faz uma viagem de ida e volta de 100 km em uma velocidade de 60 km/h na ida e 40 km/h na volta. Para calcular a velocidade média da viagem completa, você usaria a média harmônica, que é $\displaystyle\ \frac{2}{\frac{1}{60} + \frac{1}{40}} \approx 48 km/h$. Isso representa a velocidade média da viagem.

5. **Média Quadrática (RMS - Root Mean Square)**:
   - **Exemplo Prático**: Em um experimento de física, você registra os valores de amplitude de uma onda sonora: [2 V, 3 V, 4 V]. Para calcular a amplitude média, você usaria a média quadrática, que é $\displaystyle\ \sqrt{\frac{1}{3} \cdot (2^2 + 3^2 + 4^2)} \approx 3 V$. Isso representa a amplitude média da onda.

6. **Média Truncada**:
   - **Exemplo Prático**: Suponha que você esteja calculando a média de salários em uma empresa, e os salários variam de $25.000 a $200.000. Se você decidir excluir os 10% dos salários mais baixos e 10% dos salários mais altos para evitar distorções, a média truncada seria a média dos salários restantes. Isso fornece uma medida mais robusta do salário médio na empresa.

Cada tipo de média é aplicável em cenários específicos com base nas características dos dados e nos objetivos da análise. Os exemplos acima ilustram como cada tipo de média é usado em situações práticas.



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
