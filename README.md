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


## 🎯 Motivações Técnicas — Por que usar essas tecnologias?

🐍 Por que PySpark?

Linguagem amplamente usada por engenheiros de dados

Ideal para manipulação de grandes volumes

APIs mais simples e expressivas que Scala para ETL

Fácil integração com Databricks e Delta Lake

É a tecnologia mais adequada para times mistos (data + software), sendo a mais produtiva para ETL.


⚡ Por que Spark Structured Streaming?

Oferece processamento contínuo, essencial para real-time

Garante fault-tolerance e exactly-once processing

É escalável e gerenciado automaticamente pelo Databricks

Reduz a complexidade de clusters e estados


🔺 Por que Delta Lake?

É o formato oficial do Databricks

Garante:

ACID Transactions

Time Travel

Merge / Upsert

Schema Evolution

Permite fluxos batch e streaming usando o mesmo formato

Evita corrupção de dados em streaming (coisa que parquet/csv não fazem)


🧱 Por que Arquitetura Medallion (Bronze → Silver → Gold)?

Padroniza pipelines entre squads

Separa zonas de:

ingestão bruta (Bronze)

limpeza e qualidade (Silver)

agregações para negócio (Gold)

Escalável e modular

Suporte nativo no Databricks
