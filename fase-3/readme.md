# Fase 3: Carga de Dados

Nesta fase do projeto, nosso foco é a carga de dados nos armazéns de dados do Google Cloud. Garantir que os dados sejam carregados de maneira eficiente e confiável é fundamental para o sucesso das análises subsequentes.

## Objetivo

O objetivo principal desta fase é levar os dados modelados na Fase 2 para os armazéns de dados do Google Cloud, como o BigQuery ou o Cloud SQL. Isso nos permitirá acessar os dados de maneira conveniente e realizar análises em tempo real ou sob demanda.

## Passos a Seguir

Aqui estão os passos que seguiremos nesta fase:

### 1. Seleção de Armazéns de Dados

- Escolheremos os armazéns de dados apropriados no Google Cloud para a carga dos dados modelados.
- Consideraremos fatores como desempenho, escalabilidade e custos.

### 2. Configuração do Processo de Carga

- Configuraremos o processo de carga de dados usando o Google Cloud Dataflow ou serviços similares, dependendo dos requisitos do projeto.
- Definiremos as transformações necessárias durante a carga, se aplicável.

### 3. Execução da Carga

- Iniciaremos o processo de carga de dados, garantindo que ele seja confiável e eficiente.
- Acompanharemos o progresso da carga e resolveremos quaisquer problemas que surjam.

## Código de Exemplo

Aqui está um exemplo de código que representa a configuração básica de um processo de carga de dados usando o Google Cloud Dataflow:

```python
# Configuração do pipeline de carga de dados
pipeline_options = PipelineOptions.from_dictionary({
    'project': 'seu-projeto',
    'runner': 'DataflowRunner',
    'temp_location': 'gs://seu-bucket/temp',
    'staging_location': 'gs://seu-bucket/staging',
})

# Definição do pipeline
pipeline = beam.Pipeline(options=pipeline_options)

# Leitura de dados modelados
data_modelado = (
    pipeline
    | 'Leitura de Dados Modelados' >> beam.io.Read(beam.io.BigQuerySource(query='SELECT * FROM tabela_modelada'))
)

# Configuração das transformações e carga nos armazéns de dados
# ... (insira suas transformações aqui)

# Execução do pipeline
result = pipeline.run()
result.wait_until_finish()
