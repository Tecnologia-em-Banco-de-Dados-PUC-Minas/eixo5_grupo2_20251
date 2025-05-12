

## 10 APRENDIZAGEM DE MAQUINA

### 10.1 Objetivos da etapa

Na Etapa 4, serão realizados diferentes experimentos utilizando mais de um algoritmo de cada abordagem, com o objetivo de obter e comparar distintos resultados. Essa comparação visa identificar a solução mais eficaz para o problema, proporcionando maior compreensão sobre o domínio analisado. Os experimentos realizados, bem como suas análises, deverão ser apresentados e discutidos na documentação do projeto.

### 10.2 Implementação
Para a classificação do sentimento dos comentários, utilizou-se a biblioteca TextBlob, que realiza uma análise de polaridade do texto (variando de -1 a 1). A função criada (analisar_sentimento) categorizou os comentários em:
- Positivo: polaridade > 0.1
- Negativo: polaridade < -0.1
- Neutro: polaridade entre -0.1 e 0.1, ou mensagens ausentes/vazias
Essa abordagem, apesar de simples, oferece resultados rápidos e interpretáveis, adequados para uma primeira análise exploratória.

Essa abordagem, apesar de simples, oferece resultados rápidos e interpretáveis, adequados para uma primeira análise exploratória.

## 10.3 Resultados

Ao aplicar a função nos dados, foi possível classificar automaticamente os sentimentos expressos nos comentários. Uma amostra dos resultados é apresentada abaixo:


## 10.4 Considerações Finais da Etapa
A análise de sentimentos mostrou-se eficaz para identificar padrões de satisfação e insatisfação dos clientes. Comentários negativos, por exemplo, estiveram frequentemente relacionados a atrasos na entrega e produtos com defeito, enquanto os positivos destacavam rapidez na entrega e qualidade do atendimento.
