# Scripts

Scripts are the set of SQL commands which will be launched under certain conditions. There are 4 types of scripts: Pre-Deployment script – this script will be launched prior to DWH synchronization and prior to deployment. Post-Deployment script – this script will be launched after to DWH synchronization and prior to deployment. Pre-Workflow script – this script will be launched in workflow package prior to start all other packages. Pre-Workflow script – this script will be launched in workflow package after all other packages are finished.

You can disable the deployment script during the synchronization or during deployment using “Do not deploy” and “Do not synchronize” flags. Typical script definition:

You can use the pre- and post-deployment scripts to create stored procedures which you will use in transformations. In this case you should run the user's script during the DWH synchronization only – you don’t have to use the CREATE PROCEDURE script during deployment because the procedure definition already exists in deployment package.
