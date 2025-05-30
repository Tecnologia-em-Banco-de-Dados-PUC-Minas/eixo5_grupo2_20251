## 5.0 ANÁLISE DE RESULTADOS

Os resultados apresentados no relatório de classificação revelam um desempenho variado do modelo conforme as classes analisadas. A classe **positivo** obteve os melhores indicadores, com alta precisão (0.94), recall (0.89) e F1-score (0.92), demonstrando que o modelo identifica com eficácia os comentários positivos. Isso era esperado, já que essa classe era a mais representativa no conjunto de dados (1371 amostras).

Já a classe **negativo** apresentou resultados razoáveis, com precisão e recall próximos de 0.78, indicando um equilíbrio entre acertos e falsos positivos/negativos. Por outro lado, a classe **neutro** teve desempenho significativamente inferior, com F1-score de apenas 0.27, sugerindo dificuldade do modelo em distinguir essa categoria. A baixa precisão (0.22) e recall (0.33) mostram que muitos neutros foram classificados erroneamente como positivos ou negativos, o que é comum em problemas com desbalanceamento de classes.

A acurácia geral foi de **82.67%**, um valor alto, mas que mascara a baixa performance na classe minoritária (neutro). A matriz de confusão confirma essa tendência: enquanto a classe positivo teve apenas 147 erros (entre negativos e neutros), a classe neutro foi frequentemente confundida com as demais (53 classificados como negativo e 46 como positivo).

## 5.1 Conclusão

Criamos um modelo que analisa textos para classificar sentimentos (positivo, neutro ou negativo). Para evitar que os comentários positivos (que eram a maioria) prejudicassem a análise dos outros, usamos técnicas para equilibrar os dados.

Notamos que o modelo acabou usando indiretamente as notas de avaliação (review_score) para ajudar, especialmente nos casos neutros - provavelmente porque notas médias (como 3/5) geralmente correspondiam a esse tipo de comentário.

Depois, testamos o BERTimbau (um modelo avançado de análise de texto em português), mas ele não melhorou muito os resultados em comparação com o método mais simples, principalmente para identificar comentários neutros.

No geral, o modelo funcionou bem para classificar positivos e negativos, que eram nosso foco principal. Para melhorar no futuro, podemos tentar:

- Técnicas especiais para lidar melhor com poucos exemplos neutros
- Incluir mais informações para ajudar a identificar neutros

Os testes manuais mostraram que o modelo acerta bem, até em frases complicadas como "A entrega atrasou, mas o produto é bom", mostrando que funciona bem na prática.
