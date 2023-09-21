# ETL Process for Product Data

This repository contains the ETL (Extraction, Transformation, and Loading) process for the company's product data under study, involving the extraction of data from raw sources, transformation into an analytical format, and loading into the destination database (in this case, Google BigQuery on GCP).

## Author
Ubiratan J. Motta Filho
Created on: 08/17/2023

## Overview
This ETL process was created to move product data from the raw layer to the analytical layer, enabling more comprehensive analyses and reports.

## Source and Destination Layers
- Source Layer: Raw
- Destination Layer: Analytical

## Objective
The objective of this ETL process is to load product data into the analytical layer for detailed analysis and reporting.

## Prerequisites
- Python environment with the necessary libraries (google-cloud-bigquery, pyspark, argparse)
- Access to Google Cloud services (BigQuery)
- Properly formatted JSON files in the source directory

## Usage
1. Ensure the required Python environment and mandatory libraries are installed.
2. Execute the ETL process using the provided script.

## Parameters
- `p_dataref`: Date reference in the format YYYYMMDD (e.g., 20220530)
- `p_ambiente`: Execution environment (dev, hml, prd)

## Spark Configuration
The ETL process utilizes Spark for data processing. The Spark session and context are initialized with specific configurations for improved performance.

## Logger
The ETL process employs logging to provide detailed information about the execution steps.

## Data Processing Steps
1. Reading raw JSON files from the source directory based on the specified date reference and topic.
2. Structuring and expanding nested structures in the data.
3. Filtering records with missing or invalid data.
4. Transforming and cleaning the data to create the desired schema.
5. Converting the processed data into a Pandas DataFrame.
6. Loading the Pandas DataFrame into a BigQuery table in the 'ANALITICO_CONTROLE_LOJA' dataset.

## BigQuery Destination
- Dataset: ANALITICO_CONTROLE_LOJA
- Table: CONSOLIDADO_PRODUTO

## Running the ETL Process
1. Ensure the Python environment is correctly configured with the necessary libraries.
2. Execute the provided script with the required parameters.

## Notes
- This ETL process was designed for the specific structure and schema of co-brokerage data.
- Ensure proper access to Google Cloud services and permissions for data loading.

---
**Disclaimer**: This ETL process is provided "as-is" and may require customization to fit your specific data and requirements.

------------------------------------------------------------------------------------------------
# Processo ETL para dados de Produtos

Este repositório contém o processo ETL (Extração, Transformação e Carregamento) para os dados de produtos da empresa em estudo, que envolve a extração de dados de fontes brutas, a transformação em um formato analítico e o carregamento no banco de dados de destino (neste caso o BigQuery da GCP).


## Autor
Ubiratan J. Motta Filho
Criado em: 17/08/2023


## Visão Geral  
Este processo ETL foi criado para carregar dados de produtos da camada bruta para a camada analítica, permitindo análises e relatórios mais completos.  
  
## Camadas de Origem e Destino  
- Camada de Origem: Bruta  
- Camada de Destino: Analítica  
  
## Objetivo  
O objetivo deste processo ETL é carregar os dados de produtos na camada analítica para análises e relatórios mais detalhados.  
  
  
## Pré-requisitos  
- Ambiente Python com as bibliotecas necessárias (google-cloud-bigquery, pyspark, argparse)  
- Acesso aos serviços do Google Cloud (BigQuery)  
- Arquivos JSON formatados corretamente no diretório de origem  
  
## Uso  
1. Certifique-se de que o ambiente Python necessário e as bibliotecas obrigatórias estão instalados.  
2. Execute o processo ETL usando o script fornecido.  
  
## Parâmetros  
- `p_dataref`: Referência de data no formato YYYYMMDD (por exemplo, 20220530)  
- `p_ambiente`: Ambiente de execução (dev, hml, prd)  
  
## Configuração do Spark  
O processo ETL utiliza o Spark para processamento de dados. A sessão e o contexto do Spark são inicializados com configurações específicas para melhor desempenho.  
  
## Logger  
O processo ETL utiliza um registro para fornecer informações detalhadas sobre as etapas de execução.  
  
## Etapas de Processamento de Dados  
1. Leitura de arquivos JSON brutos do diretório de origem com base na referência de data e tópico especificados.  
2. Estruturação e expansão de estruturas aninhadas nos dados.  
3. Filtragem de registros com dados ausentes ou inválidos.  
4. Transformação e limpeza dos dados para criar o esquema desejado.  
5. Conversão dos dados processados em um DataFrame Pandas.  
6. Carregamento do DataFrame Pandas em uma tabela BigQuery no conjunto de dados 'ANALITICO_CONTROLE_LOJA'.  
  
## Destino no BigQuery  
- Conjunto de Dados: ANALITICO_CONTROLE_LOJA
- Tabela: CONSOLIDADO_PRODUTO
  
## Executando o Processo ETL  
1. Certifique-se de que o ambiente Python está configurado corretamente com as bibliotecas necessárias.  
2. Execute o script fornecido com os parâmetros obrigatórios.  
  
## Observações  
- Este processo ETL foi projetado para a estrutura e o esquema específicos dos dados de cocorretagem.  
- Garanta acesso adequado aos serviços do Google Cloud e permissões para o carregamento de dados.  
  
---  
  
**Aviso**: Este processo ETL é fornecido "como está" e pode requerer personalização para se adequar aos seus dados e requisitos específicos.
