---
description: >-
  The Adventure Works database is a sample database originally developed by
  Microsoft. It simulates a fictional company, providing a comprehensive schema
  for business operations and processes.
noIndex: true
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Adventure Works Data Warehouse

###

<mark style="background-color:orange;">**###RECORD A VIDEO##**</mark>



In this step, you'll configure and deploy your project to the desired destination. **Please note that only the metadata will be deploye**&#x64;**; there will be no data movement or copy during this process.**\
\
Follow the instructions below to create and set up a new **deployment**.

1. Navigate to **Deployments** in the menu and create a new deployment.&#x20;
2. Assign a name to your deployment.&#x20;
3. Configure the connection for the **Destination**.&#x20;
4. Set the project path where the deployment will be saved.&#x20;
5. Select the packages you want to generate.&#x20;
6. Review the connection variables and click **Deploy** to initiate the process. Finally, click Deploy to complete the deployment.
7. Finally, click **Deploy** to complete the deployment.

{% embed url="https://www.analyticscreator.com/hubfs/My%20first%20Deploy.mp4" %}

In this step, your initial Data Warehouse project is created. Note that only the metadata—the structure of your project—is generated at this stage. You can choose between two options for package generation: [**SSIS** (SQL Server Integration Services) ](https://learn.microsoft.com/pt-br/sql/integration-services/sql-server-integration-services?view=sql-server-ver16)or [**ADF** (Azure Data Factory)](https://learn.microsoft.com/en-us/azure/data-factory/introduction), or both.

SSIS follows a traditional ETL tool architecture, making it a suitable choice for on-premises data warehouse architectures. In contrast, ADF is designed with a modern cloud-native architecture, enabling seamless integration with various cloud services and big data systems.&#x20;

This architectural distinction makes ADF a better fit for evolving data integration needs in cloud-based environments.

To execute your package and move your data, you will still need an **Integration Runtime (IR)**. Keep in mind that AnalyticsCreator only generates the project at the metadata level and does not access your data outside the AnalyticsCreator interface. It does not link your data to us, ensuring that your data remains secure in its original location.

For testing purposes, you can run your package in [Microsoft Visual Studio 2022](https://visualstudio.microsoft.com/#vs-section), on your local SQL Server, or even in Azure Data Factory

