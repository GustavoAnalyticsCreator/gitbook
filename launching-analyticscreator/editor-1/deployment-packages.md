# Deployment packages

Multiple deployment packages can be created to manage different deployment configurations. Each deployment package is a Visual Studio solution containing the necessary elements required to deploy the data warehouse.&#x20;

Below is a typical description of a deployment package:

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

**Deployment Package Properties**

1. **Name**: The name of the deployment package and the generated Visual Studio solution.
2. **Create DACPAC**: If checked, the DACPAC file containing the DWH structure will be generated.
3. **Deploy DACPAC**: If checked, the DACPAC file will be deployed to the database defined below.
4. **Server, DB Name, Integrated Security, Login, and Password**: Connection attributes of SQL Server to which the DACPAC file should be deployed.
5. **Deployment Options**:
   1. **Allow Data Loss**
   2. **Drop Objects Not in Source**
   3. **Backup DB Before Changes**
   4. **Block When Drift Detected**
   5. **Deploy in Single User Mode**
   6. **Allow Incompatible Platform**\
      These options control how the DACPAC is deployed. See [SQLDEPLOY.EXE ](https://learn.microsoft.com/en-us/sql/integration-services/devops/ssis-devops-standalone?view=sql-server-ver16#ssisdeployexe)options for more information.
6. **Create Power Pivot**: If checked, the Excel file containing the Power Pivot/Power BI semantic model will be created. This Power Pivot file can be imported into Power BI.

**Next options are common for Multidimensional and Tabular OLAP databases:**

7. **Create XMLA File**: If checked, the XMLA file containing the OLAP database definition will be created.
8. **Server, DB Name, Login, Password**: Connection attributes of the OLAP server where the OLAP database will be deployed. Dummy information can be added here, but the XMLA file should be edited to replace it with the correct server credentials.
9. **Process Cube in Workflow Package**: If checked, the cube processing task will be added to the workflow package.
10. **Create Cube During Deployment**: If checked, the OLAP cube will be created using the OLAP server connection attributes.
11. **SSIS Packages**: SSIS packages that will be generated during deployment. To invert the selection, click on the header of the **"Deploy"** column in the package list.
12. **SSIS Config Type**: Choose between an environment variable and a config file to configure the connection to the database containing the **\[CFG].\[SSIS\_Configuration]** table. This table holds the configurations for all SSIS packages.
13. **SSIS Config Env. Var./SSIS Config File Path**: The name of the environment variable or the path to the config file that will be created.
14. **Deploy SSIS\_Configuration**: If checked, the content of the **\[CFG].\[SSIS\_Configuration]** table will be recreated.
15. **Use Project Reference**: If selected, the workflow package will access other SSIS packages using a project reference. Otherwise, it will use a file reference.
