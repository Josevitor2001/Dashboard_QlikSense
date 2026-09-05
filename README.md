# 📊 Termômetro de Metas — PostgreSQL + Qlik Sense

## 📌 Sobre o projeto

Este projeto foi desenvolvido como um desafio prático de **Análise de Dados e Business Intelligence**, com o objetivo de criar uma solução para acompanhamento de indicadores de consumo de energia e interrupções de serviço.

A proposta foi construir desde a estruturação dos dados em banco até a visualização dos principais indicadores em um dashboard no **Qlik Sense**, simulando um cenário com grande volume de registros.

## 🛠️ Tecnologias utilizadas

* **PostgreSQL** — criação e estruturação do banco de dados
* **DBeaver** — gerenciamento do banco e execução das consultas SQL
* **SQL** — criação de tabelas, relacionamentos, consultas e views
* **Qlik Sense** — tratamento, análise e visualização dos dados
* **Set Analysis** — construção de indicadores e comparação entre realizado e meta

## 🗄️ Estrutura dos dados

O banco foi estruturado utilizando uma abordagem semelhante a um modelo dimensional, separando informações de região dos registros de consumo e interrupções.

### `Dim_Regioes`

Tabela responsável pelas informações das regiões e suas respectivas metas:

* ID da região
* Nome da região
* Meta de consumo mensal
* Meta máxima de interrupção

### `Fato_Consumo_Interrupcoes`

Tabela contendo os registros operacionais:

* Data e hora
* Região
* Consumo de energia (MWh)
* Duração das interrupções
* Status do serviço

As tabelas foram relacionadas através do **ID da região**, utilizando chave primária e chave estrangeira.

## 🔎 Tratamento e preparação

No PostgreSQL foi criada a view:

`vw_indicadores_energia`

Essa view realiza a integração entre os dados de regiões, metas, consumo e interrupções, deixando as informações preparadas para utilização na ferramenta de BI.

O objetivo dessa etapa foi centralizar parte da lógica no banco de dados e facilitar a posterior carga e análise dos dados no Qlik Sense.

## 📈 Dashboard no Qlik Sense

Após a preparação dos dados, foi realizada a conexão do **Qlik Sense diretamente com o PostgreSQL**.

No dashboard foram trabalhados indicadores como:

* Consumo de energia
* Duração das interrupções
* Quantidade de regiões
* Status do serviço
* Comparação entre valores realizados e metas
* Indicadores visuais para identificação de situações críticas

Também foi utilizado **Set Analysis** para trabalhar comparações e regras específicas dentro dos indicadores.

## 🎯 Objetivo

O principal objetivo foi transformar dados operacionais armazenados em banco de dados em informações visuais que possam apoiar a tomada de decisão.

O projeto permitiu praticar um fluxo de BI envolvendo:

**Banco de Dados → SQL → Preparação dos Dados → Qlik Sense → Indicadores → Dashboard**

## 📚 Aprendizados

Durante o desenvolvimento foram praticados conceitos de:

* Modelagem de dados
* SQL
* Chaves primárias e estrangeiras
* Views
* Integração PostgreSQL + Qlik Sense
* ETL e preparação de dados
* KPIs
* Set Analysis
* Visualização de dados
* Business Intelligence

---

💡 **Projeto desenvolvido para fins de estudo e portfólio, simulando um cenário de análise de indicadores do setor de energia.**
