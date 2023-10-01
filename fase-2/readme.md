# Fase 2: Modelagem de Dados com BigQuery

Nesta fase do projeto, estarei detalhando como realizaremos a modelagem de dados usando o Google BigQuery. A modelagem de dados desempenha um papel fundamental na transformação dos dados brutos em informações valiosas e prontas para análise.

## Objetivo
O objetivo principal desta fase é criar um modelo de dados eficiente e bem estruturado no BigQuery, que nos permitirá realizar análises significativas dos dados de comportamento do consumidor em compras online.

## Passos a Seguir

### 1. Análise do Conjunto de Dados
Antes de iniciar a modelagem, farei uma análise detalhada do conjunto de dados disponível. Isso incluirá a compreensão das tabelas, colunas, tipos de dados e relações entre as tabelas, se aplicável.



### 2. Criação de Tabelas no BigQuery
Com base na análise do conjunto de dados, criarei as tabelas necessárias no Google BigQuery. Isso envolverá a definição de esquemas adequados, tipos de dados e chaves primárias, se aplicável.
![BigQuery com Storage](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/02.png)


### 3. Limpeza e Transformação de Dados
Realizarei a limpeza e transformação de dados conforme necessário. Isso pode incluir a remoção de duplicatas, tratamento de valores ausentes e a aplicação de transformações específicas para melhorar a qualidade dos dados.

```sql
-- Remover duplicatas e preencher valores ausentes na coluna event_time
SELECT DISTINCT event_time AS event_time_timestamp FROM dadosecommerce.Out;

-- Preencher valores ausentes na coluna category_code com um valor padrão
SELECT IFNULL(category_code, 'Valor_Padrao') AS category_code_string FROM dadosecommerce.Out;

-- Padronizar a coluna brand para maiúsculas
SELECT UPPER(brand) AS brand_string FROM dadosecommerce.Out;

-- Remover caracteres indesejados da coluna user_session
SELECT REGEXP_REPLACE(user_session, '[^a-zA-Z0-9]', '') AS user_session_string FROM dadosecommerce.Out;

-- Converter a coluna price em um tipo de dados FLOAT64
SELECT CAST(price AS FLOAT64) AS price_float FROM dadosecommerce.Out;

-- Criar uma nova coluna calculada com base nas colunas category_id e product_id
SELECT category_id, product_id, category_id * product_id AS nova_coluna FROM dadosecommerce.Out;```

![tabela tratada](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/tratadas.png) 

## Considerações Importantes

- **Segurança dos Dados:** Os dados não possuem informações sensíveis ou que sejam regulamentadas pela LGPD (Lei Geral de Proteção de Dados). Portanto, não é necessário tratamento especial em relação à privacidade.

- **Escalabilidade:** O modelo de dados é projetado para ser escalável, permitindo a adição de novos dados à medida que eles estiverem disponíveis.

- **Colaboração:** Este projeto faz parte de uma disciplina do curso de Cientista de Dados da PUC-RIO e é de autoria exclusiva do seu criador. Após avaliação, está autorizado o ```git clone``` , desde que os créditos de sua criação sejam mantidos e respeitados.

Esta fase de modelagem de dados é crucial para o sucesso do projeto, pois define a base para análises futuras. Estou empolgado para continuar avançando e transformar nossos dados brutos em insights valiosos!

