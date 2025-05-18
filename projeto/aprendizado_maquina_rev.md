

## 10 APRENDIZAGEM DE MAQUINA

### 10.1 Objetivos da etapa

Na Etapa 4, serão realizados diferentes experimentos utilizando mais de um algoritmo de cada abordagem, com o objetivo de obter e comparar distintos resultados. Essa comparação visa identificar a solução mais eficaz para o problema, proporcionando maior compreensão sobre o domínio analisado. Os experimentos realizados, bem como suas análises, deverão ser apresentados e discutidos na documentação do projeto.

### 10.2 Implementação
O script realiza a análise de sentimentos de avaliações de produtos utilizando aprendizado de máquina em Python. Ele carrega dados do GitHub, pré-processa os textos com o spaCy, classifica os sentimentos (positivo, neutro ou negativo) com base nas notas, e utiliza um pipeline com TfidfVectorizer, SMOTE e LinearSVC para treinar o modelo. Após avaliar o desempenho com métricas como matriz de confusão e relatório de classificação, o script aplica o modelo a todos os dados e exporta os resultados com os sentimentos previstos. Por fim, permite testes manuais de classificação e realiza o upload automático do arquivo final para esse repositório na pasta chamada gold mediante autenticação com token pessoal.

Essa abordagem, apesar de simples, oferece resultados rápidos e interpretáveis, adequados para uma primeira análise exploratória.

## 10.3 Resultados
Ao aplicar a função nos dados, foi possível classificar automaticamente os sentimentos expressos nos comentários. Uma amostra dos resultados é apresentada abaixo:

https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo2_20251/issues/1#issue-3064573755

## 10.4 Considerações Finais da Etapa
A análise de sentimentos mostrou-se eficaz para identificar padrões de satisfação e insatisfação dos clientes. Comentários negativos, por exemplo, estiveram frequentemente relacionados a atrasos na entrega e produtos com defeito, enquanto os positivos destacavam rapidez na entrega e qualidade do atendimento.
