# Fase 2: Coleta de Dados

Nesta fase do projeto, concentraremos nossos esforços na coleta de dados essenciais para a análise de comportamento de consumidores em compras online.

## Objetivo
O principal objetivo desta fase é adquirir os dados brutos necessários para a análise, provenientes do conjunto de dados "eCommerce behavior data from multi-category store".

## Passos a Seguir

### 1. Acesso à Fonte de Dados
Para iniciar a coleta de dados, acessaremos a fonte de dados principal, que é o conjunto de dados disponível no Kaggle com o seguinte tema: ["eCommerce behavior data from multi-category store"](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store).

### 2. Extração de Dados
Realizei a extração de dados pela url, criando um job de transferência no Google Storage:
 Print do job 

![Configuraçã do Job](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/job%2001.png)


![Job em Processamento](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/job%2002%20.png)


### 3. Armazenamento de Dados Brutos
Configuramos previamente o Google Cloud Storage na Fase 01 como o local para armazenar os dados brutos coletados. Os dados coletados serão carregados para o nosso bucket no Google Cloud Storage, onde serão organizados e armazenados de forma segura.

### 4. Documentação
Durante o processo de coleta, documentamos todos os detalhes relevantes, incluindo a fonte dos dados, como foram extraídos, quaisquer problemas encontrados durante a coleta e quaisquer transformações preliminares realizadas.

### 5. Monitoramento
Estabelecemos um sistema de monitoramento para garantir que a coleta de dados seja contínua e confiável. Qualquer problema que surgir durante o processo de coleta será identificado e tratado prontamente.

Esta fase de coleta de dados é crucial para o sucesso do projeto, pois garante que tenhamos acesso aos dados necessários para análises futuras. Estou ansioso para continuar e transformar esses dados brutos em informações valiosas!
