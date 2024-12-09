---
icon: plug
noIndex: true
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Connectors

Connectors in AnalyticsCreator serve as the foundation for integrating external data sources into your Data Warehouse projects. They allow you to define and manage metadata, facilitating seamless data extraction and processing. Below, you'll find detailed instructions for adding, importing, exporting, and managing connectors.

### Supported Connector Types

AnalyticsCreator supports a variety of connectors:

<table data-full-width="false"><thead><tr><th width="248">Connector Type</th><th>Description</th></tr></thead><tbody><tr><td>MSSQL</td><td>Microsoft SQL Server</td></tr><tr><td>ORACLE</td><td>Oracle Database</td></tr><tr><td>CSV</td><td>CSV or text file</td></tr><tr><td>EXCEL</td><td>Excel file</td></tr><tr><td>ACCESS</td><td>Microsoft Access Database</td></tr><tr><td>OLEDB</td><td>OLEDB driver</td></tr><tr><td>SAP</td><td>SAP via Theobald connector</td></tr><tr><td>ODBC</td><td>Any ODBC Driver</td></tr><tr><td>DIRECT</td><td>Direct access to local or <a href="https://learn.microsoft.com/en-us/sql/relational-databases/linked-servers/linked-servers-database-engine?view=sql-server-ver16">linked databases</a></td></tr></tbody></table>

***

{% hint style="info" %}
If your data source is not supported, you can use the **Externally Filled Tables** feature as a workaround.
{% endhint %}

* [**Edit and Manage Connectors**:](create-or-edit-a-connector.md#create-or-edit-a-connector) Use the **Navigation Tree** to list, search, edit, or delete connectors.
* **Refresh Connectors**: Update metadata for existing connectors to ensure data accuracy.
* **No Direct Access Required**: Connectors can be used without a live connection to the data, enabling distributed development of Data Warehouses.
