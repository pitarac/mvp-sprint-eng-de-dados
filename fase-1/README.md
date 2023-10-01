# Fase 01: Identificação da Fonte de Dados e Configuração de Conexões

Olá Professor Victor! Nesta primeira fase do meu projeto de Engenharia de Dados, vou descrever os passos que estou seguindo para identificar a fonte de dados principal e configurar as conexões necessárias.

## Passos que vou seguir:

1. **Identificação da Fonte de Dados:** Começo identificando a fonte de dados principal para o meu projeto. Optei por utilizar um dataset disponível no Kaggle com o seguinte tema: ["eCommerce behavior data from multi-category store"](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store). Este dataset é uma fonte rica de informações sobre o comportamento de compras online em uma loja com várias categorias de produtos.

2. **Configuração de Conexões:** Para armazenar os dados brutos coletados deste dataset, vou usar o Google Cloud Storage. Isso me proporciona um repositório seguro e escalável para os dados iniciais.

   - **Utilização do Google Cloud Storage:** [Link para a documentação do Google Cloud Storage](https://cloud.google.com/storage)

   ![Imagem print screen de uma tela do Google na criação do projeto](https://storage.googleapis.com/ecommerce-behavior/google%20storage.png)

3. **Criação do Bucket:** Durante a configuração do Google Cloud Storage, criei um bucket para armazenar os dados brutos. Este bucket será o local onde os dados coletados serão armazenados de forma organizada e segura.

   ![Imagem print screen de uma tela do Google na criação do projeto](https://storage.googleapis.com/ecommerce-behavior/Imangens%20/bucket%20-1.png)

## Considerações Importantes

- **Segurança dos Dados:** Os dados não possuem informações sensíveis ou que sejam regulamentadas pela LGPD (Lei Geral de Proteção de Dados). Portanto, não é necessário tratamento especial em relação à privacidade.

- **Escalabilidade:** O modelo de dados é projetado para ser escalável, permitindo a adição de novos dados à medida que eles estiverem disponíveis.

- **Colaboração:** Este projeto faz parte de uma disciplina do curso de Cientista de Dados da PUC-RIO e é de autoria exclusiva do seu criador. Após avaliação, está autorizado o ```git clone``` , desde que os créditos de sua criação sejam mantidos e respeitados.
