**Python - Estatística** 
>**Amostragem Estratificada**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



### Amostragem Estratificada

```python
# Importação das bibliotecas: pandas para carregar arquivos .csv e train_test_split para divisão da base de dados (separar amostras)
import pandas as pd
from sklearn.model_selection import train_test_split

# Dataset
iris = pd.read_csv('iris.csv')
iris.head(5)
```

**Resultado:**


|   |   sepal length |   sepal width |   petal length |   petal width | class        |
|---|-----------------|--------------|----------------|---------------|--------------|
| 0 |             5.1 |          3.5 |            1.4 |          0.2  | Iris-setosa  |
| 1 |             4.9 |          3.0 |            1.4 |          0.2  | Iris-setosa  |
| 2 |             4.7 |          3.2 |            1.3 |          0.2  | Iris-setosa  |
| 3 |             4.6 |          3.1 |            1.5 |          0.2  | Iris-setosa  |
| 4 |             5.0 |          3.6 |            1.4 |          0.2  | Iris-setosa  |


```python
# Carregamento da base de dados e contagem de quantos registros existem por classe
iris['class'].value_counts()
```

**Resultado:**


|               |   count |
|---------------|---------|
| Iris-setosa   |      50 |
| Iris-versicolor |      50 |
| Iris-virginica |      50 |


```python
# iris.iloc[:, 0:4]: buscamos somente os atributos previsores, ou seja, os dados sobre pétala e sépala da planta
base1 = iris.iloc[:, 0:4]
base1
```

**Resultado:**


|    |   sepal length |   sepal width |   petal length |   petal width |
|---:|-----------------|--------------|----------------|---------------|
|  0 |             5.1 |          3.5 |            1.4 |          0.2  |
|  1 |             4.9 |          3   |            1.4 |          0.2  |
|  2 |             4.7 |          3.2 |            1.3 |          0.2  |
|  3 |             4.6 |          3.1 |            1.5 |          0.2  |
|  4 |             5   |          3.6 |            1.4 |          0.2  |
...


```python
# iris.iloc[:, 4]: buscamos somente a classe, que é a espécie da planta (setosa, virginica ou versicolor)
base2 = iris.iloc[:, 4]
base2
```

**Resultado:**

```
|    | class        |
|---:|:-------------|
|  0 | Iris-setosa  |
|  1 | Iris-setosa  |
|  2 | Iris-setosa  |
|  3 | Iris-setosa  |
|  4 | Iris-setosa  |
...
```

```python
# test_size: selecionamos 50% da base de dados, que serão copiados para as variáveis X e Y. Essa função retorna 4 valores,
# porém, vamos usar somente os 50% da base de dados e por isso colocamos "_" para os outros valores
# stratify: para retornar a amostra baseada na classe
X, _, y, _ = train_test_split(iris.iloc[:, 0:4], iris.iloc[:, 4],
                              test_size = 0.5, stratify = iris.iloc[:, 4])
y.value_counts()
```

**Resultado:**


|               |   count |
|---------------|---------|
| Iris-versicolor |      25 |
| Iris-virginica |      25 |
| Iris-setosa   |      25 |


### Explicando o Código

Este código está realizando a divisão de dados utilizando a função `train_test_split` do scikit-learn. A função `train_test_split` é comumente usada para dividir um conjunto de dados em dois subconjuntos: um para treinamento e outro para teste. Neste caso, ele é usado para dividir um conjunto de dados relacionado ao conjunto de dados Iris.

- `X, _, y, _`: A função `train_test_split` retorna quatro conjuntos de dados, mas neste código os dois conjuntos intermediários são ignorados usando `_`. Os conjuntos relevantes são `X` e `y`, que representam as características (atributos) e as classes, respectivamente.

- `iris.iloc[:, 0:4]`: Seleciona todas as linhas e as colunas de 0 a 3 do DataFrame `iris`, que correspondem aos atributos do conjunto de dados Iris.

- `iris.iloc[:, 4]`: Seleciona todas as linhas da coluna 4 do DataFrame `iris`, que normalmente contém as classes das flores Iris.

- `test_size = 0.5`: Define a proporção dos dados que serão usados para o conjunto de teste, neste caso, metade dos dados.

- `stratify = iris.iloc[:,4]`: O

 parâmetro `stratify` garante que a divisão dos dados mantenha a mesma distribuição das classes no conjunto original, o que é útil quando as classes são desequilibradas.

Em resumo, o código divide o conjunto de dados Iris em duas partes, `X` contendo as características e `y` contendo as classes, garantindo que a proporção das classes seja mantida nos conjuntos de treinamento e teste.




### Explicando todas as saídas - xtr, X, ytr, Y

- `xtr, X, ytr, Y`: Essa linha de código atribui os resultados da função `train_test_split` a quatro variáveis:
  - `xtr`: Representa o conjunto de características (atributos) do conjunto de treinamento.
  - `X`: Representa o conjunto de características (atributos) do conjunto de teste.
  - `ytr`: Representa o conjunto de rótulos (classes) do conjunto de treinamento.
  - `Y`: Representa o conjunto de rótulos (classes) do conjunto de teste.

Essa divisão é comum ao construir e testar modelos de machine learning, pois permite que você treine o modelo em parte dos dados e avalie seu desempenho em outra parte, garantindo que o modelo seja capaz de generalizar para novos dados.


```python
xtr, X, ytr, Y = train_test_split(iris.iloc[:, 0:4], iris.iloc[:, 4],
                              test_size = 0.5, stratify = iris.iloc[:,4])
```



### Variáveis independentes
```python
# Conjunto de características (atributos) do conjunto de treinamento - xtr
xtr
```

**Resultado:**


|    |   sepal length |   sepal width |   petal length |   petal width |
|---:|-----------------|--------------|----------------|---------------|
| 19 |             5.1 |          3.8 |            1.5 |          0.3  |
| 145 |             6.7 |          3   |            5.2 |          2.3  |
| 69 |             5.6 |          2.5 |            3.9 |          1.1  |
| 22 |             4.6 |          3.6 |            1   |          0.2  |
| 59 |             5.2 |          2.7 |            3.9 |          1.4  |
...


```python
# Conjunto de características (atributos) do conjunto de teste - X
X
```

**Resultado:**


|    |   sepal length |   sepal width |   petal length |   petal width |
|---:|-----------------|--------------|----------------|---------------|
| 75 |             6.6 |          3   |            4.4 |          1.4  |
| 46 |             5.1 |          3.8 |            1.6 |          0.2  |
| 20 |             5.4 |          3.4 |            1.7 |          0.2  |
| 54 |             6.5 |          2.8 |            4.6 |          1.5  |
| 76 |             6.8 |          2.8 |            4.8 |          1.4  |
...



### Variáveis dependentes

```python
# Conjunto de rótulos (classes) do conjunto de treinamento - ytr
ytr
```

**Resultado:**


|    | class        |
|---:|:-------------|
| 19 | Iris-setosa  |
| 145 | Iris-virginica |
| 69 | Iris-versicolor |
| 22 | Iris-setosa  |
| 59 | Iris-versicolor |
...


```python
# Conjunto de rótulos (classes) do conjunto de teste - Y
Y
```

**Resultado:**


|    | class        |
|---:|:-------------|
| 75 | Iris-versicolor |
| 46 | Iris-setosa  |
| 20 | Iris-setosa  |
| 54 | Iris-versicolor |
| 76 | Iris-versicolor |
...






&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>