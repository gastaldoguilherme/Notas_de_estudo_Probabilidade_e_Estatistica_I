**Python - Estatística** 
>**Medidas de Centralidade e Variabilidade**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


### Medidas de Centralidade e Variabilidade

#### Importação das bibliotecas: scipy para gerar estatísticas mais detalhadas

```python
import numpy as np
from scipy import stats
```

#### Criação da variável com os dados dos jogadores, visualização da mediana e média

```python
jogadores = [40000, 18000, 12000, 250000, 30000, 140000, 300000, 40000, 800000]
np.mean(jogadores)  

# Resultado: 181111.11111111112
```

```python
np.median(jogadores)  

# Resultado: 40000.0
```

#### Criação da variável para geração dos quartis (0%, 25%, 50%, 75% e 100%)

```python
quartis = np.quantile(jogadores, [0, 0.25, 0.5, 0.75, 1])
quartis  # Resultado: array([ 12000.,  30000.,  40000., 250000., 800000.])
```

#### Visualização do desvio padrão

```python
np.std(jogadores, ddof=1)  

# Resultado: 255307.87514511007
```

#### Visualização de estatísticas mais detalhadas usando a biblioteca scipy

```python
stats.describe(jogadores)
```

Resultado:

```
DescribeResult(nobs=9, minmax=(12000, 800000), mean=181111.11111111112, variance=65182111111.11111, skewness=1.758635899846188, kurtosis=1.9572075427527729)
```

### Explicando os resultados:

Os resultados apresentados pela função `stats.describe(jogadores)` fornecem estatísticas detalhadas sobre o conjunto de dados "jogadores", que contém os salários de jogadores, incluindo medidas de centralidade e variabilidade. Vou explicar cada um desses resultados:

1. `nobs=9`: Indica o número de observações (ou amostras) no conjunto de dados. Neste caso, há 9 valores de salário no conjunto.

2. `minmax=(12000, 800000)`: Representa o valor mínimo e máximo no conjunto de dados. O valor mínimo de salário é 12.000 unidades monetárias, enquanto o valor máximo é 800.000 unidades monetárias.

3. `mean=181111.11111111112`: É a média aritmética dos salários no conjunto de dados. A média é aproximadamente 181.111,11 unidades monetárias.

4. `variance=65182111111.11111`: Refere-se à variância dos salários. A variância é uma medida da dispersão dos dados. Quanto maior o valor da variância, mais dispersos estão os dados. Neste caso, a variância é aproximadamente 65.182.111.111,11 unidades monetárias.

5. `skewness=1.758635899846188`: A assimetria (skewness) mede a inclinação da distribuição dos dados. Um valor positivo indica uma inclinação para a direita, enquanto um valor negativo indica uma inclinação para a esquerda. Neste caso, o valor positivo de 1,758 sugere uma inclinação para a direita, o que significa que a distribuição dos salários é assimétrica, com uma cauda direita mais longa.

6. `kurtosis=1.9572075427527729`: A curtose (kurtosis) mede a forma das caudas da distribuição. Um valor maior do que 3 indica caudas pesadas (leptocurtica), enquanto um valor menor do que 3 indica caudas leves (platocurtica). Neste caso, o valor de 1,957 sugere que a distribuição tem caudas leves, o que significa que os salários não têm caudas pesadas e são mais próximos da normalidade.

Em resumo, os resultados indicam que o conjunto de dados de salários dos jogadores possui uma média de aproximadamente 181.111,11 unidades monetárias, uma variância considerável, uma inclinação para a direita e caudas leves na distribuição. Isso fornece informações valiosas sobre a distribuição dos salários no conjunto de dados.








&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>