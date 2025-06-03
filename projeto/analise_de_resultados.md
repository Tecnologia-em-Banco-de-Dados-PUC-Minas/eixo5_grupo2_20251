## 11 ANÁLISE DE RESULTADOS

Os resultados apresentados no relatório de classificação evidenciam um desempenho variado do modelo conforme as classes analisadas. 
A classe **positivo** obteve os melhores indicadores, com alta precisão (0.94), recall (0.89) e F1-score (0.92), demonstrando que o modelo identifica com eficácia os comentários positivos. Esse resultado era esperado, uma vez que essa classe era a mais representativa no conjunto de dados (1371 amostras).

A classe **negativo** apresentou resultados razoáveis, com precisão e recall em torno de 0.78, indicando um equilíbrio entre acertos e erros (falsos positivos e falsos negativos).

Por outro lado, a classe **neutro** apresentou desempenho significativamente inferior, com F1-score de apenas 0.27, sugerindo dificuldade do modelo em distinguir essa categoria. A baixa precisão (0.22) e recall (0.33) mostram que muitos neutros foram classificados erroneamente como positivos ou negativos, esse comportamento é comum em cenários com desbalanceamento de classes.

A acurácia geral foi de 82,67%, um valor elevado, mas que pode ser enganoso, pois oculta o fraco desempenho em relação à classe minoritária (neutro). A matriz de confusão confirma essa tendência: enquanto a classe positivo teve apenas 147 erros (entre negativos e neutros), a classe neutro foi frequentemente confundida com as demais (53 classificados como negativo e 46 como positivo).

## 12 Conclusão

Foi desenvolvido um modelo capaz de analisar textos e classificar os sentimentos expressos como positivo, neutro ou negativo. Diante da predominância de comentários positivos no conjunto de dados, foram aplicadas técnicas de balanceamento para evitar que essa desproporção comprometesse a identificação das demais classes.

Observou-se que o modelo acabou usando indiretamente as notas de avaliação (review_score) para ajudar, especialmente nos casos neutros - provavelmente porque notas médias (como 3 de 5) geralmente correspondiam a esse tipo de comentário.

Na sequência, foi testado o BERTimbau (um modelo avançado de análise de texto em português),. No entanto, ele não melhorou muito os resultados em comparação com o método mais simples, principalmente para identificar comentários neutros.

De forma geral, o modelo funcionou bem para classificar positivos e negativos, que eram o principal foco da análise. Como próximos passos, foram identificadas oportunidades de aprimoramento, como:
- Adoção de técnicas específicas para tratar a baixa representatividade da classe neutra
- Inclusão de novas variáveis que contribuam para a identificação mais precisa de comentários neutros

Testes manuais reforçaram a qualidade do modelo,  que conseguiu interpretar adequadamente frases mais complexas — como “A entrega atrasou, mas o produto é bom” —, evidenciando sua efetividade em cenários práticos.