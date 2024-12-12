# Deployment packages

Multiple deployment packages can be created to manage different deployment configurations.

Each deployment package is a Visual Studio solution containing the necessary elements required to deploy the data warehouse. Below is a typical description of a deployment package:

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

**Deployment packages** **Proprieties**

1. **Name:** The name of deployment package and the name of generated the visual studio solution.
2. **Create DACPAC:** If checked, the DACPAC file containing WDH structure will be generated&#x20;
3. Deploy DACPAC: If checked, the DACPAC file will be deployed to the database defined below.
4. Server, DB Name, Integrated security, Login and Password: the connection attributes of SQL Server the DACPAC file should be deployed to.&#x20;
5. Allow data loss, Drop objects not in source, Backup DB before changes, Block when drift detected, Deploy in single user mode and Allow incompatible platform: the DACPAC deployment options. \
   See SQLDEPLOY.EXE options for more information.&#x20;
6. Create Power Pivot: if checked, the Excel file containing Power Pivot/Poth Power BI BI semantic model will be created. This Power Pivot file can be imported into Power BI

&#x20;**Next options are common for Multidimensional and Tabular OLAP databases**

1. Create XMLA file: if checked, the XMLA file containing OLAP database definition will be created
2. Server, DB Name, Login, Password: Connection attributes of OLAP Server where the OLAP database will work. You can add there a dummy information but then you should edit the XMLA file and replace the dummy data with the properly server credentials.&#x20;
3. Process cube in workflow package: if checked, the cube processing task will be added to workflow package&#x20;
4. Create cube during deployment: if checked, the OLAP cube will be created using OLAP server connection attributes. SSIS Packages: SSIS packages which will be generated during deployment. To invert the selection please click on the header of “Deploy” – column in the package list.&#x20;
5. SSIS config type: You can select between the environment variable and config file to configure the connection to the database containing `[CFG].[SSIS_Configuration]` table. This table contains the configurations of all SSIS packages.&#x20;
6. SSIS Config env.var./SSIS config file path: Name of environment variable or path to the config file which will be created.&#x20;
7. Deploy SSIS\_Configuration: if checked, the content of `[CFG].[SSIS_Configuration]` table will be recreated.&#x20;
8. Use project reference: if selected, the workflow package will access other SSIS packages using project reference, otherwise –using file reference.
