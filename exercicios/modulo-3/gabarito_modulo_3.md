# Gabarito

## Módulo 3 - Visualização de Dados

### Questão 1
```python
import pandas as pd
import matplotlib.pyplot as plt

df_escola = pd.read_csv("datasets/escolhidos_ava_2/EquipeA_escola.csv")

plt.bar(df_escola["nome"], df_escola["nota"])
plt.show()
```

### Questão 2
```python
plt.bar(df_escola["nome"], df_escola["frequencia"])
plt.show()
```

### Questão 3
```python
plt.scatter(df_escola["frequencia"], df_escola["nota"])
plt.show()
```

### Questão 4
```python
plt.figure(figsize=(6, 4))
plt.scatter(df_escola["frequencia"], df_escola["nota"])
plt.title("Nota x Frequência")
plt.xlabel("Frequência (%)")
plt.ylabel("Nota")
plt.show()
```

### Questão 5
```python
import seaborn as sns

df_cidades = pd.read_csv("datasets/escolhidos_ava_2/EquipeE_cidades.csv")
top_pop = df_cidades.nlargest(10, "ESTIMATED_POP")

sns.barplot(data=top_pop, x="CITY", y="ESTIMATED_POP")
plt.xticks(rotation=45)
plt.show()
```

### Questão 6
```python
sns.histplot(df_cidades["IDHM"], bins=20, kde=True)
plt.show()
```

### Questão 7
```python
sns.scatterplot(data=df_cidades, x="GDP_CAPITA", y="IDHM", alpha=0.6)
plt.show()
```

### Questão 8
```python
idhm_capital = df_cidades.groupby("CAPITAL", as_index=False)["IDHM"].mean()
sns.barplot(data=idhm_capital, x="CAPITAL", y="IDHM")
plt.show()
```
Interpretação esperada: no dataset, as capitais têm `IDHM` médio maior.

### Questão 9
Resposta esperada: gráfico de barras, porque ele compara valores entre categorias de forma mais direta.

### Questão 10
Resposta esperada: significa que, em geral, valores maiores de `GDP_CAPITA` aparecem associados a valores maiores de `IDHM`, mesmo que haja dispersão.

### Questão 11
Sugestões de resposta:
- limitar o número de categorias exibidas, por exemplo usando top 10;
- rotacionar rótulos e aumentar o tamanho da figura;
- separar a análise em mais de um gráfico em vez de concentrar tudo em um só.

### Questão 12
Exemplo de resposta:
- pergunta: "quais cidades concentram maior estrutura hoteleira?";
- gráfico indicado: gráfico de barras com as cidades que têm mais hotéis.

### Questão 13
Exemplo de problema:
"Investigar como desenvolvimento humano, renda e infraestrutura variam entre municípios brasileiros."

### Questão 14
Exemplo de perguntas norteadoras:
1. Capitais têm IDHM médio mais alto?
2. PIB per capita parece se relacionar com IDHM?
3. Quais cidades se destacam em estrutura hoteleira?

### Questão 15
Exemplo de recorte:
```python
colunas = [
    "CITY", "STATE", "CAPITAL", "ESTIMATED_POP",
    "GDP_CAPITA", "IDHM", "HOTELS", "BEDS"
]
```
Justificativa esperada: essas colunas permitem observar população, renda, desenvolvimento humano e estrutura turística, cobrindo bem a análise inicial.
