# Curso Introdutório de Python para Ciência de Dados

Repositório oficial do **Curso Introdutório de Python para Ciência de Dados**, desenvolvido como Atividade Extensionista da disciplina **T326 - Ciência de Dados | UNIFOR**.

**Instrutores:** Equipe E  
**Professora:** Rilder de Sousa Pires  
**Dataset principal:** Brazilian Cities — 5.578 municípios brasileiros

---

## Como executar

Certifique-se de ter o [Git](https://git-scm.com/) e o [Python 3.8+](https://www.python.org/) instalados.

```bash
git clone https://github.com/SaulSantos1/curso-python-ciencia-dados.git
cd curso-python-ciencia-dados-main

python -m venv venv
source venv/bin/activate        # Linux/macOS
venv\Scripts\activate           # Windows

pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook
```

---

## Estrutura do Repositório

```
curso-python-ciencia-dados-main/
│
├── modulo-1/                        # Módulo 1: Fundamentos de Python
│   ├── notebooks/
│   │   └── aula_01_python_basico.ipynb
│   ├── exercicios/
│   │   └── exercicios_aula_01.ipynb
│   ├── datasets/
│   │   └── dataset_alunos.csv
│   ├── slides/
│   │   ├── Curso_Introdutório_de_Python_para_Ciência_de_Dados.pdf
│   │   └── Fundamentos_de_Python_-_Módulo_1.pdf
│   └── materiais_complementares.txt
│
├── modulo-2/                        # Módulo 2: Manipulação de Dados
│   ├── notebook/
│   │   └── modulo2.ipynb
│   ├── exercicios/
│   │   └── gabarito_exercicios_modulo2.ipynb
│   ├── datasets/
│   │   └── brazilian_city.csv
│   └── slides/
│       └── Desenvolvimento Base.pdf
│
├── modulo-3/                        # Módulo 3: Visualização de Dados
│   ├── notebook/
│   │   └── modulo3.ipynb
│   ├── exercicios/
│   │   └── gabarito_exercicios_modulo3.ipynb
│   ├── datasets/
│   │   └── brazilian_city.csv
│   └── slides/
│       └── Desenvolvimento Base.pdf
│
├── modulo-4/                        # Módulo 4: Análise Exploratória de Dados (EDA)
│   ├── notebook/
│   │   └── modulo4.ipynb
│   └── exercicios/
│       └── gabarito_exercicios_modulo4.ipynb
│
├── projeto-final/                   # Projeto Final: EDA Completa
│   ├── primeira_versao_eda.ipynb    # Versão inicial (definição do problema)
│   └── analise_final_eda.ipynb     # Análise completa com insights
│
└── README.md                        # Este arquivo
```

---

## Ementa do Curso

### Módulo 1 — Fundamentos de Python
- Sintaxe básica, variáveis e tipos de dados
- Estruturas condicionais, repetição e estruturas de dados
- Boas práticas de programação

### Módulo 2 — Manipulação de Dados com Pandas
- Introdução ao Pandas e leitura de dados
- Limpeza, tratamento e transformação de dados
- Estatística descritiva básica

### Módulo 3 — Visualização de Dados e Storytelling
- Fundamentos de visualização
- Gráficos com Matplotlib e Seaborn
- Comunicação visual e boas práticas

### Módulo 4 — Análise Exploratória de Dados (EDA)
- Definição do problema e perguntas norteadoras
- Análise univariada, bivariada e multivariada
- Storytelling com dados e comunicação de insights

### Projeto Final
- Dataset real: Brazilian Cities (5.578 municípios brasileiros)
- Problema: Determinantes do IDHM Municipal
- 6 perguntas norteadoras respondidas com visualizações e insights

---

## Dataset Principal

**Brazilian Cities** — Dados socioeconômicos de todos os 5.578 municípios brasileiros.

| Variável | Descrição |
|----------|-----------|
| `CITY` / `STATE` | Nome da cidade e UF |
| `IDHM` | Índice de Desenvolvimento Humano Municipal |
| `IDHM_Renda`, `IDHM_Longevidade`, `IDHM_Educacao` | Componentes do IDHM |
| `GDP_CAPITA` | PIB per capita (R$) |
| `POP_FINAL` | População (censo ou estimada) |
| `AREA` | Área em km² |
| `CAPITAL` | 1 se é capital estadual, 0 caso contrário |

---

## Pré-requisitos

- Python 3.8+
- Jupyter Notebook ou JupyterLab
- Bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## Como Aproveitar o Curso

1. **Siga a ordem dos módulos** — o conteúdo é progressivo
2. **Tente os exercícios antes do gabarito** — a prática consolida o aprendizado
3. **Explore o dataset por conta própria** — formule suas próprias perguntas
4. **Use os slides para revisão rápida** — ótimos antes de provas ou entrevistas

---

## Links Úteis

- [Documentação do Pandas](https://pandas.pydata.org/docs/)
- [Documentação do Matplotlib](https://matplotlib.org/stable/contents.html)
- [Documentação do Seaborn](https://seaborn.pydata.org/)
- [Jupyter Notebook](https://jupyter.org/)

---

*Desenvolvido com dedicação pela Equipe E — T326 Ciência de Dados | UNIFOR*
