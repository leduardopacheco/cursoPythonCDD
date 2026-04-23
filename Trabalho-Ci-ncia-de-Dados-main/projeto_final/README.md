# Dataset - Atlas do Desenvolvimento Humano (ADH)

O dataset selecionado para este trabalho foi o **Atlas do Desenvolvimento Humano (ADH)**, disponibilizado pela plataforma **Base dos Dados**.

O Atlas do Desenvolvimento Humano reúne indicadores socioeconômicos e demográficos dos municípios brasileiros, permitindo a análise do desenvolvimento humano ao longo do tempo. A base utilizada possui cobertura temporal entre **1991 e 2010**, contemplando diferentes dimensões relacionadas à qualidade de vida da população.

A estrutura do dataset é composta por variáveis organizadas em nível municipal (`id_municipio`) e anual (`ano`), permitindo análises espaciais e temporais. Entre os principais grupos de variáveis disponíveis, destacam-se:

- **Indicadores de desenvolvimento humano**, como o `idhm` (Índice de Desenvolvimento Humano Municipal) e suas dimensões (`idhm_e`, `idhm_r`, `idhm_l`);
- **Indicadores de educação**, como `expectativa_anos_estudo`, taxas de analfabetismo e frequência escolar;
- **Indicadores de renda e desigualdade**, como `renda_pc`, `indice_gini` e proporções de pobreza (`prop_pobreza`, `prop_pobreza_extrema`);
- **Indicadores de saúde e longevidade**, como `expectativa_vida` e taxas de mortalidade infantil;
- **Indicadores de trabalho e atividade econômica**, como `taxa_atividade` e `taxa_desocupacao`;
- **Indicadores de infraestrutura domiciliar**, como acesso à água, energia elétrica e coleta de lixo.

A escolha deste dataset se justifica pela sua abrangência e pela possibilidade de analisar o desenvolvimento humano de forma integrada, considerando múltiplas dimensões (educação, renda e saúde), o que o torna adequado para investigações sobre desigualdades regionais no Brasil.

---

# ❗ Problema formulado

O desenvolvimento humano no Brasil apresenta fortes desigualdades regionais e sociais, refletidas em diferenças significativas nos níveis de renda, educação e qualidade de vida entre municípios.

Embora indicadores como o IDHM forneçam uma visão geral do desenvolvimento, eles agregam múltiplos fatores em um único índice, dificultando a compreensão detalhada dos elementos que mais influenciam essas variações. Além disso, a evolução desses indicadores ao longo do tempo pode revelar padrões importantes sobre o progresso ou estagnação de determinadas regiões.

Nesse contexto, torna-se necessário investigar de forma mais aprofundada como diferentes dimensões do desenvolvimento humano — como educação, renda e condições de vida — se relacionam entre si e influenciam o IDHM dos municípios brasileiros.

Dessa forma, o problema central deste trabalho pode ser definido como:

> **Quais fatores socioeconômicos e educacionais influenciam o nível de desenvolvimento humano dos municípios brasileiros entre 1991 e 2010?**

A análise desse problema permite compreender melhor as desigualdades estruturais do país e identificar variáveis-chave associadas ao desenvolvimento humano.

---

# ❓ Perguntas norteadoras

Para orientar a análise, foram definidas as seguintes perguntas norteadoras:

## 1. Evolução do desenvolvimento humano

- Como o IDHM (`idhm`) evoluiu ao longo do período de 1991 a 2010?
- Houve melhora significativa nos indicadores de desenvolvimento humano nos municípios brasileiros?

## 2. Educação e desenvolvimento

- Qual a relação entre educação (ex.: `expectativa_anos_estudo`, taxas de analfabetismo) e o IDHM?
- Municípios com melhores indicadores educacionais apresentam maiores níveis de desenvolvimento humano?

## 3. Renda e desigualdade

- Como a renda per capita (`renda_pc`) influencia o IDHM?
- Existe relação entre desigualdade (`indice_gini`) e níveis de desenvolvimento humano?

## 4. Condições de vida e infraestrutura

- O acesso a serviços básicos (água, energia, saneamento) impacta o desenvolvimento humano?
- Municípios com melhor infraestrutura apresentam maiores valores de IDHM?

## 5. Desigualdades regionais

- Existem diferenças significativas de desenvolvimento humano entre municípios brasileiros?
- Quais regiões apresentam maiores níveis de desigualdade socioeconômica?

## 6. Saúde e longevidade

- Como indicadores de saúde, como `expectativa_vida` e mortalidade infantil, se relacionam com o IDHM?
- Municípios com maior longevidade apresentam maior desenvolvimento humano?

---

# 📂 Estrutura dos Dados

Para a realização deste trabalho, foram utilizados **dois datasets**, que em conjunto permitem a análise adequada dos dados do Atlas do Desenvolvimento Humano.

## 1. Dataset principal — Indicadores do ADH

Arquivo: `indices_adh_municipio.csv`

Este dataset contém os **indicadores socioeconômicos e de desenvolvimento humano** em nível municipal, incluindo variáveis como:

- IDHM (`idhm`) e suas dimensões (`idhm_e`, `idhm_r`, `idhm_l`)
- Renda per capita (`renda_pc`)
- Índice de desigualdade (`indice_gini`)
- Indicadores de educação (ex.: `expectativa_anos_estudo`, taxas de analfabetismo)
- Indicadores de saúde (ex.: `expectativa_vida`, mortalidade infantil)

A identificação dos municípios neste dataset é feita exclusivamente por meio da coluna:

- `id_municipio` (código do IBGE)

## 2. Dataset auxiliar — Identificação dos municípios

Arquivo: `identificador_municipios.csv`

Este dataset contém informações descritivas dos municípios, permitindo a interpretação dos dados do dataset principal. Entre as principais informações, destacam-se:

- Nome do município
- Estado (UF)
- Região

Esse dataset é utilizado para complementar o dataset principal, já que este contém apenas o identificador numérico dos municípios.

## 🔗 Integração entre os datasets

A análise completa requer a **junção (merge)** dos dois datasets, utilizando a coluna comum:

- `id_municipio`

Essa integração permite:

- Associar os indicadores socioeconômicos aos nomes dos municípios
- Realizar análises por estado e região
- Melhorar a interpretabilidade dos resultados

## Créditos

Este dataset foi compilado e disponibilizado por:

- **Atlas Brasil**
  - Dataset: Atlas do Desenvolvimento Humano (ADH)
  - Kaggle: https://basedosdados.org/dataset/cbfc7253-089b-44e2-8825-755e1419efc8?table=ec5fb3d1-fa98-4ab3-8a02-4b9950048a83

---
