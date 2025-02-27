# Scripts

Scripts are a set of SQL commands that will be executed under specific conditions. There are four types of scripts:

1. **Pre-Deployment Script**: This script is executed prior to DWH synchronization and before deployment.
2. **Post-Deployment Script**: This script is executed after DWH synchronization and before deployment.
3. **Pre-Workflow Script**: This script is executed in the workflow package before starting all other packages.
4. **Post-Workflow Script**: This script is executed in the workflow package after all other packages have finished.

**Deployment Script Control**\
The deployment script can be disabled during synchronization or deployment by using the **"Do Not Deploy"** and **"Do Not Synchronize"** flags.\
Below is a typical script definition:

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

**Pre and Post-Deployment Scripts for Stored Procedures**\
Pre and Post-deployment scripts can be used to create stored procedures for use in transformations. In this case, the script should be executed only during Data Warehouse (DWH) synchronization.\
Including the **CREATE PROCEDURE** script during deployment is unnecessary, as the procedure definition is already included in the deployment package.
