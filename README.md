# 📦 Pipeline Bronze → Silver em Streaming

Este repositório contém a implementação de um pipeline de dados desenvolvido como parte do case da startup Juntos Somos Mais, utilizando o dataset disponível em:
https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business/data

O projeto aplica a Arquitetura Medallion (Bronze → Silver) com Spark Structured Streaming e Delta Lake, totalmente desenvolvido no Databricks Free Edition.


## 🚀 Objetivo do Projeto

Criar um pipeline robusto que:

- Converte em Delta Lake
- Faz leitura contínua com Structured Streaming
- Aplica transformações e qualidade de dados
- Executa UPSERT/MERGE na camada Silver
- Mantém histórico usando Delta
- Armazena checkpoints em caminhos permitidos no Free Edition 
