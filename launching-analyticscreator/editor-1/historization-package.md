# Historization package

This package will be used to historicize data. One package can be used to define many historization.&#x20;

There is a typical historization definition:

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

There are several options to customize historization:&#x20;

1. **Missing record behavior:** This parameter describes what happens If the primary key is missing in the source table
   1. **Close:** The validity period of according primary key in the historicized table will be closed. The key will be missed in the actual data.&#x20;
   2. **Add empty record:** The validity period of according primary key in the historicized table will be closed. A new record containing the values defined in “Empty value” column will be added. The key will exist in the actual data.&#x20;
   3. **Do not close:** Do nothing. The key will exist in the actual data.&#x20;
2. **Insert only:** If flag is set, no historicizing will happen, the source data will be just added to the historicized table. This kind of historization is only possible if the source has no primary key.
3. **Type:** You can select betthe documentationen different historization algorithms:&#x20;
   1. SSIS Package: Historization will be done using SSIS Package
   2. Automatically created stored procedure. Historization will be made using automatically generated stored procedure. You can see the procedure text in the tab “Procedure”. The procedure name \[CFG].\[HIST\_TableName] where the TableName is the name of historicized table. The procedure will be launched in SSIS Package.&#x20;
   3. Manually created stored procedure. Historization will be done using stored manually created procedure. You can change the procedure text in the tab “Procedure”. The procedure name should be always \[CFG].\[HIST\_TableName] where the TableName is the name of historicized table. The procedure will be launched in SSIS package. You can set the historization algorithm to “Automatically created stored procedure” and click on “Save” to generate the procedure and then set algorithm to ”Manually created stored procedure” and change the procedure text.&#x20;
4. Optional statement to calculate ValidFrom date: Usually the validation start date is the current timestamp but the user can define the SQL statement to calculate it. The statement can contain the field names of the source. You can separately define the validation start date for the new keys and for the existing keys. The result of the statement should be of the type date or datetime.&#x20;
5. Ins. Filter and Del. Filter: You can define the filters to restrict the data you will historicize. You can define the “insert filter” to restrict the source data which should be historicized. You can define the “delete filter” to restrict the historicized data which can be “closed” in case of the missing primary keys in source.&#x20;
6. SCDType: You can decide for every field, which historization type should be used. You can select between the following historization types:&#x20;
   1. **None(SCD Type 0)** – the changes of this field will be not monitored but if the new record will be added to the historicized table, the actual value of this field will be stored.&#x20;
   2. **SCD Type 1** – the changes of this field will be monitored but the history of changes will not be stored. In case of changes the actual historical value will be updated.&#x20;
   3. **SCD Type 2** – the changes of this field will be monitored and the history of changes will be stored. In case of changes the validity period of previous record will be closed and the new record with the new value and new validity period will be added.&#x20;
7. **Calculated columns:** You can define the calculated columns and use the previous and actual values in calculation statement. For example, to calculate the stock changes the user can use the following statement: ISNULL(I.Amount, 0) - ISNULL(S.Amount, 0) \[I] is alias for the actual values, \[S] is alias for the previous values.&#x20;
8. **SSIS variables:** You can define the SSIS variables. You can define expression to calculate the variable value and the user can set the variable value using SSIS\_Configuration table. These variables the user can use to define filters. To address a variable in filter please use @-prefix (@VariableName). Scripts: You can define SQL&#x20;
9. **Scripts:** which will be executed before or after historization. To do that use the “Scripts” tab.
