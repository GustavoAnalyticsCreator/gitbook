# Import package

This package is used to import data from external data sources.&#x20;

A single package can be used to define multiple imports.&#x20;

Below is a typical import definition:

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

Import package Proprieties:

1. **Fields**: Defines the mapping between the source and target fields and specifies the SSIS statements for the import fields.
2. **SSIS Variables**: Allows the definition of variables, expressions to calculate variable values, and settings for these values using the **`SSIS_Configuration`** table. These variables are used to define filters.
3. **Filter**: Defines filters to restrict the data being imported. SSIS variables are used in filters, with the “@” character serving as the variable identifier (e.g., `@Date`).
4. **Scripts** (Tab): Defines SQL scripts that are executed before or after the data import process.
5. **ImpSQL**: Redefines the SQL command used for importing data.
6. **Update Statistics**: Selecting this checkbox launches the `UPDATE STATISTICS` command after the import process is completed.
7. **Manually Created**: Selecting this checkbox indicates the SSIS package is manually created or modified. If selected, the package is not generated during deployment but is added to the workflow.
8. **Use Logging**: If enabled, log information about the package execution is stored in the DWH log tables.
9. **Externally Launched**: If selected, the package is excluded from the workflow and must be launched manually.
