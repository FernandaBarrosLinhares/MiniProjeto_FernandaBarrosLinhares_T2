# Análise Exploratória de Dados - Base Varejo

Este projeto realiza uma Análise Exploratória de Dados (AED) na base de varejo, com foco na identificação, tratamento e limpeza de inconsistências nos dados.

O objetivo é preparar a base para análises estatísticas e geração de insights confiáveis.

## Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Jupyter Notebook / VS Code

## Como executar o projeto

1. Clone o repositório:

```bash
git clone https://github.com/FernandaBarrosLinhares/MiniProjeto_FernandaBarrosLinhares_V2
```

2. Acesse a pasta do projeto:

```bash
cd Miniprojeto_FernandaBarrosLinhares_V2
```

3. Instale as dependências:

```bash
pip install -r requirements.txt
```

4. Execute o notebook no VS Code ou Google Colab.

5. Certifique-se de que o arquivo `Base Varejo.csv` esteja dentro da pasta `data`.

## Etapas do Projeto

### Limpeza de Dados

Nesta etapa foi realizada a limpeza da base de dados, incluindo:

* Remoção de colunas totalmente vazias (Unnamed);
* Identificação e remoção de registros duplicados;
* Tratamento de valores ausentes na coluna PR_CAT;
* Padronização de categorias inconsistentes (ex.: "#N/D");
* Conversão da coluna DATA para formato datetime.

#### Decisões de Tratamento

* Duplicatas completas foram removidas para evitar distorções nas análises.
* Valores ausentes em PR_CAT foram preenchidos com "SEM CATEGORIA".
* Categorias inválidas foram padronizadas para manter consistência dos dados.
* A coluna DATA foi convertida para datetime para permitir análises temporais.
* A repetição do identificador CO_ID foi mantida, pois uma mesma compra pode conter vários produtos diferentes.

#### Resultado

Após a limpeza, a base de dados ficou consistente e preparada para análises estatísticas e agrupamentos, garantindo maior confiabilidade nos resultados.

### Análise Estatística da Coluna CL_FHL

A coluna CL_FHL representa a quantidade de filhos dos clientes.

* Média: 1,15 filhos por cliente.
* Mediana: 0 filhos.
* Moda: 0 filhos.
* Valor mínimo: 0 filhos.
* Valor máximo: 4 filhos.
* Desvio padrão: 1,42.

#### Quartis

| Quartil | Valor |
| ------- | ----- |
| 25%     | 0     |
| 50%     | 0     |
| 75%     | 2     |

Esses resultados indicam que a maior parte dos clientes possui poucos ou nenhum filho.

### Análise de Agrupamentos

#### Distribuição por Gênero

Foram identificados:

* 382.427 registros do gênero feminino;
* 351.020 registros do gênero masculino.

Observa-se uma leve predominância de clientes do gênero feminino na base analisada.

#### Distribuição por Gênero e Estado Civil

O agrupamento entre gênero e estado civil mostrou diferenças na distribuição dos clientes.

Entre as mulheres, os estados civis identificados pelos códigos 3 e 4 apresentaram as maiores quantidades de registros.

Entre os homens, o código 1 apresentou a maior frequência de registros.

A categoria de estado civil identificada pelo código 5 apresentou a menor quantidade de registros para ambos os gêneros.

#### Distribuição por Categoria de Produto

A categoria ALIMENTOS apresentou o maior número de registros, com 384.197 ocorrências.

Em seguida aparecem:

* HIGIENE: 137.702 registros;
* LIMPEZA: 128.632 registros;
* BEBIDAS: 38.264 registros;
* PET: 28.553 registros.

As categorias ACESSORIOS e SEM CATEGORIA apresentaram menor representatividade na base.

## Principais Resultados

* Base original: 830.000 registros e 14 colunas.
* Base final após limpeza: 733.447 registros.
* Compras únicas identificadas: 18.471.
* Registros duplicados removidos: 96.553.
* Categoria de produto mais frequente: ALIMENTOS.
* Predominância de clientes do gênero feminino.

## Conclusões

* A base original possuía 830.000 registros e 14 colunas, sendo identificadas quatro colunas totalmente vazias.
* Foram encontrados 96.553 registros duplicados, que foram removidos durante a etapa de limpeza.
* Após o tratamento dos dados, a base final ficou composta por 733.447 registros válidos.
* A análise da variável CL_FHL indicou predominância de clientes sem filhos.
* O público feminino apresentou quantidade de registros ligeiramente superior ao público masculino.
* A categoria ALIMENTOS foi a mais representativa da base, destacando-se como principal grupo de produtos analisado.
