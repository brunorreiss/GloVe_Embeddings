# Geração de Texto com Redes Neurais e Embeddings GloVe

Este projeto demonstra como treinar um modelo de rede neural para geração de texto utilizando embeddings de palavras pretreinados (GloVe) e um modelo LSTM. O código está implementado em Python usando a biblioteca Keras.

## Sumário

1. [Importação de Bibliotecas](#importação-de-bibliotecas)
2. [Download e Extração dos Vetores de Palavras GloVe](#download-e-extração-dos-vetores-de-palavras-glove)
3. [Função para Mostrar as Primeiras Linhas de um Arquivo](#função-para-mostrar-as-primeiras-linhas-de-um-arquivo)
4. [Processamento de Texto e Tokenização](#processamento-de-texto-e-tokenização)
5. [Preparação de Sequências para Treinamento](#preparação-de-sequências-para-treinamento)
6. [Carregamento dos Vetores de Palavras GloVe](#carregamento-dos-vetores-de-palavras-glove)
7. [Função para Imprimir os Primeiros Itens de um Dicionário](#função-para-imprimir-os-primeiros-itens-de-um-dicionário)
8. [Criação da Matriz de Embeddings](#criação-da-matriz-de-embeddings)
9. [Construção do Modelo de Rede Neural](#construção-do-modelo-de-rede-neural)
10. [Compilação do Modelo](#compilação-do-modelo)
11. [Treinamento do Modelo](#treinamento-do-modelo)
12. [Função para Geração de Texto](#função-para-geraçao-de-texto)
13. [Geração de Texto com o Modelo Treinado](#geraçao-de-texto-com-o-modelo-treinado)

## Importação de Bibliotecas

As bibliotecas necessárias são importadas para manipulação de dados, processamento de texto, construção de modelo e download de arquivos.

## Download e Extração dos Vetores de Palavras GloVe

Os vetores de palavras GloVe são baixados e descompactados se ainda não estiverem presentes no diretório especificado. Esta etapa é crucial para utilizar embeddings de palavras pretreinados em nosso modelo.

## Função para Mostrar as Primeiras Linhas de um Arquivo

Uma função é definida para abrir um arquivo e exibir as primeiras linhas, permitindo uma rápida inspeção do conteúdo do arquivo.

## Processamento de Texto e Tokenização

Um texto de entrada é definido e tokenizado, convertendo-o em uma sequência de números inteiros que representam as palavras no vocabulário.

## Preparação de Sequências para Treinamento

As sequências de entrada e os rótulos são preparados para o treinamento da rede neural, com as entradas consistindo em subsequências de palavras e os rótulos sendo a próxima palavra na sequência.

## Carregamento dos Vetores de Palavras GloVe

Os vetores de palavras do GloVe são carregados em um dicionário, onde as chaves são as palavras e os valores são os vetores de embeddings correspondentes.

## Função para Imprimir os Primeiros Itens de um Dicionário

Uma função é fornecida para imprimir os primeiros itens de um dicionário, permitindo a inspeção rápida do conteúdo do dicionário de embeddings.

## Criação da Matriz de Embeddings

Uma matriz de embeddings é criada e preenchida com os vetores de palavras do GloVe para as palavras no vocabulário do texto de entrada.

## Construção do Modelo de Rede Neural

Um modelo sequencial é construído com uma camada de embeddings, uma camada LSTM e uma camada densa com ativação softmax para predição das próximas palavras.

## Compilação do Modelo

O modelo é compilado utilizando o otimizador Adam e a função de perda `categorical_crossentropy`, configurando-o para treinamento.

## Treinamento do Modelo

O modelo é treinado por 300 épocas com os dados de entrada preparados, ajustando os pesos para minimizar a função de perda.

## Função para Geração de Texto

Uma função é definida para gerar uma sequência de texto a partir de um texto inicial utilizando o modelo treinado. A função ajusta a predição com base na diversidade para controlar a aleatoriedade na escolha das próximas palavras.

## Geração de Texto com o Modelo Treinado

O modelo treinado é utilizado para gerar e imprimir uma sequência de texto com 10 palavras a partir de um texto inicial fornecido.

---
# Text Generation with Neural Networks and GloVe Embeddings

This project demonstrates how to train a neural network model for text generation using pre-trained GloVe word embeddings and an LSTM model. The code is implemented in Python using the Keras library.

## Table of Contents

1. [Importing Libraries](#importing-libraries)
2. [Downloading and Extracting GloVe Word Vectors](#downloading-and-extracting-glove-word-vectors)
3. [Function to Show First Lines of a File](#function-to-show-first-lines-of-a-file)
4. [Text Processing and Tokenization](#text-processing-and-tokenization)
5. [Preparing Sequences for Training](#preparing-sequences-for-training)
6. [Loading GloVe Word Vectors](#loading-glove-word-vectors)
7. [Function to Print First Items of a Dictionary](#function-to-print-first-items-of-a-dictionary)
8. [Creating the Embedding Matrix](#creating-the-embedding-matrix)
9. [Building the Neural Network Model](#building-the-neural-network-model)
10. [Compiling the Model](#compiling-the-model)
11. [Training the Model](#training-the-model)
12. [Text Generation Function](#text-generation-function)
13. [Generating Text with the Trained Model](#generating-text-with-the-trained-model)

## Importing Libraries

The necessary libraries are imported for data manipulation, text processing, model building, and file downloading.

## Downloading and Extracting GloVe Word Vectors

The GloVe word vectors are downloaded and extracted if they are not already present in the specified directory. This step is crucial for using pre-trained word embeddings in our model.

## Function to Show First Lines of a File

A function is defined to open a file and display the first few lines, allowing for a quick inspection of the file's content.

## Text Processing and Tokenization

An input text is defined and tokenized, converting it into a sequence of integers representing the words in the vocabulary.

## Preparing Sequences for Training

Input sequences and labels are prepared for training the neural network, with inputs consisting of subsequences of words and labels being the next word in the sequence.

## Loading GloVe Word Vectors

The GloVe word vectors are loaded into a dictionary where the keys are words and the values are the corresponding embedding vectors.

## Function to Print First Items of a Dictionary

A function is provided to print the first few items of a dictionary, allowing for quick inspection of the embedding dictionary's content.

## Creating the Embedding Matrix

An embedding matrix is created and filled with the GloVe word vectors for the words in the input text's vocabulary.

## Building the Neural Network Model

A sequential model is built with an embedding layer, an LSTM layer, and a dense layer with softmax activation for predicting the next words.

## Compiling the Model

The model is compiled using the Adam optimizer and the `categorical_crossentropy` loss function, setting it up for training.

## Training the Model

The model is trained for 300 epochs with the prepared input data, adjusting weights to minimize the loss function.

## Text Generation Function

A function is defined to generate a sequence of text from an initial seed text using the trained model. The function adjusts predictions based on diversity to control randomness in word selection.

## Generating Text with the Trained Model

The trained model is used to generate and print a sequence of text with 10 words from a given initial seed text.
