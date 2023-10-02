# Fase 3: Modelagem de Dados

Nesta fase do projeto, concentramos nossos esforços na modelagem de dados. O objetivo principal é criar uma estrutura sólida que nos permita organizar e compreender os dados de forma eficaz. Esta fase é fundamental para o sucesso das etapas subsequentes de carga e análise de dados.

## Estilo de Modelagem

Para esta fase, optei por usar Modelo Snowflake para a organização dos dados. Esta escolha foi feita com base nas necessidades específicas do projeto e na facilidade de consulta.

## Catálogo de Dados

O Catálogo de Dados é uma parte crítica da nossa modelagem. Ele fornece informações detalhadas sobre os conjuntos de dados que estamos trabalhando. Abaixo estão os principais componentes do nosso Catálogo de Dados:

![catalago](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/fase03-01.png)

### Descrição Detalhada dos Dados

- Descrevemos minuciosamente cada conjunto de dados, explicando o significado e a relevância de cada um no contexto do projeto.

| Nome da Coluna  | Tipo de Dado | Descrição                                                                                   |
|-----------------|--------------|---------------------------------------------------------------------------------------------|
| event_time      | TIMESTAMP    | Armazena o horário em que o evento ocorreu. Isso permite rastrear quando os eventos aconteceram. |
| event_type      | STRING       | Contém diferentes tipos de eventos, como "visualização", "compra", "clicou", etc. Essa coluna ajuda a categorizar os eventos. |
| product_id      | INTEGER      | Armazena o ID do produto associado ao evento, facilitando a análise de comportamento do produto. |
| category_id     | INTEGER      | Contém o ID da categoria à qual o produto pertence. Isso ajuda a agrupar produtos por categoria. |
| category_code   | STRING       | Contém códigos de categoria. Pode ser útil para categorização rápida. |
| brand           | STRING       | Armazena a marca do produto como uma STRING. Isso permite analisar o comportamento das marcas. |
| price           | FLOAT        | Armazena o preço do produto associado ao evento. |
| user_id         | INTEGER      | Contém o ID do usuário que realizou o evento. Isso ajuda a rastrear o comportamento do usuário. |
| user_session    | STRING       | Armazena o ID da sessão do usuário. Isso é útil para rastrear a atividade de um usuário durante uma sessão. |


### Domínios dos Dados

- Para manter a integridade dos dados, fornecemos valores mínimos e máximos esperados para dados numéricos, bem como categorias para dados categóricos. Isso ajuda a definir limites claros para os dados.

| Nome da Coluna  | Tipo de Dado | Domínio                                      | Descrição                                                                                   |
|-----------------|--------------|----------------------------------------------|---------------------------------------------------------------------------------------------|
| event_time      | TIMESTAMP    | Data e hora em formato TIMESTAMP             | Armazena o horário em que o evento ocorreu. Isso permite rastrear quando os eventos aconteceram. |
| event_type      | STRING       | Diferentes tipos de eventos                  | Contém diferentes tipos de eventos, como "visualização", "compra", "clicou", etc. Essa coluna ajuda a categorizar os eventos. |
| product_id      | INTEGER      | Números inteiros positivos                   | Armazena o ID do produto associado ao evento, facilitando a análise de comportamento do produto. |
| category_id     | INTEGER      | Números inteiros positivos                   | Contém o ID da categoria à qual o produto pertence. Isso ajuda a agrupar produtos por categoria. |
| category_code   | STRING       | Texto alfanumérico                          | Contém códigos de categoria. Pode ser útil para categorização rápida. |
| brand           | STRING       | Texto alfanumérico                          | Armazena a marca do produto como uma STRING. Isso permite analisar o comportamento das marcas. |
| price           | FLOAT        | Números de ponto flutuante positivos ou zero | Armazena o preço do produto associado ao evento. |
| user_id         | INTEGER      | Números inteiros positivos                   | Contém o ID do usuário que realizou o evento. Isso ajuda a rastrear o comportamento do usuário. |
| user_session    | STRING       | Texto alfanumérico                          | Armazena o ID da sessão do usuário. Isso é útil para rastrear a atividade de um usuário durante uma sessão. |


### Linhagem dos Dados

Os dados foram inicialmente obtidos da plataforma Kaggle e, em seguida, passaram por transformações no Google BigQuery.


## Próximas Etapas

Após a conclusão desta fase, seguiremos para as próximas etapas do projeto:

- **Fase 4: Carga de Dados**: Nesta etapa, realizaremos a carga dos dados modelados em um Data Warehouse/Data Lake usando o Google Cloud Dataflow. Os dados serão armazenados e consultados no Google BigQuery.

- **Fase 5: Análise de Dados**: Aqui, realizaremos análises de qualidade dos dados e resolveremos o problema inicialmente definido. Usaremos o Google Data Studio para criar painéis de visualização e consultaremos dados complexos no Google BigQuery.


