# 📦 Pipeline Bronze → Silver em Streaming (Databricks Free Edition)

Este repositório contém a implementação de um pipeline de dados do https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business/data 
Usando **arquitetura Medallion (Bronze → Silver)**, **Spark Structured Streaming** e **Delta Lake**.
Desenvolvido na **Databricks Free Edition**.


## 🚀 Objetivo do Projeto

Criar um pipeline robusto que:

- Converte em Delta Lake
- Faz leitura contínua com Structured Streaming
- Aplica transformações e qualidade de dados
- Executa **UPSERT/MERGE** na camada Silver
- Mantém histórico usando Delta
- Armazena checkpoints em caminhos permitidos no Free Edition 
