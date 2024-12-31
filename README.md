English description below


Classificação de Sentimentos com IMDb Reviews

Este projeto foca na criação de um modelo para classificação binária de sentimentos utilizando a base de dados de avaliações de filmes do IMDb.

Durante o desenvolvimento, explorei técnicas de pré-processamento de texto, otimização de hiperparâmetros e treinamento de um modelo de rede neural usando TensorFlow e Keras Tuner.

Passos que segui no projeto

1. Carregamento e exploração do dataset

Utilizei o dataset imdb_reviews do TensorFlow Datasets, que contém 50.000 avaliações de filmes classificadas como positivas ou negativas. Separei os dados em conjuntos de treino, validação e teste.

2. Pré-processamento

Implementei um processo de pré-processamento para normalizar os textos:

Converto para letras minúsculas.

Removo tags HTML utilizando expressões regulares.

3. Vetorização de texto

Utilizei a camada TextVectorization do TensorFlow para transformar os textos em vetores TF-IDF. Adaptei a camada com base nos textos do conjunto de treino.

4. Construção do modelo

Defini uma função para criar o modelo com Keras, incluindo:

Uma camada de vetorização.

Duas camadas densas com hiperparâmetros ajustáveis como número de unidades e funções de ativação.

Camadas de normalização (BatchNormalization) e otimização (SGD com taxa de aprendizado, momentum e Nesterov ajustáveis).

5. Otimização de hiperparâmetros

Usei o Keras Tuner para otimizar os hiperparâmetros, realizando uma busca bayesiana. Testei diferentes configurações de unidades, funções de ativação, taxas de aprendizado e momentums.

6. Treinamento do modelo

Treinei o modelo com os hiperparâmetros ótimos encontrados, utilizando o conjunto de validação para monitorar a precisão.

Resultados

Os melhores hiperparâmetros encontrados foram:

Número de unidades: 256

Função de ativação: ReLU

Taxa de aprendizado: 0.0001

O modelo alcançou precisão de teste de 84% e uma precisão de validação de aproximadamente 87% após ajustes e treinamento.





Sentiment Classification with IMDb Reviews

This project focuses on creating a binary sentiment classification model using the IMDb movie reviews dataset.

During development, I explored text preprocessing techniques, hyperparameter optimization, and training a neural network model using TensorFlow and Keras Tuner.

Steps followed in the project

Loading and exploring the dataset

I used the imdb_reviews dataset from TensorFlow Datasets, which contains 50,000 movie reviews classified as positive or negative. The data was split into training, validation, and test sets.

Preprocessing

I implemented a preprocessing pipeline to normalize the text:

Converted text to lowercase.

Removed HTML tags using regular expressions.

Text vectorization

I used the TextVectorization layer from TensorFlow to transform text into TF-IDF vectors. The layer was adapted based on the training set texts.

Model building

I defined a function to create the model with Keras, including:

A vectorization layer.

Two dense layers with adjustable hyperparameters such as the number of units and activation functions.

Normalization layers (BatchNormalization) and optimization (SGD with adjustable learning rate, momentum, and Nesterov).

Hyperparameter optimization

I used Keras Tuner to optimize hyperparameters by conducting a Bayesian search. Tested different configurations of units, activation functions, learning rates, and momentum values.

Model training

I trained the model using the optimal hyperparameters found, leveraging the validation set to monitor accuracy.

Results

The best hyperparameters found were:

Number of units: 256

Activation function: ReLU

Learning rate: 0.0001

The model achieved a test accuracy of 84% and a validation accuracy of approximately 87% after adjustments and training.
