## 5ª Etapa
### Análise de Resultados

Como o objetivo inicial era prever os valores de 'popularity' do dataset 'df_2023', e este não possui algumas das features utilizadas no treinamento anterior, novos modelos foram treinados mantendo apenas as features comuns aos dois datasets.

![image](../imagens/etapa5/1-features-comuns.png)

Após identificar as features comuns, as demais foram removidas. Em seguida, o dataset foi normalizado, separado da variável target e dividido em conjuntos de treino e teste.

![image](../imagens/etapa5/2-treino-teste.png)

O primeiro modelo foi treinado utilizando o algoritmo de regressão linear.

![image](../imagens/etapa5/3-linear-regression.png)

E o segundo utilizando árvore de decisão.

![image](../imagens/etapa5/4-decision-tree.png)

Para realizar a predição sobre os dados do 'df_2023', o dataset também passou pela remoção das colunas extras e pela normalização.

![image](../imagens/etapa5/5-normalizacao.png)

A ordem das colunas foi alterada, o predict foi realizado

![image](../imagens/etapa5/6-colunas.png)

![image](../imagens/etapa5/7-predict-decision-tree.png)

e os dados previstos foram acrescentado ao dataset

![image](../imagens/etapa5/8-previsoes.png)


Após uma análise extensiva dos dados, em busca de um modelo de aprendizado de máquina adequado ao projeto proposto, concluiu-se que os atributos presentes na base de dados não são suficientes para obter uma correlação significativa. As relações entre os atributos de áudio e a popularidade apresentaram coeficientes baixos, o que impossibilita a construção de um algoritmo capaz de prever a popularidade com base nesses atributos. Acredita-se que a versão da base de dados de domínio público seja mais limitida que a versão paga. Assim, para uma análise mais acurada, seria necessário um investimento financeiro na obtenção dos dados. 