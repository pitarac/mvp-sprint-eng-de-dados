**Passos que vou seguir:**

1. **Identificação da Fonte de Dados:** Começo identificando a fonte de dados principal para o meu projeto. Optei por utilizar um dataset disponível no Kaggle com o seguinte tema: ["eCommerce behavior data from multi-category store"](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store). Este dataset é uma fonte rica de informações sobre o comportamento de compras online em uma loja com várias categorias de produtos.

2. **Configuração de Conexões:** Para acessar esse dataset, criei um bucket no google clound storage conforme imagem abaixo. 

2.1 **Criação do Google Clound Storage:**
![Imagem print screen de uma tela do google na criação do projeto]([imagens/google storage.png]([https://github.com/pitarac/mvp-sprint-eng-de-dados/blob/main/imagens/google%20storage.png](https://storage.cloud.google.com/ecommerce-behavior/google%20storage.png)))



3. **Utilização do Google Cloud Storage:** Para armazenar os dados brutos coletados deste dataset, vou usar o Google Cloud Storage. Isso me proporciona um repositório seguro e escalável para os dados iniciais.

4. **Implementação do Google Cloud Dataflow:** Para a coleta eficiente dos dados em tempo real ou batch, vou implementar fluxos de dados usando o Google Cloud Dataflow. Isso garante que os dados sejam capturados de forma contínua e confiável.

5. **Agendamento de Tarefas:** Em muitos casos, configurarei agendamentos para automatizar a coleta de dados, garantindo que as informações estejam sempre atualizadas.

6. **Monitoramento de Integridade:** Implementarei mecanismos de monitoramento para garantir a integridade dos dados coletados deste dataset, incluindo a detecção e o tratamento de erros durante o processo de coleta.

7. **Documentação:** Manterei uma documentação clara de todas as etapas, incluindo detalhes sobre a fonte de dados do Kaggle, conexões, processos de coleta e outros aspectos para referência futura.

Ao concluir esta fase, terei um sistema sólido para buscar e coletar os dados iniciais deste dataset do Kaggle, fornecendo a base necessária para as análises subsequentes em meu projeto de engenharia de dados. Continuarei com a próxima fase, que é a Modelagem de Dados.
