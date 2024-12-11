# Scripts

Scripts are the set of SQL commands which will be launched under certain conditions.

There are 4 types of scripts:&#x20;

1. Pre-Deployment script – this script will be launched prior to DWH synchronization and prior to deployment.&#x20;
2. Post-Deployment script – this script will be launched after to DWH synchronization and prior to deployment.&#x20;
3. Pre-Workflow script – this script will be launched in workflow package prior to start all other packages.&#x20;
4. Pre-Workflow script – this script will be launched in workflow package after all other packages are finished.

The deployment script can be disabled during synchronization or deployment by using the **“Do Not Deploy”** and **“Do Not Synchronize”** flags. Below is a typical script definition:

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

**Pre** **and** **Post-deployment** **scripts** can be utilized to create stored procedures for use in transformations. In this scenario, the script should be executed only during Data Warehouse (DWH) synchronization.&#x20;

It is unnecessary to include the `CREATE PROCEDURE` script during deployment, as the procedure definition is already included in the deployment package.
