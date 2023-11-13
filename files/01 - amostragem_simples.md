**Python - Estatística** 
>**Amostragem Simples**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Amostragem Simples


### Definição da semente (seed)


O código `np.random.seed()` é usado para definir a semente (seed) para o gerador de números aleatórios do módulo NumPy, garantindo que a sequência de números aleatórios seja reproduzível. Vamos explicar os componentes desse código:

- `np.random`: É o módulo de geração de números aleatórios do NumPy. Ele fornece funcionalidades para gerar números aleatórios e é amplamente usado em tarefas relacionadas à aleatoriedade, como amostragem aleatória e simulações.

- `seed(2345)`: O método `seed` é usado para inicializar o gerador de números aleatórios com uma semente específica. Neste caso, `2345` é o valor que foi usado como semente. A semente é um valor inicial que permite ao gerador de números aleatórios começar a partir de um ponto específico em sua sequência pseudoaleatória.

Ao definir uma semente específica com `np.random.seed(2345)`, você garante que, se você executar o código novamente em outra instância ou em outro momento, a sequência de números aleatórios gerada pelo NumPy será a mesma. Isso é útil para reproduzir resultados em cenários de pesquisa ou desenvolvimento, onde a aleatoriedade precisa ser controlada e consistente.

Em resumo, `np.random.seed(2345)` inicializa o gerador de números aleatórios do NumPy com a semente 2345, o que torna a geração de números aleatórios determinística e reproduzível.




#### 1° Exemplo:

```python
# Importação das bibliotecas: pandas para carregar arquivos .csv e numpy para gerar números aleatórios
import pandas as pd
import numpy as np

# Suponha que você tenha um DataFrame base
base = pd.DataFrame({'ColunaA': [1, 2, 3, 4, 5, 1],
                     'ColunaB': [6, 7, 8, 9, 10, 1],
                     'ColunaC': [11, 12, 13, 14, 15, 1]})
base
```

Resultado:

|   | ColunaA | ColunaB | ColunaC |
|---|---------|---------|---------|
| 0 |       1 |       6 |      11 |
| 1 |       2 |       7 |      12 |
| 2 |       3 |       8 |      13 |
| 3 |       4 |       9 |      14 |
| 4 |       5 |      10 |      15 |
| 5 |       1 |       1 |       1 |



```python
# Suponha que você tenha um array de índices
np.random.seed(2345)
indice = np.random.choice(a=[0, 1], size=6, replace=True, p=[0.7, 0.3])
indice
```

Resultado:

```
array([1, 1, 0, 1, 0, 0])
```

```python
# Use o método loc para selecionar as linhas com base nos índices igual a zero
base_final = base.loc[indice == 0]
base_final.shape
```

Resultado:

```
(3, 3)
```

```python
base_final
```

Resultado:

|   | ColunaA | ColunaB | ColunaC |
|---|---------|---------|---------|
| 2 |       3 |       8 |      13 |
| 4 |       5 |      10 |      15 |
| 5 |       1 |       1 |       1 |



```python
# Use o método loc para selecionar as linhas com base nos índices igual a um
base_final2 = base.loc[indice == 1]
base_final2.shape
```

Resultado:

```
(3, 3)
```

```python
base_final2
```

Resultado:

|   | ColunaA | ColunaB | ColunaC |
|---|---------|---------|---------|
| 0 |       1 |       6 |      11 |
| 1 |       2 |       7 |      12 |
| 3 |       4 |       9 |      14 |



#### 2° Exemplo:

```python
# Importação das bibliotecas: pandas para carregar arquivos .csv e numpy para gerar números aleatórios
import pandas as pd
import numpy as np

# Carregamento da base de dados (o arquivo .csv precisa estar na mesma pasta do código fonte) e visualização dos dados
base = pd.read_csv('iris.csv')
base
```

Resultado:

| sepal length | sepal width | petal length | petal width |       class       |
|--------------|------------|-------------|------------|-------------------|
|     5.1      |    3.5     |     1.4     |    0.2     |   Iris-setosa     |
|     4.9      |    3.0     |     1.4     |    0.2     |   Iris-setosa     |
|     4.7      |    3.2     |     1.3     |    0.2     |   Iris-setosa     |
|     4.6      |    3.1     |     1.5     |    0.2     |   Iris-setosa     |
|     5.0      |    3.6     |     1.4     |    0.2     |   Iris-setosa     |
|     ...      |    ...     |     ...     |    ...     |   ...             |
|     6.7      |    3.0     |     5.2     |    2.3     |   Iris-virginica  |
|     6.3      |    2.5     |     5.0     |    1.9     |   Iris-virginica  |
|     6.5      |    3.0     |     5.2     |    2.0     |   Iris-virginica  |
|     6.2      |    3.4     |     5.4     |    2.3     |   Iris-virginica  |
|     5.9      |    3.0     |     5.1     |    1.8     |   Iris-virginica  |


```python
# Verificar quantas linhas e colunas existem na base de dados, 150 linhas e 5 colunas
base.shape
```

Resultado:

```
(150,5)
```

```python
# Mudança da semente aleatória randômica para manter os resultados em várias execuções
np.random.seed(2345)

# 150 amostras, de 0 a 1, com reposição, probabilidades equivalentes
amostra = np.random.choice(a=[0, 1], size=150, replace=True, p=[0.7, 0.3])
amostra
```

Resultado:

```
array([0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 0, 1, 0, 1, 1, 1, 0,
       0, 1, 1, 1, 0, 1, 0, 0, 1, 0, 0, 1, 1, 0, 1, 0, 0, 0, 1, 0, 1, 0,
       0, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0,
       0, 1, 0, 0, 1, 0, 0, 0, 0, 1, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0,
       0, 0, 0, 0, 1, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0,
       0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 1, 1, 0, 1, 0, 1, 1,
       1, 0, 0, 0, 0, 0, 0, 0

, 0, 1, 1, 0, 0, 1, 1, 0, 0, 1])
```

```python
# Verificar tamanho da amostra
len(amostra)
```

Resultado:

```
150
```

```python
# Verificar tamanho da amostra para valores igual a 1 e 0
len(amostra[amostra == 1])
```

Resultado:

```
49
```

```python
len(amostra[amostra == 0])
```

Resultado:

```
101
```

```python
base_final = base.loc[amostra == 0]
base_final.shape
```

Resultado:

```
(101, 5)
```

```python
base_final.head()
```

Resultado:

| sepal length | sepal width | petal length | petal width |       class       |
|--------------|------------|-------------|------------|-------------------|
|     5.1      |    3.5     |     1.4     |    0.2     |   Iris-setosa     |
|     4.9      |    3.0     |     1.4     |    0.2     |   Iris-setosa     |
|     4.7      |    3.2     |     1.3     |    0.2     |   Iris-setosa     |
|     4.6      |    3.1     |     1.5     |    0.2     |   Iris-setosa     |
|     5.4      |    3.9     |     1.7     |    0.4     |   Iris-setosa     |


```python
base_final2 = base.loc[amostra == 1]
base_final2.shape
```

Resultado:

```
(49, 5)
```

```python
base_final2.head()
```

Resultado:

| sepal length | sepal width | petal length | petal width |       class       |
|--------------|------------|-------------|------------|-------------------|
|     5.0      |    3.6     |     1.4     |    0.2     |   Iris-setosa     |
|     4.4      |    2.9     |     1.4     |    0.2     |   Iris-setosa     |
|     4.8      |    3.4     |     1.6     |    0.2     |   Iris-setosa     |
|     4.3      |    3.0     |     1.1     |    0.1     |   Iris-setosa     |
|     5.4      |    3.9     |     1.3     |    0.4     |   Iris-setosa     |
|     5.7      |    3.8     |     1.7     |    0.3     |   Iris-setosa     |
|     5.1      |    3.8     |     1.5     |    0.3     |   Iris-setosa     |
|     5.4      |    3.4     |     1.7     |    0.2     |   Iris-setosa     |
|     5.1      |    3.3     |     1.7     |    0.5     |   Iris-setosa     |
|     4.8      |    3.4     |     1.9     |    0.2     |   Iris-setosa     |





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>