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