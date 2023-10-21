## Fase 5: Análise

Nesta etapa, dividi a análise em duas partes: Qualidade de Dados e Solução do Problema.

### a. Qualidade de Dados

Na avaliação da qualidade de dados, examinei minuciosamente cada atributo do conjunto de dados. A boa notícia é que, devido à fonte confiável do Kaggle, não encontrei problemas significativos nos dados. Essa base de dados é conhecida por sua curadoria e tratamento meticuloso, o que se refletiu em atributos bem estruturados e ausência de preocupações críticas, como valores ausentes ou erros de entrada.

A qualidade dos dados desempenhou um papel fundamental, garantindo que os dados fossem confiáveis e bem organizados, o que economizou tempo valioso durante a análise.

[Print da Tela do BigQuery](https://storage.googleapis.com/ecommerce-behavior/bigquery.png).


### b. Solução do Problema

Agora é o momento de abordar a solução do problema em questão, conforme definido preliminarmente nos objetivos. Busquei respostas para as perguntas elencadas e realizei análises técnicas dos dados para obtê-las. Cada resposta obtida foi discutida em detalhes, conectando os números aos objetivos do problema a ser solucionado.

No final, uma discussão geral da solução do problema foi apresentada, considerando as análises de cada resposta. Para a realização dessa etapa, utilizei bibliotecas Python vistas na disciplina de Análise Exploratória e Pré-Processamento de Dados, bem como as ferramentas aprendidas na disciplina de Visualização de Informação. Caso ainda não tenha cursado essas disciplinas, é possível responder às perguntas do objetivo somente através da linguagem SQL, objeto da disciplina de Banco de Dados, ou através da linguagem de consulta do banco NoSQL escolhido, objeto da disciplina de Data Warehouse.

Esta abordagem abrangente permitiu uma análise sólida e a obtenção de respostas relevantes para a solução do problema.

## Perguntas-Chave

#### 1. Produtos mais populares

```python
# Criando a tabela de produtos
products = raw_events_data[['product_id','category_id','category_code','brand','price']].drop_duplicates()
products.set_index('product_id', inplace=True)
```

#### 2. Taxa de conversão média

```python
# Criando a tabela de sessões do usuário
user_sessions = raw_events_data[['user_session','user_id']].drop_duplicates()
user_sessions.set_index('user_session', inplace=True)
```

#### 3. Horários de pico

```python
# Criando a tabela de eventos
events = raw_events_data[['event_time','event_type','product_id','user_session']]
```

[Acesse o notebook criado para o projeto](fase-5/notebook) 

*Outras perguntas que estava no objetivo foram comprometidas e ficarão para uma atualização*

##  Tecnologias e Ferramentas Utilizadas

- Google BigQuery para armazenamento e consulta de dados
- Python para análise de dados (Pandas, Matplotlib, Seaborn)
- Jupyter Notebook como ambiente de desenvolvimento
- Google Data Studio para visualização e relatórios de dados [acesse](https://lookerstudio.google.com/reporting/45287913-9e0b-420f-a478-fa2b0740df6f)

## Qualidade dos Dados

A qualidade dos dados desempenhou um papel fundamental nesta análise. Foi possível obter dados de alta qualidade, em grande parte devido à fonte da base de dados. A base de dados utilizada foi obtida do [Kaggle](https://www.kaggle.com/), uma plataforma amplamente reconhecida por suas bases de dados confiáveis e bem documentadas. Isso ajudou a garantir que os dados fossem confiáveis e estruturados de maneira consistente.

A fonte de dados do Kaggle também contribuiu para simplificar o processo de tratamento dos dados. Os dados estavam bem organizados e não havia preocupações significativas com valores ausentes ou erros de entrada. Isso economizou tempo valioso e permitiu que a análise se concentrasse mais na extração de insights significativos.

## Considerações Importantes

- **Segurança dos Dados:** Os dados não possuem informações sensíveis ou que sejam regulamentadas pela LGPD (Lei Geral de Proteção de Dados). Portanto, não é necessário tratamento especial em relação à privacidade.

- **Escalabilidade:** O modelo de dados é projetado para ser escalável, permitindo a adição de novos dados à medida que eles estiverem disponíveis.

- **Colaboração:** Este projeto faz parte de uma disciplina do curso de Cientista de Dados da PUC-RIO e é de autoria exclusiva do seu criador. Após avaliação, está autorizado o ```git clone``` , desde que os créditos de sua criação sejam mantidos e respeitados.

