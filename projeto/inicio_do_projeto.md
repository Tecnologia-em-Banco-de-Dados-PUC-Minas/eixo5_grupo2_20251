# Etapa 01: Definicao do Problema

## 1 Introdução 

No cenário altamente competitivo do e-commerce, a satisfação do cliente é um fator decisivo para o sucesso de qualquer negócio. As avaliações e comentários dos consumidores constituem uma fonte essencial de informações sobre produtos e serviços, oferecendo feedback direto sobre a experiência de compra. No entanto, muitas empresas enfrentam dificuldades para processar e analisar esse grande volume de dados, o que compromete a extração de insights valiosos para a otimização de vendas e aprimoramento da experiência do usuário. 

Para superar esse desafio, é fundamental adotar soluções tecnológicas que permitam a análise eficiente desses dados. O uso de Machine Learning e Processamento de Linguagem Natural (NLP) possibilita a classificação automática dos comentários dos clientes, permitindo a identificação de padrões e tendências de satisfação. Dessa forma, as empresas podem tomar decisões estratégicas baseadas em dados concretos, fortalecendo sua reputação e impulsionando suas vendas. 

## 2 Problema 

As avaliações e comentários dos clientes no e-commerce são fontes valiosas de informações sobre a percepção dos produtos. No entanto, muitas empresas não utilizam esses dados de maneira estratégica devido a diversos desafios: 

O grande volume de comentários torna inviável a análise manual. 

A ausência de um sistema automatizado dificulta a rápida identificação de feedbacks negativos. 

A interpretação inadequada das avaliações pode levar à perda de oportunidades de melhoria em produtos e serviços. 

A falta de uma análise estruturada pode impactar negativamente as vendas, a reputação da marca e a fidelização dos clientes. 

Assim, o problema central reside na dificuldade de processar e utilizar os comentários dos clientes para aprimorar a experiência de compra e impulsionar os resultados do negócio. 

## 3 Contexto 

Para enfrentar esse desafio, utilizaremos um conjunto de dados fictícios fornecido pelo Kaggle, que contém uma ampla variedade de comentários e avaliações de produtos de diferentes e-commerces. Esse banco de dados nos permitirá realizar testes, treinar modelos de Machine Learning e validar os resultados de maneira eficiente e realista, garantindo a confiabilidade das análises e a aplicabilidade do sistema desenvolvido. 

## 4 Objetivos 

### 4.1 Objetivo Geral 

Desenvolver um sistema baseado em Machine Learning para classificar automaticamente os comentários dos clientes como positivos, negativos ou neutros, gerando insights estratégicos para otimizar as vendas e aprimorar a experiência do usuário. 

### 4.2 Objetivos Específicos  

- Simular Ambiente de Dados: 
Simular o ambiente de coleta e armazenamento de dados de e-commerces brasileiros com base em dataset disponibilizado no Kaggle. 

- Limpeza e Pré-processamento: 
Tratar textos, remover stopwords, aplicar regras de negócio e padronizações para garantir qualidade dos dados. 

- Controle de Versão: 
Usar GitHub para versionamento e colaboração no código. 

- Dashboard Interativo: 
Desenvolver um painel para visualizar insights como avaliações negativas e positivas, principais reclamações e tendências de satisfação ao longo do tempo. 

- Modelagem de ML e NLP: 
Treinar modelos para análise de sentimentos em comentários, classificando-os como positivos, negativos ou neutros. 

- Monitoramento Contínuo: 
Acompanhar desempenho dos modelos e ajustá-los conforme novos dados são coletados. 

 
## 7 PRÉ-PROCESSAMENTO DE DADOS

### 7.1 Objetivos da etapa

A Etapa 3 tem como objetivo descrever as ferramentas utilizadas no processo de pré-processamento e justificar as escolhas com base nas necessidades do projeto e nas características de cada uma.

### 7.2.Ferramentas Utilizadas:

-	Python:
A linguagem de programação principal escolhida devido ao seu vasto ecossistema de bibliotecas para análise de dados e Machine Learning. Python é altamente eficiente para manipulação e processamento de grandes volumes de dados, sendo amplamente utilizada na área de Data Science.

-	Pandas:
Biblioteca essencial para manipulação de dados tabulares (DataFrames). Pandas facilita a leituras, manipulação e limpeza de dados, além de ser altamente otimizada para grandes datasets, o que foi crucial para lidar com os dados de e-commerce.

- UniCodeData:
Utilizada para a normalização e remoção de acentos e caracteres especiais dos dados. Isso garante que o texto esteja padronizado e sem variações de caracteres que possam interferir na análise.

-	Google Colab:
Ambiente de desenvolvimento utilizado para execução dos scripts e upload/download de arquivos. O Google Colab facilita a execução de código na nuvem e é uma plataforma gratuita, ideal para projetos de análise de dados que envolvem grandes volumes de informações.

### 7.3.Justificativa das Escolhas:

-	Python foi escolhido devido à sua versatilidade e poder para realizar operações de análise de dados e Machine Learning. A linguagem é amplamente suportada pela comunidade e possui uma rica coleção de bibliotecas como Pandas e NumPy.
  
-	Pandas foi escolhida por ser a melhor ferramenta para manipulação de dados tabulares, oferecendo funcionalidades robustas para a limpeza, transformação e análise de dados em ormato CSV, como no caso do dataset utilizado.
  
-	UniCodeData foi crucial para garantir que todos os dados textuais fossem normalizados e limpos, eliminando problemas relacionados a acentuação e caracteres especiais, que poderiam interferir em análises posteriores.
  
-	Google Colab foi uma escolha estratégica, pois oferece um ambiente de execução gratuito e fácil de usar, com a possibilidade de trabalhar diretamente com arquivos CSV grandes, além de ser uma plataforma acessível para quem não dispõe de infraestrutura própria de servidores.
  
### 8 Colunas Excluídas:

Durante o processo de pré-processamento, algumas colunas do dataset foram consideradas desnecessárias para a análise de sentimentos e, portanto, removidas. Essas colunas não traziam informações relevantes para a tarefa em questão, como a análise da polaridade dos comentários dos clientes, e sua exclusão ajudou a simplificar o conjunto de dados, tornando-o mais focado nas variáveis essenciais.
A exclusão de colunas desnecessárias é uma prática comum em projetos de data science, pois permite otimizar o processamento, reduzir a complexidade e melhorar a performance dos modelos de análise. No caso deste projeto, foram removidas as seguintes colunas:

-	ORDER_ITEMS:
	ORDER_ITEMS_ID: Identificador único do item do pedido, que não contribui diretamente para a análise de sentimentos.
 shipping_limit_date: Data limite de envio, que não é relevante para a análise de opinião dos consumidores sobre os produtos.
	ORDER_PAYMENTS:
	payment_sequential: Sequência do pagamento, uma variável relacionada ao método de pagamento, mas não essencial para identificar sentimentos expressos nos
 comentários.

-	OLIST_PRODUCTS:
	product_name_length: Comprimento do nome do produto, que não impacta diretamente a análise do sentimento do cliente em relação ao produto.
	product_description_length: Comprimento da descrição do produto, que também não é relevante para avaliar a percepção do cliente.
	product_photos_qty: Quantidade de fotos do produto, que não afeta a opinião expressa nos comentários.
	product_weight_g: Peso do produto, uma característica do produto, mas não essencial para determinar o sentimento dos clientes.
	product_length_cm: Comprimento do produto, outra característica física sem relação direta com a análise de sentimentos.
	product_height_cm: Altura do produto, igualmente não necessária para entender o feedback do cliente.
	product_width_cm: Largura do produto, outra variável física que não influencia a análise dos sentimentos dos consumidores.

- OLIST_SELLERS:
	seller_zip_code_prefix: Prefixo do código postal do vendedor, não relacionado ao sentimento do cliente, sendo irrelevante para a análise proposta.
	ORDER_REVIEW:
 review_answer_timestamp: O timestamp de resposta da avaliação não é relevante para a análise de sentimentos do conteúdo textual dos comentários.
 Essas exclusoes permitiram focar apenas nas informações que são diretamente relacionadas à análise de sentimentos e ajudaram a criar um dataset mais enxuto 
 e eficiente para os próximos passos do projeto.





 

 
