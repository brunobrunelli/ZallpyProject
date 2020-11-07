# ZallpyProject

* **Desenvolvedor**: Bruno Scovoli Bruneli
* **Data**: 2020-11-07
* **Objetivo**: Projeto criado com o objetivo de responder ao teste proposto pela empresa Zallpy para área de BI.

**Descrição**: 
<p>Foi disponibilizado um arquivo .bak que será utilizado para realizar o restore de um banco de dados no SQL Server 2019. Esse arquivo é responsável por conter as tabelas fato e dimensão em um modelo DW que será utilizado no desenvolvimento de um painel na ferramenta Tableau.</p>

`/documents`: diretório responsável por conter arquivos utilizados no desenvolvimento do projeto.

`/sql`: diretório responsável por conter o arquivo .bak.

`/visualization`: diretório responsável por conter o arquivo **bmw_challenge_tableau_panel.twb** (painel tableau).

Versão utilizadas:
* SQL Server 2019
* Tableau Desktop 2020.3

---

**Painel Tableau**

O painel foi desenvolvido utilizando a conexão em tempo real com o banco de dados SQL Server para acessar as seguintes tabelas:
* fact_pricing
* dim_cars
* dim_fuel
* dim_date

Foram utilizados os campos disponíveis nas entidades fato e dimensões para criação das visualizações e painéis. Também foram criados campos calculados, funcionalidades, ações e parametros que compõem o painéis, assim como:
  
##### Campos Calculados:
```
* Range Sold Year: responsável por filtrar os dados das visualizações quando modificado o parametro *Param Sold Year*.
* Range Sold Month: responsável por filtrar os dados das visualizações quando modificado o parametro *Param Sold Month*.
* # Quantity Sold: responsável pela quantidade de vendas realizadas.
* % Total Sales:  responsável pelo percentual das vendas realizadas.
* $ Max Price: responsável por retornar o maior preço.
* $ Min Price: responsável por retornar o menor preço.
* $ Sales Weighted Average: responsável por retornar a média ponderada das vendas realizadas.
```

##### Ações: 
```
* Filter by models - responsável por filtrar as visualizações disponíveis no painel "Sales per month" quando selecionado um modelo de carro.
* Filter Sales Details - responsável por filtrar a visualização "Sales Details" no painel "Sales arround months".
* Highlight Quantity and Sales Revenue - responsável por destacar os dados das visualizações "Total Sales Revenue" e "Quantity Sales" no painel "Sales arround months".
```

##### Parametros:
```
* Param Sold Month: responsável por conter os valores do campo "Sold Month" em formato de lista.
* Param Sold Year: responsável por conter os valores do campo "Sold Year" em formato de lista.
```

