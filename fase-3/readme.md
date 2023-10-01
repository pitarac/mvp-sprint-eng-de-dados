# Fase 3: Carga de Dados no BigQuery

Nesta fase do projeto, nosso foco é a carga de dados diretamente no BigQuery, o armazém de dados do Google Cloud. Garantir que os dados sejam carregados de maneira eficiente e confiável é fundamental para o sucesso das análises subsequentes.

## Objetivo

O objetivo principal desta fase é levar os dados modelados na Fase 2 para o BigQuery, onde eles estarão prontos para análise em tempo real ou sob demanda.

## Passos a Seguir

Aqui estão os passos que seguiremos nesta fase:

### 1. Definir a Tabela de Destino no BigQuery

- Definiremos a tabela de destino no BigQuery onde desejamos carregar os dados.
- Certificaremos de que a tabela de destino esteja devidamente configurada com o esquema correto.

### 2. Carga de Dados no BigQuery

- Usaremos SQL para realizar a carga de dados diretamente no BigQuery.
- Inseriremos os dados modelados na tabela de destino especificada.

### 3. Configuração de Permissões

- Certificaremos de que as permissões adequadas estejam configuradas para inserir dados na tabela de destino no BigQuery.
- Você deve ter as permissões necessárias para executar esta operação com sucesso.

## Código de Exemplo

Aqui está um exemplo de código SQL para realizar a carga de dados no BigQuery:


-- Carga de Dados no BigQuery

-- Defina a tabela de destino no BigQuery onde você deseja carregar os dados
```sql DECLARE target_table STRING; SET target_table = 'seu_projeto.seu_dataset.sua_tabela_destino';
-- Insira os dados modelados na tabela de destino
```sql INSERT INTO `project.dataset.table` SELECT * FROM `project.dataset.modelado`;


 -- Substitua pelos nomes reais dos projetos, datasets e tabelas

-- Lembre-se de configurar corretamente as permissões para inserir dados na tabela de destino
-- Você deve ter as permissões adequadas no BigQuery para executar esta operação
