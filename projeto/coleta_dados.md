
## 5 Arquitetura do Projeto

O projeto simulará um ambiente de lakehouse utilizando a Arquitetura Medallion, um padrão de design voltado para a organização eficiente dos dados.

![building-data-pipelines-with-delta-lake-120823](https://github.com/user-attachments/assets/3a04443b-44d9-43fc-9103-7c8d894bfe22)
Medallion Archicture disponivel em https://www.databricks.com/glossary/medallion-architecture

Características dessa arquitetura:
- Camada Bronze (dados brutos): Contém os dados extraídos diretamente de sistemas de origem externa, sem transformações. As tabelas dessa camada preservam a estrutura original dos dados.
- Camada Prata (dados limpos e conformados): Aqui os dados da camada Bronze são refinados e tratados para padronização e qualidade.
  - Nessa camada, são organizadas informações estruturadas sobre clientes, lojas, produtos, entre outros.
- Camada Ouro (dados enriquecidos e análises): Aplica regras de negócios e agrega os dados para visualizações e análises.
  - Essa camada é utilizada para geração de relatórios e insights, como análise de clientes, qualidade de produtos e recomendações personalizadas.

## 6 Origem dos Dados 

Os conjuntos de dados utilizados neste projeto estão disponíveis no [Kaggle]([https://www.kaggle.com/](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data?select=product_category_name_translation.csv)), uma plataforma colaborativa voltada para ciência de dados e aprendizado de máquina. 
O Kaggle permite que pesquisadores e profissionais compartilhem datasets, desenvolvam modelos e participem de competições. 


Esse dataset contém dados reais e públicos de comércio eletrônico no Brasil, referentes a pedidos realizados na Olist Store. 
Ele abrange informações de 100 mil pedidos feitos entre 2016 e 2018 em diversos mercados do país.

Para simplificar o projeto, os arquivos foram baixados em formato CSV e posteriormente enviados para o GitHub, na pasta denominada 'Bronze'.

---
## 6.1 Segurança e Proteção de Dados  

Para garantir a confidencialidade, o dataset disponibilizado no Kaggle foi anonimizado, e as referências a empresas e parceiros foram substituídas pelos nomes das grandes casas de Game of Thrones. 
Dessa forma, nenhuma alteração adicional de segurança foi necessária.
