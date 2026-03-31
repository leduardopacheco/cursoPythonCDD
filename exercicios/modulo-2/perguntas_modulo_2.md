# Lista de Exercícios

## Módulo 2 - Manipulação de Dados com Pandas

Use, sempre que fizer sentido, os datasets:
- `datasets/escolhidos_ava_2/EquipeA_escola.csv`
- `datasets/escolhidos_ava_2/EquipeE_cidades.csv`

### Parte A - Base com Pandas

1. Carregue o dataset `EquipeA_escola.csv` em um DataFrame e mostre as 5 primeiras linhas.
2. Exiba a quantidade de linhas e colunas do dataset da escola.
3. Mostre os tipos de dados de cada coluna do dataset da escola.
4. Filtre apenas os alunos com nota maior ou igual a 8.
5. Filtre apenas os alunos com frequência maior ou igual a 80.
6. Crie uma coluna chamada `situacao` com a regra: aprovado se `nota >= 7` e `frequencia >= 75`; caso contrário, reprovado.
7. Calcule a média das notas e a média das frequências.
8. Ordene o dataset da escola da maior nota para a menor.

### Parte B - Limpeza e manipulação

9. Verifique se existem valores ausentes no dataset da escola.
10. Renomeie as colunas `nome`, `nota` e `frequencia` para nomes mais descritivos.
11. Usando o dataset das cidades, selecione apenas as colunas `CITY`, `STATE`, `ESTIMATED_POP`, `GDP_CAPITA`, `IDHM`, `HOTELS` e `BEDS`.
12. Mostre as 10 cidades com maior `ESTIMATED_POP`.
13. Mostre as 10 cidades com maior `GDP_CAPITA`.
14. Calcule a média de `IDHM` por estado e ordene do maior para o menor.
15. Filtre apenas as cidades que têm mais de 20 hotéis.

### Parte C - Interpretação

16. No dataset da escola, quantos alunos foram aprovados e quantos foram reprovados?
17. No dataset das cidades, as capitais parecem ter `IDHM` médio maior que as demais cidades? Responda com base em um agrupamento simples.
18. Cite duas vantagens de começar uma análise por um dataset pequeno antes de partir para um dataset grande.
