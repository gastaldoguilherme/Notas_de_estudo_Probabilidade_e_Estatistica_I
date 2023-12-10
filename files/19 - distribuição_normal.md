**Python - Estatística** 
>**Amostragem Simples - Teoria**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Distribuição Normal (Gaussiana)

A **distribuição normal** é um modelo bastante útil na estatística, e não seria uma surpresa, pois a soma de efeitos independentes (ou efeitos não muito correlacionados) deveriam, se houvesse muitos desses, se distribuir normalmente (sempre sujeito a certos pressupostos).

A grande utilidade dessa distribuição (função densidade de probabilidade) está associada ao fato de que ela aproxima de forma bastante satisfatória as curvas de frequências de medidas físicas. Essa curva é conhecida como **distribuição normal** ou **gaussiana**.

![Alt text](/assets/19-1.png)



## Parâmetros

A distribuição normal possui dois parâmetros:
- $\mu$ (média): onde está centralizada.
- $\sigma^2$ (variância): que descreve o seu grau de dispersão.
- $\sigma$ (desvio padrão): é comum se referir à dispersão em termos de unidades padrão.

É importante lembrar que a variável $X$ se distribui de forma contínua de $-\infty < x < +\infty$, e a área total sob a curva do modelo é unitária (ou seja, 1).

## Modelo Matemático

O modelo da função normal pode ser expresso matematicamente da seguinte forma:

### Variável Aleatória Generalizada

Seja $X$ uma variável aleatória contínua com média $\mu$, em que $-\infty < x < \infty$, e $\sigma > 0$.

### Função Densidade de Probabilidade

$$f_X(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{1}{2} \left(\frac{x - \mu}{\sigma}\right)^2}, -\infty < x < \infty$$

Podemos dizer que $X$ possui uma distribuição normal e escrever $X \sim \mathcal{N}(\mu,\sigma^2)$.


A fórmula apresentada é a **Função Densidade de Probabilidade** de uma **distribuição normal**. Ela descreve a probabilidade de que uma variável aleatória, denotada como $X$, assuma um valor específico $x$. A fórmula é representada da seguinte::

$$f_X(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{1}{2} \left(\frac{x - \mu}{\sigma}\right)^2}, -\infty < x < \infty$$

Aqui está uma explicação dos componentes da fórmula:

- $f_X(x)$: Representa a probabilidade de que a variável aleatória $X$ tenha um valor igual a $x$.

- $1/\sqrt{2\pi\sigma^2}$: É uma constante de normalização que garante que a área sob a curva da função de densidade seja igual a 1. Isso significa que a integral da função sobre todos os valores possíveis de $x$ é igual a 1.

- $e^{-\frac{1}{2} \left(\frac{x - \mu}{\sigma}\right)^2}$: Esta é a parte exponencial da fórmula. Ela descreve a forma da curva da distribuição normal. A curva é simétrica em torno da média ($\mu$) e diminui exponencialmente à medida que você se afasta da média. O termo $\sigma$ é o desvio padrão, que controla o grau de dispersão dos valores em torno da média.

- $-\infty < x < \infty$: Indica que a distribuição normal abrange todos os valores possíveis de $x$, de menos infinito até mais infinito.

Além disso, a fórmula menciona que $X$ segue uma **distribuição normal** com média $\mu$ e variância $\sigma^2$, o que é representado como $X \sim \mathcal{N}(\mu, \sigma^2)$. Isso significa que a média de $X$ é $\mu$, e a variância de $X$ é $\sigma^2$.

O valor esperado (ou média) da distribuição normal é dado por $E[X] = \mu$, o que significa que, em média, os valores da variável aleatória $X$ se aproximam da média $\mu$. A variância da distribuição normal é dada por $V(X) = \sigma^2$, o que mede a dispersão dos valores em torno da média.

Em resumo, a função densidade de probabilidade descreve como os valores de uma variável aleatória estão distribuídos em torno de sua média em uma distribuição normal, e os parâmetros $\mu$ e $\sigma^2$ determinam a posição e a dispersão dessa distribuição.



### Valor Esperado e Variância

$E[X] = \mu$

$V(X) = \sigma^2$

### Cálculo da Probabilidade

$$
P(a < X < b) = \int_{a}^{b} \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{1}{2} \left(\frac{x - \mu}{\sigma}\right)^2} dx
$$

Cabe notar que a integral da função densidade de probabilidade normal não possui solução analítica, sendo neste caso o seu cálculo deve ser realizado por uma aproximação, método numérico.





### Calculando as probabilidades de uma distribuição normal

Para uma distribuição normal dada por $X \sim \mathcal{N}(\mu=10, \sigma^2=4)$ ou ($\sigma=2$), podemos calcular as seguintes probabilidades, ou seja, as áreas sob a curva da distribuição normal utilizando o Python.

```
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Parâmetros da distribuição normal
mu = 10  # Média centralizada em 0
sigma = 2  # Desvio padrão

# Limites do intervalo
a = 8  # [a,b]=[8,12]; [6,14]; [4,16]; 
b = 12

# Criar um conjunto de valores para o eixo x
x = np.linspace(mu - 4 * sigma, mu + 4 * sigma, 1000)

# Calcular a função de densidade de probabilidade
pdf = stats.norm.pdf(x, loc=mu, scale=sigma)

# Calcular a probabilidade entre a e b
probability = stats.norm.cdf(b, loc=mu, scale=sigma) - stats.norm.cdf(a, loc=mu, scale=sigma)

# Criar o gráfico da densidade de probabilidade
plt.plot(x, pdf, label="Densidade de Probabilidade")
plt.fill_between(x, pdf, where=(x >= a) & (x <= b), alpha=0.3, label=f'Probabilidade = {probability:.2f}')
plt.axvline(x=mu, color='red', linestyle='--', label=f'Média = {mu}')
plt.xlabel('X')
plt.ylabel('Densidade de Probabilidade')
plt.legend()
plt.title('Gráfico da Distribuição Normal (Centrado em x=0)')
plt.grid(True)

# Mostrar o gráfico
plt.show()

```


**Exemplo:**

1. Probabilidade entre os valores de $X$ no intervalo $[8, 12]$



![Alt text](/assets/19-2.png)




2. Probabilidade entre os valores de $X$ no intervalo $[6, 14]$



![Alt text](/assets/19-3.png)




3. Probabilidade entre os valores de $X$ no intervalo $[4, 16]$



![Alt text](/assets/19-4.png)



## Exemplos

- Probabilidade entre os valores de $X$ no intervalo $[8, 12] \approx 0.68$
- Probabilidade entre os valores de $X$ no intervalo $[6, 14] \approx 0.95$
- Probabilidade entre os valores de $X$ no intervalo $[4, 16] \approx 0.99$

## Distribuição Normal Padronizada

A **distribuição normal padronizada** possui sempre os mesmos parâmetros: $\mu = 0$ e $\sigma^2 = 1$. É uma distribuição normal padrão.

### Padronização de uma Variável Aleatória Normal

Se $X$ for uma variável aleatória normal com $E[X] = \mu$ e $V(X) = \sigma^2$, a variável aleatória $Z$ será uma variável aleatória normal padrão, com $E[Z] = 0$ e $V(Z) = 1$. Ou seja, $Z$ é uma variável aleatória normal padrão.

## Exemplo de Padronização

Para alguns valores da $X \sim \mathcal{N}(\mu = 100, \sigma^2 = 25)$, vamos manualmente converter $X = 85, 90, 95, 100, 105, 110, 115$ em valores $Z$:


**Gráfico da Distribuição Normal (Centrado em x=100)**

```
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Parâmetros da distribuição normal
mu = 100  # Média centralizada em 0
sigma = 5  # Desvio padrão

# [a,b] = [85,100], [90,100],[95,100],[100,100],[100,105],[100,110],[100,115] Defina os valores de "a" e "b" desejados

# Limites do intervalo
a = 100  
b = 100

# Criar um conjunto de valores para o eixo x
x = np.linspace(mu - 4 * sigma, mu + 4 * sigma, 1000)

# Calcular a função de densidade de probabilidade
pdf = stats.norm.pdf(x, loc=mu, scale=sigma)

# Calcular a probabilidade entre a e b
probability = stats.norm.cdf(b, loc=mu, scale=sigma) - stats.norm.cdf(a, loc=mu, scale=sigma)

# Criar o gráfico da densidade de probabilidade
plt.plot(x, pdf, label="Densidade de Probabilidade")
plt.fill_between(x, pdf, where=(x >= a) & (x <= b), alpha=0.3, label=f'Probabilidade = {probability:.2f}')
plt.axvline(x=mu, color='red', linestyle='--', label=f'Média = {mu}')
plt.xlabel('X')
plt.ylabel('Densidade de Probabilidade')
plt.legend()
plt.title('Gráfico da Distribuição Normal (Centrado em x=100)')
plt.grid(True)

# Mostrar o gráfico
plt.show()

```

**Gráfico da Distribuição Normal Padrão (Z)**

```
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Parâmetros da distribuição normal
mu = 0  # Média centralizada em 0
sigma = 1  # Desvio padrão

# Limites do intervalo
a = 0  # Defina os valores de "a" e "b" desejados
b = 3

# Criar um conjunto de valores para o eixo x
x = np.linspace(mu - 4 * sigma, mu + 4 * sigma, 1000)

# Calcular a função de densidade de probabilidade
pdf = stats.norm.pdf(x, loc=mu, scale=sigma)

# Calcular a probabilidade entre a e b
probability = stats.norm.cdf(b, loc=mu, scale=sigma) - stats.norm.cdf(a, loc=mu, scale=sigma)

# Criar o gráfico da densidade de probabilidade
plt.plot(x, pdf, label="Densidade de Probabilidade (Z)")
plt.fill_between(x, pdf, where=(x >= a) & (x <= b), alpha=0.3, label=f'Probabilidade = {probability:.2f}')
plt.axvline(x=mu, color='red', linestyle='--', label=f'Média = {mu}')
plt.xlabel('X')
plt.ylabel('Densidade de Probabilidade')
plt.legend()
plt.title('Gráfico da Distribuição Normal Padrão (Z)')
plt.grid(True)

# Mostrar o gráfico
plt.show()


```

---
$$X = 85, 90, 95, 100, 105, 110, 115$$

$$Z = \frac{X - \mu}{\sigma}$$

$$(\mu = 100, \sigma^2 = 25)$$
---

- $X = 85 \rightarrow Z = -3$

$Z = \frac{85 - 100}{5} = -3$



| X = 85  | Z = -3|
| --- | --- |
| ![Alt text](/assets/19-5.png) | ![Alt text](/assets/19-6.png) |


- $X = 90 \rightarrow Z = -2$

- $Z = \frac{90 - 100}{5} = -2$



| X = 90  | Z = -2|
| --- | --- |
| ![Alt text](/assets/19-7.png) | ![Alt text](/assets/19-8.png) |



- $X = 95 \rightarrow Z = -1$

- $Z = \frac{95 - 100}{5} = -1$



| X = 95  | Z = -1|
| --- | --- |
| ![Alt text](/assets/19-9.png) | ![Alt text](/assets/19-10.png) |



- $X = 100 \rightarrow Z = 0$

- $Z = \frac{100 - 100}{5} = 0$



| X = 100  | Z = 0|
| --- | --- |
| ![Alt text](/assets/19-11.png) | ![Alt text](/assets/19-12.png) |



- $X = 105 \rightarrow Z = 1$

- $Z = \frac{105 - 100}{5} = 1$



| X = 105  | Z = 1|
| --- | --- |
| ![Alt text](/assets/19-13.png) | ![Alt text](/assets/19-14.png) |




- $X = 110 \rightarrow Z = 2$

- $Z = \frac{110 - 100}{5} = 2$



| X = 110  | Z = 2|
| --- | --- |
| ![Alt text](/assets/19-15.png) | ![Alt text](/assets/19-16.png) |



- $X = 115 \rightarrow Z = 3$

- $Z = \frac{115 - 100}{5} = 3$

| X = 115  | Z = 3|
| --- | --- |
| ![Alt text](/assets/19-17.png) | ![Alt text](/assets/19-18.png) |



Os valores de $Z$ também podem ser interpretados como o número de desvios padrão afastados da média em uma distribuição normal padrão.

## Conclusão

A distribuição normal é uma ferramenta poderosa na estatística, permitindo modelar e compreender a variabilidade em uma ampla gama de fenômenos. A padronização para a distribuição normal padrão simplifica o cálculo de probabilidades e é amplamente utilizada na análise estatística.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
