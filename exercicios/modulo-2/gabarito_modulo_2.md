# Gabarito

## Módulo 2 - Manipulação de Dados com Pandas

### Questão 1
```python
import pandas as pd

df_escola = pd.read_csv("datasets/escolhidos_ava_2/EquipeA_escola.csv")
df_escola.head()
```

### Questão 2
```python
df_escola.shape
```
Resposta esperada: `(10, 3)`.

### Questão 3
```python
df_escola.dtypes
```

### Questão 4
```python
df_escola[df_escola["nota"] >= 8]
```

### Questão 5
```python
df_escola[df_escola["frequencia"] >= 80]
```

### Questão 6
```python
df_escola["situacao"] = df_escola.apply(
    lambda linha: "Aprovado" if linha["nota"] >= 7 and linha["frequencia"] >= 75 else "Reprovado",
    axis=1
)
```

### Questão 7
```python
df_escola["nota"].mean()
df_escola["frequencia"].mean()
```
Respostas esperadas:
- média das notas: `7.6`
- média das frequências: `80.8`

### Questão 8
```python
df_escola.sort_values("nota", ascending=False)
```

### Questão 9
```python
df_escola.isna().sum()
```
Resposta esperada: não há valores ausentes nas três colunas.

### Questão 10
```python
df_escola.rename(columns={
    "nome": "aluno",
    "nota": "nota_final",
    "frequencia": "frequencia_percentual"
})
```

### Questão 11
```python
df_cidades = pd.read_csv("datasets/escolhidos_ava_2/EquipeE_cidades.csv")
recorte = df_cidades[["CITY", "STATE", "ESTIMATED_POP", "GDP_CAPITA", "IDHM", "HOTELS", "BEDS"]]
```

### Questão 12
```python
recorte.nlargest(10, "ESTIMATED_POP")[["CITY", "STATE", "ESTIMATED_POP"]]
```
Exemplos esperados no topo: São Paulo, Rio de Janeiro, Brasília, Salvador e Fortaleza.

### Questão 13
```python
recorte.nlargest(10, "GDP_CAPITA")[["CITY", "STATE", "GDP_CAPITA"]]
```
Exemplos esperados no topo: Paulínia, Selvíria, São Francisco do Conde, Triunfo e Brejo Alegre.

### Questão 14
```python
recorte.groupby("STATE")["IDHM"].mean().sort_values(ascending=False)
```
Estados esperados nas primeiras posições: `DF`, `SP`, `SC`, `RS` e `RJ`.

### Questão 15
```python
recorte[recorte["HOTELS"] > 20][["CITY", "STATE", "HOTELS", "BEDS"]]
```

### Questão 16
```python
df_escola["situacao"].value_counts()
```
Resposta esperada:
- `7` aprovados
- `3` reprovados

### Questão 17
```python
df_cidades.groupby("CAPITAL")["IDHM"].mean()
```
Resposta esperada: sim. No dataset, as capitais apresentam média de `IDHM` maior do que as não capitais.

### Questão 18
Sugestão de resposta:
- facilita entender comandos básicos sem se perder em muitas colunas;
- ajuda a testar filtros, agrupamentos e renomeações antes de aplicar o mesmo raciocínio em um conjunto maior.
