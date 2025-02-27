---
icon: plug
---

# Connectors

## Setting Up Connectors in AnalyticsCreator

Connectors in AnalyticsCreator allow users to establish data source connections, enabling efficient data management and analysis. Here’s a comprehensive guide to understanding and setting up various connectors.

### Navigating Connectors

To create or edit a connector, navigate through the toolbar menu:

**Select** **Sources** -> **Connectors**

{% embed url="https://www.canva.com/design/DAGY0qZnlJA/GksgltzpUrPpIexhggPHvw/view?utlId=h9e3db782a9&utm_campaign=designshare&utm_content=DAGY0qZnlJA&utm_medium=link2&utm_source=uniquelinks" %}

### Connectors define the data source logic.&#x20;

### Here’s a list of connector types supported by AnalyticsCreator:

* MS SQL Server
* Oracle
* CSV
* Excel
* DuckDB (Parquet, CSV, S3 )
* MS Access
* OLEDB
* SAP (using Theobald connector)
* ODBC

### Connection String and Templates

AnalyticsCreator provides a friendly interface for generating connection string templates.&#x20;

For several connector types, users can access these templates by clicking the “Template” button. Here’s an example template:

```
PROVIDER=SQLNCLI11;Data Source=\[SERVER];Initial Catalog=\[DATABASE];Integrated Security=SSPI;
```

Make sure to replace the placeholders `[SERVER]` and `[DATABASE]` with the actual server and database names.

### CSV Connector Properties

The CSV connector has unique properties enhancing file handling capabilities. Users should pay attention to these additional settings to ensure seamless file integration and processing.

### Row Delimiters

When defining row delimiters, users can utilize specific abbreviations for ease. These include:

* `{CR}` for Carriage Return
* `{LF}` for Line Feed
* `{t}` for Tabulator

These specifications enable seamless formatting and data structuring within your source files.

### Automating Data Source Descriptions

For automatic data source description retrieval, ensure your connections to these data sources are active and functional. This automation simplifies data management and improves operational efficiency.

### Cloud Storage for Connectors

Store connector definitions and associated data sources in the cloud. Cloud storage provides a durable and accessible platform for managing your data across different repositories, enhancing collaboration and data security.

### Encrypted strings

We highly recommend keeping your connection strings encrypted.&#x20;

To encrypt your string, simply click on Options → Encrypted Strings → New.&#x20;

To use your encrypted strings in your sources, enclose the name you’ve created with # on both sides.&#x20;

For example, if your DSN=DuckDB, the connection string will be #DuckDB#

{% embed url="https://www.canva.com/design/DAGgT2DA3I8/igyQqQqwFilzIzIuYIRcDQ/view" %}

