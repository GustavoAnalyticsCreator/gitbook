---
noIndex: true
icon: user-tie
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

# Roles

This feature enhances the flexibility of your data warehouse by allowing you to deploy each layer to different databases. It is particularly useful for scenarios where you need to optimize storage, ensure high availability, or separate data across multiple environments.

If you're working with multiple databases, ensure you follow the above steps to correctly set up and deploy the layers for your DWH.

## **Steps to Deploy Layers into Different Databases**

**1. Enable Separate Databases**

To begin, you must enable the deployment option that allows using separate databases for storing each layer of the DWH.

* Go to AnalyticsCreator and select the option **"Allow using separate databases to store layers"** in the deployment settings.

**2. Customize Layer Variables**

Next, you need to define the names of the SQLCMD variables for each layer. These variables will determine which database each layer is deployed to.

* By default, the SQLCMD variable is named `$(MAIN_DWH_DB)`. You can change the variable names to match your desired database configurations for each layer.

**3. Additional Dacpac File**

If you change the name of a layer variable, AnalyticsCreator will generate an additional `.dacpac` file named `{DWHNAME_VARIABLENAME}`. This file will ensure that all objects in the DWH are created using the correct SQLCMD variable for the specific layer.

Example:

**4. Deployment with SQLPACKAGE.EXE**

When deploying to separate databases, you cannot directly deploy `.dacpac` files from AnalyticsCreator. Instead, use the **SQLPACKAGE.EXE** utility to deploy the `.dacpac` files while setting the values of the layer variables using the `/variable` option.

This allows for a dynamic deployment process where the appropriate layer is deployed to the designated database.

***

**5. Azure SQL Server Limitations**

Please note that this feature is not yet available for deployment to **Azure SQL Server databases**.

***

**6. Config-Script Changes**

The **Config-Script** that populates the `CFG.SSIS_Configuration` table now uses the names of the layer-specific SQLCMD variables. This enables the configuration script to dynamically reference the correct database for each layer.

* To execute Config-Scripts, use **SQLCMD mode** in SQL Server Management Studio (SSMS).

To run the script in SQL Server Management Studio, enable **SQLCMD Mode**:

