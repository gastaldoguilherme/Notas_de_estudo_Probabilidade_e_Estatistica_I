**Python - Estatística** 
>**Medidas de Variabilidade - Variância**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

A variância é uma medida de variabilidade estatística que indica o quão dispersos estão os valores de um conjunto de dados em relação à média. Em outras palavras, a variância quantifica a dispersão ou a propagação dos valores em torno da média. Quanto maior a variância, mais dispersos os dados; quanto menor a variância, mais próximos os dados estão da média.

A fórmula da variância, denotada por `σ²` (sigma ao quadrado) para uma população ou `S²` (S ao quadrado) para uma amostra, é a seguinte:

Para uma população:
$ \displaystyle\ \sigma² = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2 $

Para uma amostra:
$ \displaystyle\ S² = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2 $

Onde:
- $ \sigma² $ ou $ S² $ é a variância para a população ou amostra, respectivamente.
- $ N $ é o tamanho da população.
- $ n $ é o tamanho da amostra.
- $ x_i $ representa cada valor individual no conjunto de dados.
- $ \mu $ é a média da população.
- $ \bar{x} $ é a média da amostra.

Para calcular a variância, você segue estas etapas:

1. Calcule a média dos dados ($ \mu $ ou $ \bar{x} $).
2. Subtraia a média de cada valor no conjunto de dados.
3. Eleve ao quadrado cada uma das diferenças.
4. Calcule a média dos valores resultantes (a soma das diferenças ao quadrado dividida pelo número de dados menos 1 para amostras).
5. Esse valor é a variância.

A variância é uma medida importante em estatística, frequentemente usada para avaliar a dispersão dos dados e calcular o desvio padrão, que é a raiz quadrada da variância e fornece uma medida de dispersão mais facilmente interpretável em termos das unidades dos dados originais.




## Usos da Variância

A variância tem vários usos e funções importantes em estatística e análise de dados. Aqui estão alguns dos principais usos e funções da variância:

1. Medida de dispersão: A variância é uma medida fundamental de dispersão que indica o quão espalhados estão os dados em relação à média. Uma variância maior indica maior dispersão, enquanto uma variância menor indica menor dispersão.

2. Avaliação da variabilidade: A variância é útil para comparar a variabilidade de diferentes conjuntos de dados. Por exemplo, você pode comparar a variância de dois grupos de dados para determinar quão consistentes ou variáveis são em relação à média.

3. Análise de risco: A variância é comumente usada em finanças e gestão de investimentos para avaliar o risco associado a um ativo financeiro. Um ativo com alta variância é considerado mais arriscado, pois os retornos são mais voláteis.

4. Controle de qualidade: Em controle estatístico de processos, a variância é usada para monitorar a variabilidade de um processo de fabricação. Se a variância aumentar, pode ser um sinal de que o processo não está sob controle.

5. Otimização em pesquisa operacional: A variância é usada em problemas de otimização para ajudar a minimizar ou maximizar uma função sujeita a restrições. Por exemplo, minimizar o custo de produção sujeito a uma variância máxima.

6. Estimação de incerteza: Em análise de dados experimentais, a variância é usada para quantificar a incerteza associada às medições. Uma variância mais alta indica maior incerteza nas medições.

7. Seleção de modelos estatísticos: Em análise de regressão, a variância é usada para avaliar a adequação do modelo aos dados. Modelos com variância residual mais baixa são geralmente preferidos, pois indicam um melhor ajuste aos dados.

8. Desenvolvimento de intervalos de confiança: A variância é usada para calcular intervalos de confiança ao estimar parâmetros populacionais a partir de amostras. Ela desempenha um papel fundamental na determinação da precisão das estimativas.

9. Análise de variação: Em análise de variância (ANOVA), a variância é usada para avaliar a contribuição de diferentes fontes de variação em um conjunto de dados. Isso ajuda a entender se os grupos são significativamente diferentes uns dos outros.

Em resumo, a variância desempenha um papel crítico na análise estatística e na interpretação de dados. Ela fornece informações valiosas sobre a dispersão e a variabilidade dos dados, sendo uma ferramenta essencial para a tomada de decisões, o controle de qualidade e a avaliação de riscos em várias áreas.


## Exemplos práticos:

### Exemplo 1:

1. Medida de Dispersão:
   - Conjunto de dados: Alturas de 5 estudantes (em centímetros) - [160, 165, 155, 170, 150].
   - Fórmula usada: Variância = Σ(xi - μ)² / n, onde xi são os valores, μ é a média e n é o número de observações.
   - Cálculo: Média (μ) = (160 + 165 + 155 + 170 + 150) / 5 = 160.
   - Variância = [(160 - 160)² + (165 - 160)² + (155 - 160)² + (170 - 160)² + (150 - 160)²] / 5 = 50.
   - Conclusão: A variância de 50 (cm)² indica que as alturas estão relativamente espalhadas em relação à média de 160, sugerindo dispersão moderada.

```
#1° modo:
media1 = np.mean(dados1)
var1= np.var(dados1)
print("Média:", media1)
print("Variância:", var1)
```
```
Média: 160.0 (cm)
Variância: 50.0 (cm)²
```


```
#2° modo:
# Seu conjunto de dados
dados1 = [160, 165, 155, 170, 150]

# Calcule a média dos dados
media = sum(dados1) / len(dados1)

# Use a fórmula da variância
variancia = sum((x - media) ** 2 for x in dados1) / len(dados1)

# Imprima o resultado
print("Média:", media)
print("Variância:", variancia)
```
```
Resposta: 
Média: 160.0 (cm)
Variância: 50.0 (cm)²

```


### Exemplo 2:
2. Avaliação da Variabilidade:
   - Conjunto de dados 1: Níveis de poluição do ar em uma cidade ao longo de 5 dias - [30, 35, 40, 25, 30].
   - Conjunto de dados 2: Níveis de poluição do ar em outra cidade ao longo de 5 dias - [20, 22, 23, 25, 21].


### Resolução Exemplo 2:
"Variância Amostral (com n-1):"
**Conjunto de dados 21 (Cidade 1):**
Níveis de poluição (partes por milhão (ppm)) do ar ao longo de 5 dias - [30, 35, 40, 25, 30].
**Conjunto de dados 22 (Cidade 2):**
Níveis de poluição partes por milhão (ppm) do ar ao longo de 5 dias - [20, 22, 23, 25, 21].

```
#1° modo:
# Use a fórmula da variância amostral com n-1
variancia_amostral21 = np.var(dados21, ddof=1)
variancia_amostral22 = np.var(dados22, ddof=1)
print("Variância21:", variancia_amostral21)
print("Variância21:", variancia_amostral22)

```
```
Resposta: 
Variância21: 32.5 (ppm)²
Variância21: 3.7 (ppm)²
```
```
#2° modo:
# Seu conjunto de dados
dados21 = [30, 35, 40, 25, 30]
dados22 = [20, 22, 23, 25, 21]

# Calcule a média dos dados
media21 = sum(dados21) / len(dados21)
media22 = sum(dados22) / len(dados22)

# Use a fórmula da variância
variancia21 = sum((x - media21) ** 2 for x in dados21) / (len(dados21)-1)
variancia22 = sum((x - media22) ** 2 for x in dados22) / (len(dados21)-1)
```
```
# Imprima o resultado
print("Média21:", media21)
print("Variância21:", variancia21)

print("Média22:", media22)
print("Variância22:", variancia22)
```
```
Resposta: 
Média21: 32.0 (ppm)
Variância21: 32.5 (ppm)²
Média22: 22.2 (ppm)
Variância22: 3.7 (ppm)²
```

Conclusão: A variância do conjunto de dados 21 é 32.5 (ppm)², enquanto a do conjunto de dados 22 é 3.70 (ppm)². Isso indica que a primeira cidade tem uma variabilidade muito maior nos níveis de poluição do ar ao longo dos 5 dias em comparação com a segunda cidade. Portanto, os dados da primeira cidade estão mais dispersos em relação à média, sugerindo uma maior variabilidade nos níveis de poluição do ar nessa cidade.


### Exemplo 3:
"Variância Amostral (com n-1):"

3. Análise de Risco:
   - Ativo financeiro A: Retornos mensais percentuais ao longo de 10 meses - [2%, 3%, -1%, 1%, 2%, -2%, 1%, 3%, 0%, -1%].
   - Ativo financeiro B: Retornos mensais percentuais ao longo de 10 meses - [4%, 5%, -3%, 4%, 3%, -4%, 2%, 5%, 1%, -2%].


### Resolução Exemplo 3:


**Ativo Financeiro A:**
Retornos mensais percentuais ao longo de 10 meses - [2%, 3%, -1%, 1%, 2%, -2%, 1%, 3%, 0%, -1%].

**Ativo Financeiro B:**
Retornos mensais percentuais ao longo de 10 meses - [4%, 5%, -3%, 4%, 3%, -4%, 2%, 5%, 1%, -2%].


```
#1° modo:
# Use a fórmula da variância amostral com n-1
variancia_amostral31 = np.var(dados31, ddof=1)
variancia_amostral32 = np.var(dados32, ddof=1)
print("Variância31:", variancia_amostral31)
print("Variância32:", variancia_amostral32)

```
```
Variância31: 0.0307 %²
Variância32: 0.1139 %²

```

```
#2° modo:
# Seu conjunto de dados
dados31 = [0.02, 0.03, -0.01, 0.01, 0.02, -0.02, 0.01, 0.03, 0, -0.01]
dados32 = [0.04, 0.05, -0.03, 0.04, 0.03, -0.04, 0.02, 0.05, 0.01, -0.02]

# Calcule a média dos dados
media31 = sum(dados31) / len(dados31)
media32 = sum(dados32) / len(dados32)

# Use a fórmula da variância
variancia31 = sum((x - media31) ** 2 for x in dados31) / (len(dados31)-1)
variancia32 = sum((x - media32) ** 2 for x in dados32) / (len(dados31)-1)


# Imprima o resultado
print("Média31:", media31)
print("Variância31:", variancia31)

print("Média32:", media32)
print("Variância32:", variancia32)


```

```
Média31: 0.8 %
Variância31: 0.0307 %²
Média32: 1.5000 %
Variância32: 0.1139 %²
```

Conclusão: O ativo financeiro B (variância:0.1139 %² ) é mais arriscado do que o ativo financeiro A (variância:0.0307 %² ), pois tem uma variância de retorno maior, indicando maior volatilidade nos retornos. Isso significa que os retornos mensais do ativo B são mais imprevisíveis e variáveis em comparação com os retornos do ativo A, tornando-o mais arriscado para os investidores.


### Exemplo 4:
"Variância Amostral (com n-1):"

4. Controle de Qualidade:
   - Peso de 5 embalagens de açúcar em gramas - [500, 505, 503, 498, 502].
   - Variância é usada para monitorar a variabilidade no peso das embalagens. Se a variância aumentar, pode indicar problemas no processo de enchimento de açúcar.

### Resolução Exemplo 4:

**Conjunto de dados:**
Peso de 5 embalagens de açúcar em gramas - [500, 505, 503, 498, 502].

1. Calcule a média (x-barra) dos pesos das embalagens:
   μ = (500 + 505 + 503 + 498 + 502) / 5 = 2508 / 5 = 501.6.

2. Calcule as diferenças entre cada valor e a média, eleve ao quadrado e some esses quadrados:
   [(500 - 501.6)² + (505 - 501.6)² + (503 - 501.6)² + (498 - 501.6)² + (502 - 501.6)²] ≈ [2.56 + 11.56 + 2.56 + 12.96 + 0.16] ≈ 30.8.

3. Divida a soma pelo número de observações menos 1 (n-1), que é 4:
   Variância ≈ 30.8 / 4 ≈ 7.3 gramas².


```
#1° modo:
# Use a fórmula da variância amostral com n-1
variancia_amostral = np.var(dados, ddof=1)

print("Variância:", variancia_amostral)
```

```
Variância: 7.3000 gramas²
```
```
#2° modo:
# Seu conjunto de dados
dados = [500, 505, 503, 498, 502]


# Calcule a média dos dados
media = sum(dados) / len(dados)


# Use a fórmula da variância
variancia = sum((x - media) ** 2 for x in dados) / (len(dados)-1)



# Imprima o resultado
print("Média:", media)
print("Variância:", variancia)
```
```
Média: 501.6
Variância: 7.3000 gramas²
```

Conclusão: A variância de 7.3 gramas² indica a variabilidade nos pesos das embalagens de açúcar. Quando a variância é monitorada ao longo do tempo e se observa um aumento significativo, pode ser um sinal de problemas no processo de enchimento de açúcar, como inconsistências nas quantidades. Portanto, a variância é uma ferramenta útil no controle de qualidade para garantir que os produtos atendam aos padrões desejados.



### Exemplo 5:
"Variância Amostral (com n-1):"

5. Otimização em Pesquisa Operacional:
   - Em uma linha de produção, a variância da espessura de peças metálicas é monitorada para otimizar a produção. O objetivo é minimizar a variância da espessura enquanto atende às especificações.

### Resolução Exemplo 5:  
Suponha que temos uma linha de produção de peças metálicas, e a espessura das peças é um parâmetro crítico. O objetivo é produzir peças com uma espessura consistente, mas minimizar a variância da espessura para economizar material. Vamos coletar dados de espessura de 10 peças.

**Conjunto de dados:**
Espessura de 10 peças metálicas em milímetros - [5.2, 5.3, 5.1, 5.4, 5.0, 5.2, 5.3, 5.2, 5.3, 5.1].

```
#1° modo:
# Use a fórmula da variância amostral com n-1
variancia_amostral = np.var(dados, ddof=1)

print("Variância:", variancia_amostral)
```
```
Variância: 0.01433mm²
```

```
#2° modo:
# Seu conjunto de dados
dados = [5.2, 5.3, 5.1, 5.4, 5.0, 5.2, 5.3, 5.2, 5.3, 5.1]


# Calcule a média dos dados
media = sum(dados) / len(dados)


# Use a fórmula da variância
variancia = sum((x - media) ** 2 for x in dados) / (len(dados)-1)



# Imprima o resultado
print("Média:", media)
print("Variância:", variancia)
```
```
Média: 5.21 mm
Variância: 0.01433mm²
```


Neste contexto, a variância (0.01433mm²) é uma medida da variabilidade na espessura das peças metálicas. O objetivo da otimização em pesquisa operacional seria minimizar essa variância, o que resultaria em produzir peças com uma espessura mais consistente e, ao mesmo tempo, economizar material. Portanto, o controle da variância é crucial para a otimização do processo de produção.


### Exemplo 6:
"Variância Amostral (com n-1):"

6. Estimação de Incerteza:
   - Medidas de temperatura de um termômetro digital em 5 leituras consecutivas - [25.2°C, 25.1°C, 25.4°C, 25.3°C, 25.2°C].
   - A variância é usada para quantificar a incerteza associada às medições de temperatura. Uma variância mais alta indica maior incerteza.


### Resolução Exemplo 6: 
Para demonstrar o cálculo da variância no contexto de estimação de incerteza, vamos considerar medidas de temperatura de um termômetro digital em 5 leituras consecutivas:

**Conjunto de dados:**
Medidas de temperatura em graus Celsius em 5 leituras consecutivas - [25.2°C, 25.1°C, 25.4°C, 25.3°C, 25.2°C].

```
#1° modo:
# Use a fórmula da variância amostral com n-1
variancia_amostral = np.var(dados, ddof=1)

print("Variância:", variancia_amostral)
```
```
Variância: 0.0130 °C²
```
```
#2° modo:
# Seu conjunto de dados
dados = [25.2, 25.1, 25.4, 25.3, 25.2]


# Calcule a média dos dados
media = sum(dados) / len(dados)


# Use a fórmula da variância
variancia = sum((x - media) ** 2 for x in dados) / (len(dados)-1)



# Imprima o resultado
print("Média:", media)
print("Variância:", variancia)
```
```
Média: 25.24 °C
Variância: 0.0130 °C²
```


Neste contexto, a variância é usada para quantificar a incerteza associada às medições de temperatura. Uma variância mais alta indica maior dispersão das medições em relação à média, o que sugere maior incerteza nas medições de temperatura. Portanto, nesse exemplo, a variância de 0.0130°C² indica que as medições de temperatura têm uma incerteza relativamente baixa.


### Exemplo 7:
"Variância Amostral (com n-1):"

7. Seleção de Modelos Estatísticos:
   - Duas equações de regressão linear ajustadas a um conjunto de dados. Modelo 1 tem uma variância residual de 20, e o Modelo 2 tem uma variância residual de 15. O Modelo 2 é preferido devido à menor variância residual, indicando um melhor ajuste aos dados.


### Resolução Exemplo 7: 

Para demonstrar o uso da variância na seleção de modelos estatísticos, vamos considerar dois modelos de regressão linear ajustados a um conjunto de dados. A variância residual é usada para avaliar o ajuste dos modelos aos dados.

**Modelo 1:**
Variância residual = 20.

**Modelo 2:**
Variância residual = 15.

Em análise de modelos estatísticos, modelos com uma variância residual mais baixa são geralmente preferidos, pois indicam um melhor ajuste aos dados. A variância residual representa a dispersão dos resíduos, ou seja, a diferença entre os valores observados e os valores previstos pelo modelo.

Neste caso, o "Modelo 2" é preferido, pois tem uma variância residual de 15, que é menor do que a variância residual do "Modelo 1", que é 20. Isso indica que o "Modelo 2" tem um melhor ajuste aos dados, pois os resíduos são menos dispersos, o que sugere que ele é mais preciso na previsão dos valores observados no conjunto de dados. Portanto, a seleção do "Modelo 2" é baseada na menor variância residual, que é uma medida de melhor ajuste aos dados.



### Exemplo 8:
"Variância Amostral (com n-1):"

8. Desenvolvimento de Intervalos de Confiança:
   - Amostra de 100 consumidores para estimar a média de gastos mensais. A variância amostral é usada para calcular intervalos de confiança ao estimar a média da população, determinando a precisão da estimativa.

### Resolução Exemplo 8: 

Para demonstrar o uso da variância no desenvolvimento de intervalos de confiança, vamos considerar uma amostra de 100 consumidores usada para estimar a média de gastos mensais. A variância amostral é usada para calcular intervalos de confiança e determinar a precisão da estimativa da média da população.

Suponhamos que temos uma amostra de gastos mensais de 100 consumidores e que desejamos estimar a média de gastos mensais da população. Vamos calcular a variância amostral da amostra para demonstrar seu uso no desenvolvimento de intervalos de confiança:

**Amostra de gastos mensais (valores hipotéticos):**
[150, 200, 180, 220, ...] (100 valores no total).

1. Calcule a média (μ) da amostra de gastos mensais.

2. Calcule as diferenças entre cada valor na amostra e a média, eleve ao quadrado e some esses quadrados.

3. Divida a soma pelo número de observações menos 1 (n-1) para obter a variância amostral.

4. Para calcular um intervalo de confiança para a média da população, você usaria a variância amostral e o tamanho da amostra (n) juntamente com um nível de confiança desejado, geralmente representado por um valor crítico Z (ou T, dependendo do tamanho da amostra) a partir das tabelas de distribuição normal ou t-Student.

A variância amostral é fundamental para calcular a precisão do intervalo de confiança. Quanto menor a variância amostral, mais estreito será o intervalo de confiança, indicando uma estimativa mais precisa da média populacional. Por outro lado, uma variância amostral maior resultaria em um intervalo de confiança mais amplo, o que indica uma estimativa menos precisa da média populacional.

Assim, a variância amostral desempenha um papel crítico na determinação da precisão das estimativas de intervalos de confiança ao estimar a média da população a partir de uma amostra.



### Exemplo 9:
"Variância Amostral (com n-1):"

9. Análise de Variação:
   - Três grupos de estudantes submetidos a diferentes métodos de ensino. A variância é usada em ANOVA para avaliar a contribuição de diferentes métodos de ensino para a variação no desempenho dos grupos. Isso ajuda a determinar se os métodos de ensino são significativamente diferentes uns dos outros.

### Resolução Exemplo 9: 

Para demonstrar o uso da variância na análise de variação (ANOVA) para avaliar a contribuição de diferentes métodos de ensino para a variação no desempenho de grupos de estudantes, vamos considerar um exemplo hipotético com três grupos de estudantes submetidos a diferentes métodos de ensino.

Suponhamos que temos três grupos de estudantes (Grupo A, Grupo B e Grupo C) submetidos a diferentes métodos de ensino, e estamos interessados em determinar se os métodos de ensino têm um impacto significativo no desempenho dos grupos. Vamos calcular a variância do desempenho dos grupos para demonstrar como a ANOVA é usada.

**Desempenho dos Grupos (valores hipotéticos):**
Grupo A: [85, 90, 88, 92, 87] (5 alunos).
Grupo B: [78, 82, 79, 85, 80] (5 alunos).
Grupo C: [95, 93, 97, 96, 94] (5 alunos).

1. Calcule a média (x-barra) do desempenho de cada grupo.

2. Calcule a soma dos quadrados das diferenças entre cada valor no grupo e a média do grupo.

3. Divida a soma pelo número de observações menos 1 (n-1) para obter a variância dentro de cada grupo.

4. Calcule a média das médias dos grupos (grand mean).

5. Calcule a soma dos quadrados das diferenças entre a média de cada grupo e o grand mean.

6. Divida a soma pelo número de grupos (k) menos 1 para obter a variância entre os grupos.

7. Use o resultado da variância dentro de grupos e a variância entre grupos para realizar o teste ANOVA, que avalia se as diferenças entre os grupos são estatisticamente significativas.

Se a variância entre grupos for significativamente maior do que a variância dentro dos grupos, isso indicaria que os métodos de ensino têm um impacto significativo no desempenho dos grupos, ou seja, os grupos são significativamente diferentes uns dos outros em termos de desempenho.

Portanto, a variância é uma ferramenta essencial na análise de variação (ANOVA) para determinar se os métodos de ensino são significativamente diferentes em termos de impacto no desempenho dos grupos de estudantes.



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>