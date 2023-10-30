# Classificação com KNN

Este projeto tem como objetivo principal a aplicação do algoritmo K-Nearest Neighbors (KNN) para classificação de dados, visando o entendimento do funcionament odo algoritmoo.  O projeto inclui análise exploratória, aplicação do KNN, técnicas de validação, otimização de hiperparâmetros e visualização das fronteiras de decisão.

![Cartão de Visita](https://cdn.discordapp.com/attachments/1167606494536142864/1167606533811601429/Copia_de_Modern_Creative_Business_Card.png?ex=654ebd52&is=653c4852&hm=78a86e0bfea405ba39b4970117881fee3e14aefb38b23db2ad685b7a785f6708&)

## Índice
- [1. Introdução](#1-Introdução)
- [2. Compreensão dos Dados](#2-Compreensão-dos-Dados)
- [3. Plano de Ação](#3-Plano-de-Ação)
- [4. Insight dos Dados](#4-Insights-dos-Dados)
- [5. Projeções Futuras](#5-Projeções-Futuras)


## 1. Introdução

Este projeto utiliza o algoritmo K-Nearest Neighbors (KNN) para classificar dados do conjunto **Wine**. O KNN é uma técnica de aprendizado de máquina que classifica um ponto de dados com base nos pontos mais próximos a ele no espaço multidimensional. No contexto do conjunto de dados Wine, que contém informações químicas de vinhos, o KNN será aplicado para categorizar vinhos em diferentes grupos. Os dados estão disponiveis no [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/109/wine), [Kaggle](https://www.kaggle.com/datasets/tawfikelmetwally/wine-dataset/data) e [Scikit Learn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine).
 

## 2. Compreensão dos Dados
Os dados do dataset wine são compostos por 14 features com uma delas sendo target e 178 labels. Todos os dados são do tipo númerico, há ausencia de valores núlos e duplicados. O dicionario de nommenclatura é composto por:

|Attribute|Definition|Data Type|
|---|---|---|
|alcohol|Teor alcoólico|float64|
|malic_acid|Ácido málico|float64|
|ash|Cinzas|float64|
|alcalinity_of_ash|Alcalinidade das cinzas|float64|
|magnesium|Magnésio|float64|
|total_phenols|Fenóis totais|float64|
|flavanoids|Flavonoides|float64|
|nonflavanoid_phenols|Fenóis não flavonoides|float64|
|proanthocyanins|Proantocianidinas|float64|
|color_intensity|Intensidade da cor|float64|
|hue|Cor|float64|
|od280/od315_of_diluted_wines|OD280/OD315 de vinhos diluídos|float64|
|proline|Proline|float64|
|class|Tipo do vinho (target)|int32|

## 3. Plano de Ação

### 3.1. Objetivo
Após concluir o [projeto inicial de implementação do KNN](https://github.com/lfaferreira/ada-potencia-tech-knn-project), fiquei intrigado em aprofundar meu entendimento sobre seu funcionamento. Este repositório explora detalhadamente a capacidade do algoritmo KNN, com ênfase na classificação e no aprimoramento do entendimento sobre o mesmo.

### 3.2. Ferramentas e Frameworks
Escolpo de ferramentas utilizadas no projeto:

- Python 3.11.5
- Jupyter Notebook
- Git & GitHub
- Kaggle
- Pandas
- Numpy
- Machine Learning Classification Model (KNN)

## 4. Insights dos Dados

*   Flavanoids mostra uma forte correlação com outras características, principalmente com Total Phenols (0.86) e OD280/OD315 of diluted wines (0.79).
*   No entanto, a menor correlação ocorre com a variável target (Class), apresentando um coeficiente de -0.85.
*   A característica Proline destaca-se como a que proporciona a melhor separação entre as classes, especialmente para a classe 0.
*   Color_intensity também se destaca, especialmente quando combinada com Flavanoids e Total Phenols.
*   Foi observado que os dados estão em uma escala significativamente variada. Essa disparidade é evidente nos sumários, análises e nos gráficos de distribuição.
*   A menor valor encontrado está em Nonflavanoid Phenols (0.13).
*   Considerando a vasta gama de escalas, a aplicação de técnicas como PCA (Principal Component Analysis) pode ser benéfica para reduzir a dimensionalidade dos dados, permitindo uma análise mais eficaz e precisa.

## 5. Projeções Futuras
* Adicionar as metricas de Machine Learning e Filtro Selecionado
* Adicionar resultados do projeto
* Adicionar uma conclusão do projeto