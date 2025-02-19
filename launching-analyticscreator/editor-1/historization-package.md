# Historization package

This package is used to historicize data. One package can be used to define multiple historizations.&#x20;



{% hint style="info" %}
**Historicizing Data** refers to the process of tracking and **storing changes to data over time.** Instead of just storing the **current state of the data**, historicizing data ensures that previous versions or states of the data are preserved. This allows organizations to analyze how data has evolved over time, which is particularly useful for understanding trends, auditing, and reporting. In the context of a data warehouse, historicizing typically involves creating records that represent historical snapshots of data, including the valid periods for each record (e.g., valid from and valid to dates).
{% endhint %}

Below is a typical historization definition:

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

There are several options to customize historization:&#x20;

1. **Missing record behavior:** This parameter describes the behavior when the primary key is missing in the source table:
   1. **Close:** The validity period of the corresponding primary key in the historicized table will be closed, and the key will not exist in the actual data.
   2. **Add empty record:** The validity period of the corresponding primary key in the historicized table will be closed, and a new record containing the values defined in the "Empty value" column will be added. The key will remain in the actual data.
   3. **Do not close:** No action will be taken. The key will remain in the actual data.
2. **Insert only:** If this flag is set, no historicizing will occur. The source data will simply be added to the historicized table. This type of historization is only possible if the source has no primary key.
3. **Type:** You can select betthe documentationen different historization algorithms:&#x20;
   1. SSIS Package: Historization will be done using SSIS Package
   2. **Automatically created stored procedure**: Historization will be performed using an automatically generated stored procedure. You can view the procedure text in the **"Procedure"** tab. The procedure name is **\[CFG].\[HIST\_TableName]**, where **TableName** is the name of the historicized table. The procedure will be executed in the SSIS package.
   3. **Manually created stored procedure:** Historization will be done using a manually created stored procedure. You can modify the procedure text in the **"Procedure"** tab. The procedure name should always be **\[CFG].\[HIST\_TableName]**, where **TableName** is the name of the historicized table. The procedure will be executed in the SSIS package. You can set the historization algorithm to "Automatically created stored procedure" and click **"Save"** to generate the procedure, and then set the algorithm to "Manually created stored procedure" to modify the procedure text.
4. **Optional statement to calculate ValidFrom date:** The validation start date is usually the current timestamp, but the user can define an SQL statement to calculate it. The statement can contain the field names of the source. You can separately define the validation start date for new keys and for existing keys. The result of the statement should be of the type **date** or **datetime**.
5. Ins. Filter and Del. Filter:&#x20;
   1. **Insert Filter**: You can define an insert filter to restrict the source data that should be historicized.
   2. **Delete Filter**: You can define a delete filter to restrict the historicized data that can be "closed" in case of missing primary keys in the source.
6. SCDType: You can select the historization type for each field. Available options include:
   1. **None(SCD Type 0)** :The changes in this field will not be monitored, but if a new record is added to the historicized table, the actual value of this field will be stored.
   2. **SCD Type 1:** The changes in this field will be monitored, but the history of changes will not be stored. In case of changes, the actual historical value will be updated.
   3. **SCD Type 2** : The changes in this field will be monitored, and the history of changes will be stored. In case of changes, the validity period of the previous record will be closed, and the new record with the new value and validity period will be added.&#x20;
7. **Calculated columns:** You can define calculated columns and use the previous and actual values in the calculation statement. For example, to calculate stock changes, the user can use the following statement:\
   `ISNULL(I.Amount, 0) - ISNULL(S.Amount, 0)`\
   &#x20;**\[I]** is the alias for the actual values, and **\[S]** is the alias for the previous values.
8. **SSIS variables:** You can define SSIS variables and set expressions to calculate their values. These variables can be used to define filters. To address a variable in a filter, use the `@` prefix (e.g., **@VariableName**). The values of these variables can be set using the **SSIS\_Configuration** table.
9. **Scripts:** You can define SQL scripts that will be executed before or after historization. To do this, use the **"Scripts"** tab.
