---
noIndex: true
icon: plug
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

### Adding a New Connector

**Breadcrumb:**\
`Toolbar -> Sources -> Connectors`\
`Navigation-tree -> Connectors -> right-click -> Add Connector`

To add a new connector:

1. Navigate to the **Connectors** section in the navigation tree.
2. Right-click on **Connectors** and select **"Add Connector"**.
3. Provide a name in the **Connector Name** field.
4. Choose a **Connector Type** from the dropdown list (e.g., MSSQL, Oracle, CSV).
5. Use the **Template** button to view and edit the connection string template. Replace placeholders (e.g., `[SERVER]`, `[DATABASE]`) with your data source details.
6. Click **Test Connection** to validate the connection.
7. Save your connector configuration by clicking **Save**.

<mark style="background-color:orange;">**Place the image here**</mark>

### Importing Connectors

**From AnalyticsCreator Cloud**

**Breadcrumb:**\
`Toolbar -> Sources -> Import from Cloud`\
`Navigation-tree -> Connectors -> right-click -> Import Connector from Cloud`

1. Right-click on **Connectors** and select **"Import Connector from Cloud"**.
2. Choose a connector from the available list.
3. Once imported, you can use the connector for your projects.

<mark style="background-color:orange;">**Place the image here**</mark>

### **From a File**

**Breadcrumb:**\
`Toolbar -> Sources -> Import from File`\
`Navigation-tree -> Connectors -> right-click -> Import Connector from File`

1. Right-click on **Connectors** and select **"Import Connector from File"**.
2. Browse for the file, select it, and click **OK**.

<mark style="background-color:orange;">**Place the image here**</mark>

***

### Exporting Connectors

**To AnalyticsCreator Cloud**

1. Right-click on the specific connector in the **Connectors** list.
2. Select **Export Connector to Cloud**.
3. Provide a name for the connector and click **OK** to save it to AC-Cloud.

<mark style="background-color:orange;">**Place the image here**</mark>

**To a File**

1. Right-click on the specific connector in the **Connectors** list.
2. Select **Export Connector to File**.
3. Specify the file name and save the connector.

<mark style="background-color:orange;">**Place the image here**</mark>

#### Additional Features

* **Refresh Connectors**: Update metadata for existing connectors to ensure data accuracy.
* **Edit and Manage Connectors**: Use the **Navigation Tree** to list, search, edit, or delete connectors.
* **No Direct Access Required**: Connectors can be used without a live connection to the data, enabling distributed development of Data Warehouses.

{% hint style="info" %}
If your data source is not supported, you can use the **Externally Filled Tables** feature as a workaround.
{% endhint %}

