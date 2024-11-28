---
noIndex: true
icon: octopus-deploy
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Deployments

#### **Deployments in AnalyticsCreator**

**Breadcrumb:**\
Toolbar → Deployment → Deployment Package\
Navigation Tree → Deployments → Add Deployment\
Navigation Tree → Deployments → Deployment → Edit Deployment

***

#### **What is a Deployment?**

Deployments in AnalyticsCreator are the processes of applying changes or publishing your data warehouse structure and configurations to the target system. Deployments ensure that your data warehouse is up to date with the latest definitions, including layers, transformations, scripts, and other metadata.

***

#### **How to Add a Deployment**

**1. Create a New Deployment**

1. Navigate to the **navigation tree** and right-click **Deployments**, then select **Add Deployment**.
2. In the **Deployment Name** box, provide a meaningful name for the deployment package.
3. In the **Description** box, describe the deployment package, including its purpose or the specific updates it contains.

**2. Configure Deployment Details**

* **Target Connection**: Define the connection to the target database where the deployment will be executed.
* **Scripts and Packages**: Include specific pre- and post-deployment scripts, if required, to customize the deployment process.
* **Layer Selection**: Specify the layers or objects to be included in the deployment, such as facts, dimensions, or specific tables.

**3. Save and Execute**

* Click the **Save** button to store the deployment package.
* Use the **Run Deployment** option to execute the deployment on the target system.

***

#### **Managing Deployments**

1. **List and Search**: View all deployment packages in the repository from the **Deployments** section in the navigation tree.
2. **Edit Deployment**: Update the deployment configuration by selecting a package and clicking **Edit Deployment**.
3. **Delete Deployment**: Remove outdated deployment packages to maintain a clean repository.

***

#### **Video Tutorial**

For a detailed walkthrough of the deployment process, watch the official video tutorial:\
[Deployment of a Data Warehouse](https://www.youtube.com/watch?v=2RYms4nn3J4)

***

#### **Best Practices for Deployments**

1. **Plan Ahead**: Ensure that all required changes are finalized before creating a deployment package.
2. **Test Scripts**: Always validate pre- and post-deployment scripts in a test environment to prevent errors during execution.
3. **Organize by Layers**: Deploy individual layers or objects incrementally for better control and troubleshooting.
4. **Version Control**: Keep a record of deployment packages to track changes and facilitate rollback if needed.

Deployments are a critical step in ensuring your data warehouse is properly synchronized with the latest configurations. By following these steps and best practices, you can streamline the deployment process and maintain a robust and reliable data warehouse.
