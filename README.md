# Criando Soluções para o Power BI Report Server - Zero Custo

Esta documentação tem como objetivo explicar a arquitetura e as etapas do projeto **"Criando Soluções para o Power BI Report Server - Zero Custo"**. O projeto visa oferecer soluções em Business Intelligence para melhorar processos de gerenciamento de recursos humanos e análise de dados, com foco em transformar planilhas do Excel em um ambiente de Power BI integrado.

## Primeiro Contato

### Cenário

O projeto nasceu da necessidade de uma empresa de médio porte em otimizar seus processos de gerenciamento de recursos humanos e análise de dados. A empresa utilizava planilhas do Excel para essas tarefas, o que gerava dificuldades na integridade dos dados - o foco também é mostrar que é possível ter um ambiente de análise de dados integrado e com zero custo.

### Desafios e Soluções

- Qual o problema?
    - Utilização de planilhas de Excel para consulta e análise de dados.
    - Cliente com budget baixíssimo para contratação de um sistema de análise integrado.
- Seu trabalho para resolver?
    - Identifiquei as fontes de dados, a partir das fontes iniciei a criação do banco de dados. Após finalizar o banco comecei a gerar os relatórios paginados e dashboards - nesse processo foi realizado a configuração do Report Server para o ambiente da empresa.
- Qual foi o resultado?
    - Um ETL que consome novas informações da planilha.
    - Um banco de dados para criação de relatórios e consultas.
    - Um ambiente análitico totalmente integrado e com zero custo.

### Ferramentas

As ferramentas utilizadas no projeto são:

- Excel
- Visual Studio 2019 (Database Project, SSIS, SSRS)
- SQL Server
- Power BI
- Power BI Report Server
- Figma

### Informações das Planilhas

Foram fornecidas duas planilhas:

1. Cargos.xlsx: Informações sobre cargos e códigos correspondentes.
2. Funcionarios.xlsx: Detalhes dos funcionários, incluindo informações completas sobre cada um.

## ETL e SQL

### Criação dos Serviços no Visual Studio

A construção do projeto começa no Visual Studio 2019, criando os seguintes componentes:

- Database Project para o banco de dados.
- Projeto SSIS para ETL (Extração, Transformação e Carga).
- Projeto SSRS para relatórios.

### Criação das Tabelas

A estrutura das tabelas é definida no projeto do banco de dados, refletindo as informações das planilhas.

### Deploy no SQL Server

As soluções são implantadas no SQL Server após a construção:

1. O Database Project é publicado no SQL Server.

## ETL

São criados pacotes ETL para carregar as tabelas do banco de dados:

- Um pacote para carregar a tabela de funcionários.
- Um pacote para carregar a tabela de cargos.

## BI

### Dashboard

Um dashboard é criado no Power BI, envolvendo as seguintes etapas:

1. Conexão com a fonte de dados SQL Server.
2. Transformações necessárias nos dados.
3. Utilização da tabela de calendário para informações temporais.
4. Criação de medidas DAX para análises.

![Architecture](Resources/Imgs/Dashboard.png)

### Report

Um relatório é criado no Power BI, com:

1. Conexão com as fontes de dados.
2. Uso de parâmetros para interatividade.
3. Visualizações e análises ad-hoc.

![Architecture](Resources/Imgs/Report.png)

### Deploy de Reports e Dashboards

Os relatórios e dashboards são implantados no Power BI Report Server:

1. Configuração do servidor de relatório.
2. Deploy do dashboard e relatório.

### Incorporação de Reports e Dashboards

Os relatórios e dashboards podem ser incorporados em sites ou compartilhados por meio de URLs ou iFrames.

**Exemplo do relatório páginado no Report Server:**
![ReportEmbed](Resources/Imgs/EmbedReport.png)

**Exemplo do Dashboard no Report Server:**
![DashboardEmbed](Resources/Imgs/EmbedDashboard.png)

## Arquitetura

### Exemplo Conceitual da Arquitetura

![Architecture](Resources/Imgs/architecture.png)

Essa documentação apresentou de forma clara as etapas e componentes do projeto **"Sinergia de Dados: Excel para Power BI através do Ciclo ETL e SQL"**. Desde a integração inicial das planilhas Excel até a criação de dashboards e relatórios no Power BI, todas as etapas foram explicadas detalhadamente. Isso permite que tanto desenvolvedores quanto não técnicos entendam o funcionamento e a utilidade desse projeto de Business Intelligence.


---
# Building Solutions for Power BI Report Server - Zero Cost

This documentation aims to explain the architecture and steps of the project **"Building Solutions for Power BI Report Server - Zero Cost"**. The project aims to provide Business Intelligence solutions to improve human resources management processes and data analysis, with a focus on transforming Excel spreadsheets into an integrated Power BI environment.

## Initial Contact

### Scenario 

The project was born from the need of a medium-sized company to optimize its human resources management and data analysis processes. The company used Excel spreadsheets for these tasks, which created difficulties in data integrity - the focus is also to show that it is possible to have an integrated data analysis environment at zero cost.

### Challenges and Solutions
- What was the problem?
    - Use of Excel spreadsheets for data consultation and analysis.
    - Client with a very low budget to hire an integrated analysis system.
- What was your work to solve it?
    - I identified data sources and initiated the database creation process. After completing the database, I started generating paginated reports and dashboards - in this process, the Report Server was configured for the company's environment.
- What was the result?
    - An ETL that consumes new information from the spreadsheet.
    - A database for creating reports and queries.
    - A fully integrated and cost-free analytical environment.

### Tools

The tools used in the project are:

- Excel
- Visual Studio 2019 (Database Project, SSIS, SSRS)
- SQL Server
- Power BI
- Power BI Report Server
- Figma

### Spreadsheet Information

Two spreadsheets were provided:

1. Cargos.xlsx: Information about job positions and corresponding codes.
2. Funcionarios.xlsx: Employee details, including comprehensive information about each employee.

## ETL and SQL

### Creating Services in Visual Studio

The project's construction starts in Visual Studio 2019, creating the following components:

- Database Project for the database.
- SSIS Project for ETL (Extraction, Transformation, and Loading).
- SSRS Project for reports.

### Table Creation

The table structure is defined in the database project, reflecting the information from the spreadsheets.

### Deploying to SQL Server

The solutions are deployed to the SQL Server after construction:

1. The Database Project is published to the SQL Server.

## ETL

ETL packages are created to load the database tables:

- A package to load the employee table.
- A package to load the job position table.

## BI

### Dashboard

A dashboard is created in Power BI, involving the following steps:

1. Connecting to the SQL Server data source.
2. Necessary data transformations.
3. Use of a calendar table for temporal information.
4. Creation of DAX measures for analysis.

![Architecture](Resources/Imgs/Dashboard.png)

### Report

A report is created in Power BI, with:

1. Connection to data sources.
2. Use of parameters for interactivity.
3. Relevant visualizations and ad-hoc analysis.

![Architecture](Resources/Imgs/Report.png)

### Deploying Reports and Dashboards

The reports and dashboards are deployed to the Power BI Report Server:

1. Configuration of the report server.
2. Deployment of the dashboard and report.

### Embedding Reports and Dashboards

The reports and dashboards can be embedded in websites or shared through URLs or iFrames.

**Paginated Report example on Report Server:**
![ReportEmbed](Resources/Imgs/EmbedReport.png)

**Dashboard example on Report Server:**
![DashboardEmbed](Resources/Imgs/EmbedDashboard.png)


## Architecture

### Conceptual Architecture Example

![Architecture](Resources/Imgs/architecture.png)

This documentation has provided a clear explanation of the steps and components of the project **"Data Synergy: Excel to Power BI through ETL Cycle and SQL"**. From the initial integration of Excel spreadsheets to the creation of dashboards and reports in Power BI, all the steps have been explained in detail. This allows both developers and non-technical individuals to understand the functioning
