# ETL Clima

Pipeline ETL desenvolvido em Python para coleta, transformação e armazenamento de dados meteorológicos utilizando Apache Airflow, PostgreSQL e Docker.

## Sobre o Projeto

O objetivo deste projeto é automatizar a coleta de dados climáticos da API OpenWeather, realizar o tratamento das informações e armazená-las em um banco de dados PostgreSQL.

Todo o fluxo é orquestrado pelo Apache Airflow e executado em containers Docker.

## Arquitetura

OpenWeather API → Extract → Transform → Load → PostgreSQL

### Fluxo do Pipeline

1. **Extract**

   * Consome dados da API OpenWeather.
   * Obtém informações climáticas da cidade de Goiânia.

2. **Transform**

   * Realiza o tratamento e organização dos dados utilizando Pandas.
   * Converte os dados para um formato estruturado.

3. **Load**

   * Armazena os dados processados no PostgreSQL.
   * Permite consultas e análises futuras.

## Tecnologias Utilizadas

* Python
* Pandas
* PostgreSQL
* Apache Airflow
* Docker
* SQLAlchemy
* OpenWeather API

## Estrutura do Projeto

```text
big_data/
│
├── dags/
│   └── weather_dag.py
│
├── src/
│   ├── extract_data.py
│   ├── transform_data.py
│   └── load_data.py
│
├── data/
├── config/
├── logs/
├── plugins/
│
├── docker-compose.yaml
├── pyproject.toml
└── README.md
```

## Execução

### Subir os containers

```bash
docker compose up -d
```

### Verificar containers

```bash
docker ps
```

### Acessar o Airflow

```text
http://localhost:8080
```

## Resultados

* Extração automática de dados meteorológicos.
* Transformação dos dados utilizando Pandas.
* Armazenamento em PostgreSQL.
* Orquestração do pipeline através do Apache Airflow.
* Ambiente totalmente containerizado com Docker.

## Aprendizados

Durante o desenvolvimento foram aplicados conceitos de:

* ETL (Extract, Transform, Load)
* Engenharia de Dados
* Orquestração de pipelines
* Bancos de dados relacionais
* Containers Docker
* Integração com APIs REST

## Autor

Matheus Ribeiro

Projeto desenvolvido para a disciplina de Extensão do curso de Análise e Desenvolvimento de Sistemas.
