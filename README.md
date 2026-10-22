# Mini-Projeto de Análise de Dados com Python — Varejo

**Aluno:** Christiano Theiss  
**Turma:** T8  
**Disciplina:** Análise de Dados com Python

## Objetivo

Realizar uma Análise Exploratória de Dados (AED) aplicada ao varejo utilizando Python e pandas, incluindo diagnóstico da qualidade, limpeza, estatísticas descritivas, filtros, agrupamentos e exportação.

## Origem dos dados

Base Varejo disponibilizada no Kaggle:

https://www.kaggle.com/datasets/namespaiva/base-varejo/data

Arquivo original utilizado: `Base Varejo.csv`.

## Estrutura da base

A base original contém 830.000 registros. Após a remoção de quatro colunas completamente vazias, restaram 830.000 registros e 10 colunas úteis.

Principais campos:
- `DATA`: data do registro.
- `CO_ID`: identificador da compra ou operação.
- `CL_ID`: identificador do cliente.
- `CL_GENERO`: gênero registrado.
- `CL_EC`: variável cadastral do cliente.
- `CL_FHL`: variável numérica do cliente.
- `CL_SEG`: segmento do cliente.
- `PR_ID`: identificador do produto.
- `PR_CAT`: categoria do produto.
- `PR_NOME`: nome do produto.

A unidade de análise é o registro da base, que não corresponde necessariamente a um cliente único ou a uma compra única.

## Limpeza e qualidade

O diagnóstico identificou:
- 830.000 registros.
- Nenhum valor ausente nas dez colunas principais.
- Quatro colunas totalmente vazias, removidas durante o tratamento.
- Nenhum texto vazio ou composto apenas por espaços nas colunas textuais verificadas.
- 96.553 linhas duplicadas exatas.
- 3.650 registros com `#N/D` na categoria do produto.

Os textos foram padronizados com remoção de espaços nas extremidades e conversão para maiúsculas nas colunas categóricas selecionadas.

As duplicatas foram mantidas porque não há informação suficiente para distinguir registros repetidos indevidos de itens repetidos em uma compra. Os registros `#N/D` também foram preservados por não haver confirmação de seu significado.

## Resultados

- A categoria `ALIMENTOS` possui 434.767 registros, aproximadamente 52,4% do total.
- A categoria `HIGIENE` possui 155.574 registros.
- A categoria `LIMPEZA` possui 145.754 registros.
- Os registros associados ao gênero `F` somam 432.576; os associados a `M` somam 397.424.
- A variável `CL_FHL` possui 830.000 valores válidos, média de aproximadamente 1,1465, mínimo 0 e máximo 4.

## Recomendação e limitação

Recomenda-se investigar a predominância da categoria `ALIMENTOS` e confirmar o significado das variáveis cadastrais e dos registros `#N/D`.

A base não apresenta valores de venda ou quantidades explícitas. Portanto, não é possível calcular faturamento nem concluir que a contagem de registros representa clientes ou compras únicas.

## Como executar

1. Baixe o notebook `Miniprojeto_Christiano_Theiss_T8.ipynb`.
2. Abra-o no Google Colab.
3. Envie o arquivo original `Base Varejo.csv`.
4. Execute as células na ordem para reproduzir o diagnóstico, a limpeza e as análises.
5. O notebook gera `varejo_limpo.csv` sem índice.

O arquivo `varejo_limpo.csv.gz` disponível neste repositório é uma cópia compactada da base tratada.

## Arquivos

- `Miniprojeto_Christiano_Theiss_T8.ipynb`: notebook de análise.
- `varejo_limpo.csv.gz`: base tratada compactada.
- `README.md`: documentação do projeto.
