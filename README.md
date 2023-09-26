# PySpark-Credit-Card-Fraud-Detection
Utilização do PySpark para detectar fraudes em transações de cartão de crédito realizadas por titulares de cartões europeus durante o ano de 2023.

<p align="center">
    <img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.3X8ke9hthJvDuaXSd_MUYQHaDY%26pid%3DApi&f=1&ipt=68466374b02d87c71f3d4704437804998ff7f870d4c1cb7079a34bafd77751c4&ipo=images" alt="card">
</p>

Este projeto tem como objetivo desenvolver um sistema de detecção de fraudes em transações de cartão de crédito, uma tarefa crítica para instituições financeiras e empresas de processamento de pagamentos. Para alcançar esse objetivo, utilizei o poderoso framework PySpark, que oferece recursos de processamento distribuído para lidar com grandes volumes de dados de maneira eficiente.

## Tecnologias Utilizadas
- PySpark: PySpark é a interface Python para o Apache Spark, um framework de processamento de dados em larga escala. Ele nos permitiu lidar com grandes datasets e aplicar algoritmos de aprendizado de máquina de maneira distribuída.
- Random Forest Classifier: Eu escolhi o algoritmo Random Forest como modelo de classificação devido à sua robustez e capacidade de lidar com dados desbalanceados, comuns em problemas de detecção de fraudes.

## Etapas Principais
### Pré-processamento dos Dados
- Definição do esquema dos dados;
- Tratamento de valores ausentes;
- Criação de uma coluna de recursos usando o VectorAssembler;
- Normalização dos recursos com o StandardScaler.
### Treinamento do Modelo
- Inicialização do modelo Random Forest Classifier;
- Treinamento do modelo com um conjunto de treinamento.
### Avaliação do Modelo
- Avaliação do modelo usando métricas como AUC (Area Under the Receiver Operating Characteristic curve), precisão, recall e F1-score;
- Cálculo da matriz de confusão para avaliar o desempenho em detalhes.

## Resultados
O modelo treinado demonstrou uma capacidade sólida de detectar transações fraudulentas, com uma alta pontuação AUC e um recall significativo.

## Conclusão
Este projeto ilustra como a combinação de PySpark e um modelo Random Forest pode ser poderosa na detecção de fraudes em transações de cartão de crédito, especialmente em um cenário em que as transações fraudulentas representam **15%** do conjunto de dados. A capacidade de lidar com grandes volumes de dados e produzir resultados precisos é essencial para empresas que desejam proteger seus clientes contra atividades fraudulentas. Além disso, a interpretabilidade do modelo permite uma análise mais profunda das transações suspeitas, melhorando ainda mais a segurança financeira.

<p align="center">
    <img src="https://i.imgur.com/aYUr0lh.png" alt="CreditCard">
</p>

||-
        
## Fonte dos dados:
https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023
## Dicionário de Dados
- **id**: Identificador exclusivo para cada transação.

- **V1-V28**: Recursos anonimizados que representam vários atributos da transação, como hora, local, etc. Esses recursos são anonimizados por questões de privacidade e segurança.

- **Amount**: Valor da transação, indicando o montante envolvido na transação.

- **Class**: Rótulo binário que indica se a transação é fraudulenta (1) ou não (0).
