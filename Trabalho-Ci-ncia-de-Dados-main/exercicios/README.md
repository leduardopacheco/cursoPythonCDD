# Curso de Ciência de Dados — Notebooks

## ⚠️ Execução dos Notebooks

Para garantir o correto funcionamento dos notebooks, é **fundamental executar as células em ordem sequencial**.

### 🔹 Por quê?

Os notebooks são estruturados de forma progressiva, ou seja:

- Algumas variáveis são criadas em células anteriores
- Etapas de tratamento de dados acontecem antes das análises
- Gráficos dependem de dados previamente preparados

Se você executar células fora de ordem, pode encontrar erros como:

- `NameError` (variável não definida)
- Dados incompletos ou inconsistentes
- Gráficos incorretos

---

## Execução Local (na sua máquina)

Se você estiver rodando os notebooks localmente (fora do Google Colab), é necessário instalar as dependências do projeto.

---

### 📦 Dependências necessárias

As principais bibliotecas utilizadas são:

- `pandas`
- `matplotlib`
- `seaborn`
- `numpy`

---

### 🔧 Instalação via pip

No terminal, execute:

```bash
pip install pandas matplotlib seaborn numpy
```
