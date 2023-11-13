**Python - Estatística** 
>**Coeficientes de Assimetria e Achatamento de uma curva**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Coeficientes de Assimetria e Achatamento de uma curva

## Coeficiente Quartílico de Assimetria em relação aos quartis

O coeficiente quartílico de assimetria é uma medida estatística que avalia a assimetria de uma distribuição de dados em relação aos quartis. Ele é calculado pela fórmula:

$ Q_s = \frac{Q_3 + Q_1 - 2Q_2}{Q_3 - Q_1} $

onde $ Q_1 $, $ Q_2 $ e $ Q_3 $ são os valores dos quartis inferior, mediano e superior, respectivamente.


#### Exemplo de Coeficiente Quartílico de Assimetria

Suponha que tenhamos os seguintes dados representando uma amostra de uma distribuição estatística:

$12, 15, 18, 20, 22, 25, 28, 30, 35, 40 $

Agora, vamos calcular o Coeficiente Quartílico de Assimetria $( Q_s $) para essa amostra. Primeiro, ordenamos os dados:

$12, 15, 18, 20, 22, 25, 28, 30, 35, 40 $

Os quartis são então calculados da seguinte forma:

- $ Q_1 $ (primeiro quartil) é a mediana dos dados abaixo do ponto médio: $ Q_1 = \frac{15 + 18}{2} = 16.5 $
- $ Q_2 $ (segundo quartil) é a mediana da amostra: $ Q_2 = 22 $
- $ Q_3 $ (terceiro quartil) é a mediana dos dados acima do ponto médio: $ Q_3 = \frac{30 + 35}{2} = 32.5 $

Agora, podemos usar a fórmula do Coeficiente Quartílico de Assimetria:

$Q_s = \frac{Q_3 + Q_1 - 2Q_2}{Q_3 - Q_1} $

Substituindo os valores:

$Q_s = \frac{32.5 + 16.5 - 2 \times 22}{32.5 - 16.5} $

Calculando:

$Q_s = \frac{33}{16} \approx 2.06 $



A interpretação do Coeficiente Quartílico de Assimetria ($ Q_s $) envolve analisar o sinal e a magnitude do resultado. Vamos interpretar o valor que calculamos no exemplo:

$ Q_s \approx 2.06 $

1. **Sinal:** O valor é positivo, indicando assimetria positiva.
   - Se $ Q_s $ é positivo, significa que a cauda direita da distribuição é mais longa ou tem uma inclinação mais suave em comparação com a cauda esquerda. Isso sugere que existem valores acima da média que estão mais afastados do centro da distribuição.

2. **Magnitude:** O valor de 2.06 é relativamente grande.
   - Quanto maior o valor em termos absolutos, maior é a assimetria.

Portanto, a conclusão para este exemplo seria que a distribuição dos dados apresenta uma assimetria positiva significativa, indicando uma cauda direita mais longa. Isso pode ser útil para compreender a forma da distribuição e identificar a presença de outliers ou valores extremos.

Lembre-se de que a interpretação pode variar dependendo do contexto da análise estatística e da natureza dos dados. Em resumo, o Coeficiente Quartílico de Assimetria fornece informações sobre a forma e simetria da distribuição dos dados, auxiliando na compreensão de sua estrutura.

---



## Coeficiente Decílico de Assimetria em relação aos decis

O coeficiente decílico de assimetria é outra medida que busca quantificar a assimetria em uma distribuição, considerando os decis (frações de 10%) em vez dos quartis. Sua fórmula é dada por:

$ D_s = \frac{D_9 + D_1 - 2D_5}{D_9 - D_1} $

onde $ D_1 $, $ D_5 $ e $ D_9 $ representam os valores dos decis de 10%, 50%, e 90%, respectivamente.




#### Exemplo de Coeficiente Decílico de Assimetria

Suponha que tenhamos os seguintes dados representando uma amostra de uma distribuição estatística:

$10, 12, 14, 18, 20, 22, 25, 28, 30, 35 $

Agora, vamos calcular o Coeficiente Decílico de Assimetria ($D_s$) para essa amostra. Primeiro, ordenamos os dados:

$10, 12, 14, 18, 20, 22, 25, 28, 30, 35 $

Os decis são então calculados da seguinte forma:


- $D_1$ = **D<sub>10%</sub>** (primeiro decil) é o valor correspondente a 10% dos dados ordenados: **D<sub>10%</sub> =12**
- $D_5$ = **D<sub>50%</sub>** (quinto decil) é a mediana da amostra: **D<sub>50%</sub> = 22**
- $D_9$ = **D<sub>90%</sub>** (nono decil) é o valor correspondente a 90% dos dados ordenados: **D<sub>90%</sub> = 35**

Agora, podemos usar a fórmula do Coeficiente Decílico de Assimetria:

$D_s = \displaystyle \frac{D_9 + D_1 - 2D_5}{D_9 - D_1} $

Substituindo os valores:

$D_s = \displaystyle\frac{35 + 12 - 2 \times 22}{35 - 12} $

Calculando:

$D_s = \frac{13}{23} \approx 0.57 $

### Conclusão

O Coeficiente Decílico de Assimetria para esta amostra é aproximadamente 0.57. O sinal positivo indica uma assimetria positiva, sugerindo que a cauda direita da distribuição é mais longa. A magnitude moderada do coeficiente sugere uma assimetria mais equilibrada em comparação com valores mais extremos. Essa análise fornece insights sobre a forma da distribuição dos dados e pode ser útil para compreender a presença de valores atípicos.

---


## Coeficiente de Assimetria de Pearson (Coeficiente de Skewness)

Os coeficientes de Pearson são formas de medir a assimetria da amostra em função das medidas de tendência central – média, moda e mediana.

#### O primeiro coeficiente de assimetria de Pearson é dado pela seguinte expressão:

$ A = \frac{\mu - \text{Mo}}{S} $

Nessa expressão:
- $ \mu $ é a média aritmética da amostra;
- Mo é a moda da amostra;
- S é o desvio padrão da amostra.
- O sinal da amostra é dado pelo numerador, portanto:
  - Se a média for superior à moda, a assimetria será positiva (ou à direita);
  - Se a média for inferior à moda, a assimetria será negativa (ou à esquerda).

#### O segundo coeficiente de assimetria de Pearson é dado pela seguinte expressão:

$ A = \frac{3 \times (\mu - \text{Mediana})}{S} $

Nessa expressão:
- $ \mu $ é a média aritmética da amostra;
- Md é a mediana da amostra;
- S é o desvio padrão da amostra.
- O sinal da amostra é dado pelo numerador, portanto:
  - Se a média for superior à mediana, a assimetria será positiva (ou à direita);
  - Se a média for inferior à mediana, a assimetria será negativa (ou à esquerda).





 ### Coeficiente de Assimetria de Pearson X Coeficiente de Skewness


 "Coeficiente de Assimetria de Pearson" e "Coeficiente de Skewness" são frequentemente usados de forma intercambiável e podem referir-se à mesma medida estatística. A forma mais comum de medir a assimetria é o Coeficiente de Skewness.

Portanto, para esclarecer:

- **Coeficiente de Skewness (ou Coeficiente de Assimetria de Pearson):**

O coeficiente de assimetria, também conhecido como coeficiente de skewness, é uma medida estatística que descreve a assimetria da distribuição de um conjunto de dados. Indica se a distribuição dos dados é simétrica, inclinada para a esquerda (negativa) ou inclinada para a direita (positiva).

O coeficiente de skewness é calculado usando a fórmula:

#### Coeficiente de Skewness (com desvio padrão)

Esta fórmula usa $ \bar{x} $ para representar a média dos dados e $ s $ para representar o desvio padrão.

$ \text{Skewness} = \displaystyle \frac{\sum{(x_i - \bar{x})^3}}{n \cdot s^3} $


   - Mede a assimetria de uma distribuição.
   - Valores positivos indicam assimetria à direita, enquanto valores negativos indicam assimetria à esquerda.
   - A fórmula típica é: $ \text{Skewness} = \displaystyle \frac{\sum{(x_i - \bar{x})^3}}{n \cdot s^3} $, onde $ \bar{x} $ é a média, $ n $ é o número de observações e $ s $ é o desvio padrão.


#### Coeficiente de Skewness (com somatórios e médias amostrais)

A segunda fórmula  é uma forma padronizada da fórmula, onde os cálculos são expressos em termos de somatórios e médias amostrais:

$ \text{Skewness} = \displaystyle\frac{\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^3}{\left(\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^2\right)^{3/2}} $

Se expandirmos e simplificarmos a segunda fórmula, veremos que ela é essencialmente a mesma que a primeira:

$ \text{Skewness} = \frac{\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^3}{\left(\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^2\right)^{3/2}} $

$ = \frac{\sum{(X_i - \bar{X})^3}}{n \cdot \left(\sum{(X_i - \bar{X})^2}\right)^{3/2}} $

$ = \frac{\sum{(x_i - \bar{x})^3}}{n \cdot s^3} $




$ \text{Skewness} = \frac{\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^3}{\left(\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^2\right)^{3/2}} $

onde:
- $ n $ é o número de observações.
- $ X_i $ é cada valor individual nos dados.
- $ \bar{X} $ é a média dos dados.

O resultado do cálculo do coeficiente de skewness fornece informações sobre a forma da distribuição dos dados:

- Se o coeficiente é próximo de 0, a distribuição é aproximadamente simétrica.
- Se o coeficiente é negativo, a cauda da distribuição está inclinada para a esquerda (assimetria negativa).
- Se o coeficiente é positivo, a cauda da distribuição está inclinada para a direita (assimetria positiva).

Em Python, você pode calcular o coeficiente de skewness usando bibliotecas como NumPy ou SciPy. Aqui está um exemplo usando o NumPy:

```python
import numpy as np

# Dados de exemplo
dados = [2, 4, 7, 1, 5, 8, 6, 3, 9, 10]

# Calcular o coeficiente de skewness
skewness = np.mean((dados - np.mean(dados))**3) / np.std(dados)**3

print(f'Coeficiente de Skewness: {skewness}')
```
```
Coeficiente de Skewness: 0.0
```


Alternativamente, você pode usar a função `skew()` da biblioteca SciPy:

```python
from scipy.stats import skew

# Calcular o coeficiente de skewness usando scipy.stats
skewness_scipy = skew(dados)

print(f'Coeficiente de Skewness (SciPy): {skewness_scipy}')
```

Ambos os métodos devem fornecer resultados semelhantes para o coeficiente de skewness.


```
Coeficiente de Skewness (SciPy): 0.0

```


```
stats.describe(dados)
```

```
DescribeResult(nobs=10, minmax=(1, 10), mean=5.5, variance=9.166666666666668, skewness=0.0, kurtosis=-1.2242424242424244)

```


### Exercício sobre Coeficiente de Assimetria de Pearson:

**Dados:**
Considere o seguinte conjunto de dados representando as idades de uma amostra de pessoas: 

$ \{25, 30, 35, 40, 45, 50, 55, 60, 65, 70\} $

**Fórmula:**
O Coeficiente de Assimetria de Pearson é calculado pela seguinte fórmula:

$ \text{Assimetria} = \frac{3(\bar{x} - \mu)}{s} $

onde $\bar{x}$ é a média, $\mu$ é a mediana, e $s$ é o desvio padrão.

**Solução:**

1. **Calcular a média ($\bar{x}$):**
   $ \bar{x} = \frac{25 + 30 + 35 + 40 + 45 + 50 + 55 + 60 + 65 + 70}{10} = 47.5 $

2. **Calcular a mediana ($\mu$):**
   - Como temos 10 observações, a mediana é a média das observações centrais, que são 45 e 50.
   $ \mu = \frac{45 + 50}{2} = 47.5 $

3. **Calcular o desvio padrão ($s$):**
   $ s = \sqrt{\frac{\sum{(x_i - \bar{x})^2}}{n}} $
   $ s = \sqrt{\frac{(25-47.5)^2 + (30-47.5)^2 + \ldots + (70-47.5)^2}{10}} $
   $ s \approx 12.5 $

4. **Calcular o Coeficiente de Assimetria de Pearson:**
   $ \text{Assimetria} = \frac{3(47.5 - 47.5)}{12.5} = 0 $

```

import numpy as np

# Dados
idades = np.array([25, 30, 35, 40, 45, 50, 55, 60, 65, 70])

# Calcular média, mediana e desvio padrão
media = np.mean(idades)
mediana = np.median(idades)
desvio_padrao = np.std(idades)

# Calcular Coeficiente de Assimetria de Pearson
assimetria_pearson = 3 * (media - mediana) / desvio_padrao

# Exibir resultados
print(f"Média: {media}")
print(f"Mediana: {mediana}")
print(f"Desvio Padrão: {desvio_padrao}")
print(f"Coeficiente de Assimetria de Pearson: {assimetria_pearson}")

```
```
Média: 47.5
Mediana: 47.5
Desvio Padrão: 14.361406616345072
Coeficiente de Assimetria de Pearson: 0.0
```



**Conclusão:**
O coeficiente de assimetria de Pearson é zero para esse conjunto de dados. Isso indica simetria, já que a média é igual à mediana. Não há inclinação para a direita ou para a esquerda na distribuição das idades. O resultado zero é consistente com uma distribuição perfeitamente simétrica.




### Exercício sobre Coeficiente de Skewness:


**Dados:**
Considere o seguinte conjunto de dados representando as notas de um grupo de estudantes:


$ \{78, 85, 92, 88, 96, 70, 82, 75, 90, 88\} $


**Fórmula:**
O Coeficiente de Skewness é calculado pela seguinte fórmula:

$ \text{Skewness} = \displaystyle\frac{\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^3}{\left(\frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^2\right)^{3/2}} $


#### Biblioteca Numpy

```
import numpy as np

# Dados de exemplo
dados = [78, 85, 92, 88, 96, 70, 82, 75, 90, 88]

# Calcular o coeficiente de skewness
skewness = np.mean((dados - np.mean(dados))**3) / np.std(dados)**3

print(f'Coeficiente de Skewness: {skewness}')

```

```
Coeficiente de Skewness: -0.39993365865733277

```


#### Biblioteca SciPy - stats -skew

```
from scipy.stats import skew

# Calcular o coeficiente de skewness usando scipy.stats
skewness_scipy = skew(dados)

print(f'Coeficiente de Skewness (SciPy): {skewness_scipy}')

```

```
Coeficiente de Skewness (SciPy): -0.3999336586573328

```

#### Biblioteca SciPy - stats - describe

```
from scipy.stats import describe
stats.describe(dados)

```

```
DescribeResult(nobs=10, minmax=(70, 96), mean=84.4, variance=65.82222222222222, skewness=-0.3999336586573328, kurtosis=-0.8549281217273386)

```



#### Observação:
 A função `np.var()` no NumPy, por padrão, usa o fator de correção de Bessel (divide por `N - 1`, onde `N` é o número de observações) para calcular a variância amostral.

Por outro lado, a função `describe()` do módulo `scipy.stats` usa um fator de correção diferente, que é `N` (divisão por `N`, sem subtrair 1). Isso pode resultar em valores ligeiramente diferentes para a variância, especialmente para conjuntos de dados pequenos.

Para obter resultados consistentes entre `np.var()` e `describe()` , pode ajustar a função `np.var()` para usar o mesmo fator de correção que `describe()`. Você pode fazer isso definindo o parâmetro `ddof` (degrees of freedom) como 1 em `np.var()`. 


---


## Coeficiente de Curtose (kurtosis) em relação aos quartis e decis

A curtose refere-se ao grau de achatamento de uma curva de distribuição de uma variável aleatória. A curtose é comparada à da curva normal, conhecida como a curva de sino.

Em relação à curva normal, uma curva pode ser:
- **Mesocúrtica:** Apresenta a mesma curtose da curva normal.
- **Platicúrtica:** Mais achatada que a distribuição normal, com curtose superior.
- **Leptocúrtica:** Mais alongada que a distribuição normal, com curtose inferior.

A curtose da curva normal é 0,263. Uma curva será:
- **Mesocúrtica:** Curtose igual a 0,263.
- **Platicúrtica:** Curtose maior que 0,263.
- **Leptocúrtica:** Curtose menor que 0,263.


As medidas de assimetria podem ser expressas em termos das medidas de tendência central, mas a curtose não pode. A fórmula comum para a curtose é o coeficiente percentílico de curtose:

$ C = \displaystyle\frac{(Q3 - Q1)}{2 \times (D9 - D1)} $

Onde:
- $ Q3 $ é o terceiro quartil.
- $ Q1 $ é o primeiro quartil.
- $ D9 $ é o nono decil.
- $ D1 $ é o primeiro decil.

Essa fórmula produz um valor entre 0 e 1. A curva normal tem índice 0,263. A curtose também pode ser expressa em função da amplitude semiquartílica:

$ Aq = \displaystyle \frac{(Q3 - Q1)}{2} $

E, finalmente, a curtose pode ser escrita como a razão entre a amplitude semiquartílica e a diferença entre o nono e o primeiro decil:

$ C = \displaystyle\frac{Aq}{(D9 - D1)} $



#### Exercício: Coeficiente de Curtose (kurtosis) em relação aos quartis e decis


```
import numpy as np

# Dados de exemplo
dados = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 6, 7, 8]

# Calcular quartis, decis e curtose
q1 = np.percentile(dados, 25)
q3 = np.percentile(dados, 75)
d1 = np.percentile(dados, 10)
d9 = np.percentile(dados, 90)

# Calcular curtose
curtose = (q3 - q1) / (2 * (d9 - d1))

# Imprimir os resultados
print(f'Q1: {q1}')
print(f'Q3: {q3}')
print(f'D1: {d1}')
print(f'D9: {d9}')
print(f'Curtose: {curtose}')

```

```
Q1: 3.0
Q3: 5.0
D1: 2.0
D9: 6.6
Curtose: 0.2173913043478261

```
#### Leptocúrtica: Curtose menor que 0,263.

Curtose: 0.2173913043478261

Em relação à curva normal, seu grau de achatamento é menor que o da curva normal padrão (curva mais pontiaguda), indica que os dados estão mais concentrados (desvio padrão menor).   


--- 


### Curtose (kurtosis) em relação com a curva de uma distribuição normal

O Coeficiente de Curtose é uma medida estatística que descreve a forma da distribuição de um conjunto de dados em relação à sua "normalidade" ou à quantidade de "peso da cauda" nas extremidades da distribuição. Em outras palavras, a curtose indica o quão achatada ou pronunciada é a curva de uma distribuição em comparação com a curva de uma distribuição normal.

A fórmula do Coeficiente de Curtose é dada por:

$ \text{Curtose} = \displaystyle\frac{\frac{1}{n}\sum_{i=1}^{n} (x_i - \bar{x})^4}{\left(\frac{1}{n}\sum_{i=1}^{n} (x_i - \bar{x})^2\right)^2} - 3 $

Onde:
- $\bar{x} $ é a média do conjunto de dados.
- $n $ é o número de observações no conjunto de dados.

A fórmula é composta por duas partes principais:
1. **Numerador (Parte Superior):** $\frac{1}{n}\sum_{i=1}^{n} (x_i - \bar{x})^4$ - Para cada valor no conjunto de dados, subtrai a média e eleva o resultado à quarta potência. Depois, soma todos esses valores.
  
2. **Denominador (Parte Inferior):** $\left(\frac{1}{n}\sum_{i=1}^{n} (x_i - \bar{x})^2\right)^2$ - Eleva ao quadrado a média dos quadrados dos desvios em relação à média.

A subtração de 3 na fórmula é um ajuste para a curtose da distribuição normal padrão, que é 3. Portanto, uma distribuição normal terá um coeficiente de curtose de 0.

Interpretando o resultado:
- Se o Coeficiente de Curtose é 0, a distribuição tem a mesma forma que a distribuição normal padrão (mesocúrtica).
- Se o Coeficiente de Curtose é maior que 0, a distribuição é mais pronunciada (leptocúrtica) e tem caudas mais pesadas.
- Se o Coeficiente de Curtose é menor que 0, a distribuição é menos pronunciada (platicúrtica) e tem caudas mais leves.

Essa medida é valiosa na análise estatística para compreender a forma e a concentração dos dados em torno da média.



### Fórmula

Vamos examinar os componentes dessa fórmula:

A curtose é frequentemente definida como:

$ \text{Curtose} = \displaystyle\frac{m_4(\mu)}{\sigma^4} - 3 $

onde:
- $ m_4(\mu) $ é o quarto momento central,
- $ \sigma $ é o desvio-padrão da distribuição,
- $ \mu $ é a média da distribuição.

O quarto momento central $ m_4(\mu) $ é calculado como a expectativa matemática do quarto poder das diferenças entre os valores da variável aleatória e a média:

$ m_4(\mu) = E\left((X - \mu)^4\right) $

Essencialmente, a curtose compara a distribuição em questão com uma distribuição normal padrão. A fórmula subtrai 3 para que uma distribuição normal padrão tenha uma curtose de 0. Valores positivos indicam uma distribuição mais "afiada" (leptocúrtica), enquanto valores negativos indicam uma distribuição mais "achatada" (platicúrtica).

Além disso, alguns textos definem a curtose como a razão entre o quarto momento central e o quadrado do segundo momento central. O segundo momento central $ \mu_2 $ é a variância da distribuição, definida como:

$ \mu_2 = E\left((X - \mu)^2\right) $

A expressão para a curtose neste contexto é:

$ \text{Curtose} = \displaystyle \frac{\mu_4}{\mu_2^2} $

Neste caso, para uma distribuição normal, a curtose seria 3. Vale ressaltar que a curtose não tem um limite superior, ou seja, existem distribuições que podem ter uma curtose tão alta quanto desejado. No entanto, o limite inferior é -2, que ocorre na distribuição Bernoulli com $ p =\displaystyle \frac{1}{2} $.


#### Exercício: Coeficiente de Curtose (kurtosis)  em relação com a curva de uma distribuição normal

A curtose é uma medida estatística que descreve a forma da distribuição de dados, indicando a "espessura" das caudas em relação ao pico. A curtose é frequentemente comparada à curtose de uma distribuição normal, que é zero por definição.

Se a curtose de uma distribuição é maior que zero, ela é considerada leptocúrtica, o que significa que as caudas da distribuição são mais pesadas (mais grossas) do que as da distribuição normal. Se a curtose é menor que zero, a distribuição é platicúrtica, o que significa que as caudas são mais leves (mais finas) do que as da distribuição normal.


Aqui está um exemplo de como você pode calcular a curtose em relação à curva de uma distribuição normal usando Python e a biblioteca NumPy:

```python
import numpy as np

# Gere uma amostra de uma distribuição normal
np.random.seed(0)
dados_normal = np.random.normal(loc=0, scale=1, size=1000)

# Calcular a curtose em relação à curva de uma distribuição normal
curtose = (np.mean((dados_normal - np.mean(dados_normal))**4) / np.mean((dados_normal - np.mean(dados_normal))**2)**2) - 3

print(f'Curtose em relação à curva normal: {curtose}')
```

```
Curtose em relação à curva normal: -0.0467663244783294

```

#### Biblioteca SciPy - stats - describe
```
from scipy.stats import describe
stats.describe(dados_normal)
```

```
DescribeResult(nobs=1000, minmax=(-3.0461430547999266, 2.759355114021582), mean=-0.045256707490195384, variance=0.9752096659781324, skewness=0.03385895323565712, kurtosis=-0.0467663244783294)

```


Neste exemplo, geramos uma amostra de uma distribuição normal usando `np.random.normal`. Em seguida, calculamos a curtose em relação à curva de uma distribuição normal . O resultado ideal seria próximo de zero, indicando uma distribuição normal padrão. 



#### Platicúrtica: Curtose < 3,00.

kurtosis=-0.0467663244783294

Em relação à curva normal, possui grau de achatamento maior que da curva normal padrão, o que nos indica que os dados estão mais espalhados (logo, o desvio padrão também é maior).














&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>