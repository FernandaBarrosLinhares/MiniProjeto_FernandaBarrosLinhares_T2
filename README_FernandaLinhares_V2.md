# Análise Exploratória de Dados - Base Varejo

Este projeto realiza uma Análise Exploratória de Dados (AED) na base de varejo, com foco na identificação, tratamento e limpeza de inconsistências nos dados.

O objetivo é preparar a base para análises estatísticas e geração de insights confiáveis.

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


## Etapas do projeto

### Limpeza de Dados

Nesta etapa foi realizada a limpeza da base de dados, incluindo:

- Remoção de colunas totalmente vazias (Unnamed)
- Identificação e remoção de registros duplicados
- Tratamento de valores ausentes na coluna PR_CAT
- Padronização de categorias inconsistentes (ex: "#N/D")
- Conversão da coluna DATA para formato datetime

#### Decisões de Tratamento

- Duplicatas completas foram removidas para evitar distorções nas análises.
- Valores ausentes em PR_CAT foram preenchidos com "SEM CATEGORIA".
- Categorias inválidas foram padronizadas para manter consistência dos dados.
- A coluna DATA foi convertida para datetime para permitir análises temporais.

#### Resultado

Após a limpeza, a base de dados ficou consistente e preparada para análises estatísticas e agrupamentos, garantindo maior confiabilidade nos resultados.


### Análise Estatística da Coluna CL_FHL

A coluna CL_FHL representa a quantidade de filhos dos clientes.

- A média foi de aproximadamente 1,15 filhos por cliente.
- A mediana foi igual a 0, indicando que pelo menos metade dos clientes não possui filhos.
- A moda também foi 0, confirmando que a quantidade mais frequente é nenhum filho.
- O valor mínimo encontrado foi 0 e o máximo foi 4 filhos.
- O desvio padrão de 1,42 indica uma dispersão moderada dos dados em relação à média.
- Os quartis mostram que:
  - 25% dos clientes possuem até 0 filhos;
  - 50% dos clientes possuem até 0 filhos;
  - 75% dos clientes possuem até 2 filhos.

Esses resultados indicam que a maior parte dos clientes possui poucos ou nenhum filho.