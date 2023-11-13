**Python - Estatística** 
>**Amostragem sistemática**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



### Importação das bibliotecas
```python
import numpy as np
import pandas as pd
from math import ceil
```

### Criação das variáveis para representar a população, a amostra e o valor de k
A função `ceil` (abreviação de "ceiling") é uma função matemática que arredonda um número para cima para o inteiro mais próximo. Em outras palavras, ela encontra o menor número inteiro que é maior ou igual ao número de ponto flutuante (número real) fornecido como entrada.
```python
populacao = 150
amostra = 15
k = ceil(populacao / amostra)
print(k)
```
Resultado: 10

### Definição do valor randômico para inicializar a amostra, iniciando em 1 até k + 1
```python
np.random.seed(4)
r = np.random.randint(low=1, high=k + 1, size=1)
print(r)
```
Resultado: [8]

```python
acumulador = r[0]
```

Resultado: 8

### Criamos um loop `for` para somar os próximos valores, baseados no primeiro valor de `r` que foi definido acima
```python
acumulador = r[0]
sorteados = []
for i in range(amostra):
    print(acumulador)
    sorteados.append(acumulador)
    acumulador += k
print(sorteados)
```


Explicando o laço:
- `acumulador` é inicializado com o valor de `r[0]`, que é 8.
- `sorteados` é uma lista vazia no início.
- `amostra` é uma sequência de números de 0 a 14.
- `k` é calculado como 10 com base na divisão de `populacao` por `amostra`.

| i  | acumulador | sorteados        |
|---|------------|-----------------|
| 0  | 8            | [8]                 |
| 1  | 18          | [8, 18]          |
| 2  | 28          | [8, 18, 28]   |
| 3  | 38          | [8, 18, 28, 38] |
| 4  | 48          | [8, 18, 28, 38, 48] |
| 5  | 58          | [8, 18, 28, 38, 48, 58] |
| 6  | 68          | [8, 18, 28, 38, 48, 58, 68] |
| 7  | 78          | [8, 18, 28, 38, 48, 58, 68, 78] |
| 8  | 88          | [8, 18, 28, 38, 48, 58, 68, 78, 88] |
| 9  | 98          | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98] |
| 10 | 108        | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108] |
| 11 | 118        | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118] |
| 12 | 128        | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118, 128] |
| 13 | 138        | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118, 128, 138] |
| 14 | 148        | [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118, 128, 138, 148] |


Resultado:
```
8
18
28
38
48
58
68
78
88
98
108
118
128
138
148

[8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118, 128, 138, 148]
```

```python
sorteados
```

Resultado: [8, 18, 28, 38, 48, 58, 68, 78, 88, 98, 108, 118, 128, 138, 148]

### Carregamos a base de dados e criamos a `base_final` somente com os valores sorteados
```python
base = pd.read_csv('iris.csv')
base_final = base.loc[sorteados]
base_final.head()
```

Resultado:

|   sepal length |   sepal width |   petal length |   petal width | class       |
|--------------:|-------------:|--------------:|-------------:|:------------|
|           4.4  |          2.9  |          1.4  |         0.2  | Iris-setosa |
|           5.7  |          3.8  |          1.7  |         0.3  | Iris-setosa |
|           5.2  |          3.4  |          1.4  |         0.2  | Iris-setosa |
|           4.4  |          3.0  |          1.3  |         0.2  | Iris-setosa |
|           5.3  |          3.7  |          1.5  |         0.2  | Iris-setosa |




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>