# Detecção de Anomalias em Transações

Projeto de Machine Learning desenvolvido em Python para identificar transações de cartão de crédito que podem ser fraudulentas.

O projeto utiliza diferentes algoritmos de classificação e detecção de anomalias para comparar seus resultados e entender quais características das transações mais influenciam as previsões.

## Objetivo

O objetivo é desenvolver um modelo capaz de identificar transações suspeitas e comparar diferentes técnicas de Machine Learning para esse problema.

O projeto também busca analisar o impacto do desbalanceamento dos dados, já que a quantidade de transações fraudulentas é muito menor que a quantidade de transações normais.

## Dataset

Foi utilizado o dataset **Credit Card Fraud Detection**, disponibilizado pelo TensorFlow.

O dataset contém informações sobre transações de cartão de crédito, incluindo a classificação:

* `0` → Transação normal
* `1` → Transação fraudulenta

O dataset possui uma grande diferença entre a quantidade de transações normais e fraudulentas, tornando o problema um caso de dados desbalanceados.

## Tecnologias utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* SHAP
* Matplotlib
* Seaborn

## Modelos utilizados

### Logistic Regression

Utilizado como modelo inicial para estabelecer uma comparação com os outros algoritmos.

### Random Forest

Modelo baseado em várias árvores de decisão, utilizado para identificar padrões mais complexos nas transações.

### XGBoost

Modelo de Gradient Boosting utilizado para melhorar a capacidade de classificação das transações.

### Isolation Forest

Algoritmo de detecção de anomalias utilizado para identificar transações diferentes do comportamento considerado normal.

## Etapas do projeto

O projeto é dividido nas seguintes etapas:

1. Carregamento do dataset
2. Análise exploratória dos dados
3. Verificação do desbalanceamento das classes
4. Tratamento e transformação dos dados
5. Separação dos dados em treino e teste
6. Treinamento dos modelos
7. Avaliação dos resultados
8. Comparação dos modelos
9. Análise das principais características utilizando SHAP

## Métricas

Como o dataset possui poucas transações fraudulentas, a acurácia não é suficiente para avaliar os modelos.

Por isso, são utilizadas métricas como:

* Precision
* Recall
* F1-Score
* ROC-AUC
* PR-AUC
* Matriz de confusão

O **Recall** é especialmente importante porque representa a capacidade do modelo de identificar transações fraudulentas.

## Explicabilidade

Foi utilizada a biblioteca **SHAP** para analisar quais características possuem maior influência nas decisões do modelo.

Isso permite entender melhor por que uma determinada transação pode ser considerada suspeita pelo modelo.

## Resultado

Ao final do projeto, os modelos são comparados para identificar qual apresenta o melhor desempenho na detecção de transações fraudulentas.

O projeto também permite analisar o equilíbrio entre detectar mais fraudes e evitar que transações legítimas sejam classificadas como suspeitas.
