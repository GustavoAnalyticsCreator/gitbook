---
icon: server
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

# Packages detailed

### **Import Packages**

### The package is used to import data from external data sources. A single package can define multiple imports. Below is a typical import definition:

#### **Customizing Data Import in AnalyticsCreator**

AnalyticsCreator supports both SSIS (SQL Server Integration Services) and Azure Data Factory for data import, offering flexibility to adapt to different environments. Several options are provided to customize the import process, allowing tailored configurations to meet specific requirements.

1. **Fields**:
   * The mapping between source and target fields can be defined.
   * Statements for processing fields during import are specified.
2. **Variables**:
   * Variables are defined to manage dynamic values during the import process.
   * Expressions are used to calculate variable values or set them using configuration tables.
   * Variables are utilized to define filters for imports.
3. **Filters**:
   * Filters are defined to restrict imported data.
   * Variables are leveraged in filters using the “@” character as the variable identifier (e.g., `@Date`).
4. **Scripts**:
   * SQL scripts are defined to execute before or after the data import process.
   * Scripts are used to prepare data or handle post-import tasks.
5. **Custom SQL Commands**:
   * The SQL command used to import data is redefined by providing a custom query.
6. **Update Statistics**:
   * The **Update Statistics** checkbox is selected to execute the `UPDATE STATISTICS` command after the import is completed.
7. **Manually Created**:
   * This checkbox is selected if the package is manually created or modified.
   * When selected, the package is not automatically generated during deployment but is included in the workflow.
8. **Use Logging**:
   * This option is enabled to store log information about the package execution in the Data Warehouse (DWH) log tables.
9. **Externally Launched**:
   * This checkbox is selected to exclude the package from the workflow.
   * In this case, the package must be launched manually.
10. **Azure Data Factory Support**:
    * When Azure Data Factory is utilized, similar configurations are defined to set up pipelines for importing data from external sources.
    * ADF integration allows operations with various cloud-based and big data systems, complementing the capabilities of SSIS for cloud-native architectures.

These options provide extensive control over the data import process, ensuring flexibility in both on-premises and cloud-based workflows.

### **Historization Packages**

### This package is used to historicize data. A single package can define multiple historization processes. Below is a typical definition of historization:

#### **ustomizing Historization in AnalyticsCreator**

AnalyticsCreator provides extensive options to customize the historization process, allowing flexibility in managing historical data. Below are the key configuration options:

**1. Missing Record Behavior**

This parameter determines how missing primary keys in the source table are handled:

* **Close**: The validity period for the corresponding primary key in the historicized table is closed, and the key is excluded from the current data.
* **Add Empty Record**: The validity period is closed, but a new record with values from the “Empty Value” column is added, ensuring the key remains in the current data.
* **Do Not Close**: No changes are made, and the key remains in the current data.

***

**2. Insert Only**

* If this flag is enabled, the source data is simply added to the historicized table without any historization.
* This option is suitable only when the source table does not have a primary key.

***

**3. Type**

Select the algorithm for performing historization:

* **SSIS Package**: Historization is executed through an SSIS package.
* **Automatically Created Stored Procedure**:
  * A stored procedure is generated automatically and executed via SSIS.
  * The procedure name is `[CFG].[HIST_TableName]`, where `TableName` represents the historicized table name.
* **Manually Created Stored Procedure**:
  * A custom stored procedure is created and edited manually.
  * The procedure name must be `[CFG].[HIST_TableName]` and is executed via SSIS.
  * To customize: First set the algorithm to "Automatically Created Stored Procedure," generate the procedure, save it, and then switch to "Manually Created Stored Procedure" to edit the text.

***

**4. ValidFrom Date Calculation**

* The default start date for validity is the current timestamp.
* SQL statements can be defined to calculate the `ValidFrom` date for both new and existing keys.
* The statement should return a value of type `date` or `datetime`.

***

**5. Filters**

* **Insert Filter**: Restricts the source data to be historicized.
* **Delete Filter**: Restricts historicized data eligible for closing due to missing primary keys in the source.

***

**6. Slowly Changing Dimension (SCD) Types**

Define the historization type for each field:

* **None**: Changes are not monitored, but new records store the current field value.
* **SCD1**: Changes are monitored, but no history is stored. The current value is updated in case of changes.
* **SCD2**: Changes are monitored, and history is preserved. The previous record’s validity period is closed, and a new record is added with the updated value and validity period.

***

**7. Calculated Columns**

* Calculated columns allow computations based on current and previous values.
*   Example: To calculate stock changes, use:

    ```sql
    ISNULL(I.Amount, 0) - ISNULL(S.Amount, 0)
    ```

    * `I` refer to current values, and `S` refers to previous values.

***

**8. SSIS Variables**

* Define SSIS variables to handle dynamic values.
* Expressions can calculate variable values, and the `SSIS_Configuration` table is used for setting values.
* Variables can also be referenced in filters using the `@` prefix (e.g., `@VariableName`).

***

**9. Scripts**

* SQL scripts can be defined to execute before or after historization.
* Use the **Scripts** tab to add these scripts, providing additional customization.

***

These customizable options offer robust tools for implementing tailored historization processes, enabling efficient management of historical data and meeting specific project needs.

* If this flag is enabled, the source data is simply added to the historicized table without any historization.
* This option is suitable only when the source table does not have a primary key.

***

**Persisting Package**

* This package is utilized to persist transformations within the data warehouse.
* **Configuration Options**: There are no options available for customization.

***

**Script Launching Package**

* This package is designed to execute script transformations.
* **Configuration Options**: There are no options available for customization.

***

**Workflow Package**

* This package is responsible for orchestrating and launching all other packages in the correct execution order.
* **Configuration Options**: There are no options available for customization.
