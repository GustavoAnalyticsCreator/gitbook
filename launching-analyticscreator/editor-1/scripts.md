---
noIndex: true
icon: square-code
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

# Scripts

**Use of Scripts**

Scripts are used to extend the functionality of your data warehouse. They allow you to execute custom SQL or other actions at different points in the data warehouse lifecycle.

#### Add a Script

1. In the **navigation tree**, right-click the **Pre-creation scripts** folder and click **Add Pre-creation script**. You can perform the same action for other types of scripts in their respective folders:
   * Post-creation scripts
   * Pre-deployment scripts
   * Post-deployment scripts
   * Pre-workflow scripts
   * Post-workflow scripts
   * Repository extension scripts
2. In the **Script type** list, select the type of script you want to add.
3. In the **Name** box, enter the name of the script.
4. In the **Description** box, type a description of the script.

**Script Options:**

| Option              | Description                                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Sequence number** | Defines the launch order of the scripts (e.g., 1, 2, 3…). Important when multiple scripts are defined.                         |
| **Inactive**        | Allows you to deactivate specific scripts using this checkbox.                                                                 |
| **Package**         | Relevant for Pre-workflow and Post-workflow scripts. You can select workflow packages where specific scripts will be launched. |
| **Run**             | If checked, the specific script will be executed as part of a specific workflow package.                                       |

**Script Types:**

* **Pre-creation scripts**: Executed before the data warehouse database is created. Used for defining SQL functions for transformations.
* **Post-creation scripts**: Executed after the database is created. Used for defining stored procedures or performing custom actions on the data warehouse.
* **Pre-deployment scripts**: Included in the DACPAC file as pre-deployment scripts, useful for user-specific deployment actions.
* **Post-deployment scripts**: Included in the DACPAC file as post-deployment scripts for user-specific deployment actions.
* **Pre-workflow scripts**: Executed before the ETL process starts in the workflow package.
* **Post-workflow scripts**: Executed after the ETL process finishes in the workflow package.
* **Repository extension scripts**: Used to extend or redefine the functionality of the AnalyticsCreator repository.

#### List, Search, Delete Scripts

For managing scripts, you can refer to the List and Search Objects section for more information.
