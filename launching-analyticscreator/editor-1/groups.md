---
noIndex: true
icon: object-intersect
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

# Groups

**Breadcrumb:**\
Diagram → \[Source] → Object Groups\
Diagram → \[Table] → Object Groups\
Diagram → \[Transformation] → Object Groups

***

#### **What Are Groups?**

Groups in AnalyticsCreator are subsets of repository objects, such as sources, tables, and transformations, that are logically connected and dependent on each other.

Groups simplify working with large repositories by organizing hundreds or thousands of objects into manageable units. Once a group is created, you can filter diagrams to display only the objects within a selected group.

***

#### **Key Features of Groups**

* **Subset Management**: Organize related repository objects into logical groups for easier management.
* **Dependency Inheritance**: Include objects that are dependent on or are depended upon by a selected object.
* **Diagram Filtering**: Filter diagrams by groups to focus on specific subsets of objects.
* **ETL Configuration**: Generate workflow configurations for ETL processes that only process specific groups of objects.

***

#### **Adding an Object to a Group**

**1. Open the Groups Window**

1. In the **Diagram**, right-click a **Source**, **Table**, or **Transformation** object.
2. Select **Object Groups** from the context menu.
   * The **Groups** window will appear.

**2. Set Group Properties**

Configure the group properties in the **Groups** window.

| Property                              | Description                                                                                             |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Member**                            | If checked, the object becomes a member of the selected group.                                          |
| **Inherit Predecessors**              | Includes all objects that the selected object depends on.                                               |
| **Inherit Successors**                | Includes all objects that depend on the selected object.                                                |
| **Inherited**                         | Read-only. Indicates if the object is included in the group due to dependency inheritance.              |
| **Exclude**                           | Explicitly excludes a dependent object from the group.                                                  |
| **Name**                              | Name of the group.                                                                                      |
| **Description**                       | Description of the group.                                                                               |
| **Create Workflow**                   | Generates a SQL file during deployment to configure ETL tasks to process only the objects in the group. |
| **SSIS Configuration**                | Name of the SQL file containing the `CFG.SSIS_Configuration` table for the group.                       |
| **SSIS Configuration Enable Script**  | Name of the SQL file enabling the processing of objects in the group.                                   |
| **SSIS Configuration Disable Script** | Name of the SQL file disabling the processing of objects in the group.                                  |
| **Inherit from Objects**              | Read-only. Displays the parent object for inherited objects.                                            |
| **Locked By**                         | Name of the user who locked the group.                                                                  |

**3. Lock or Unlock the Group**

* Use the **Lock** button to lock the group for exclusive editing. Only the lock owner can edit the group while it is locked.
* Use the **Unlock** button to release the lock for shared editing.

**4. Save the Group**

* Press the **Save** button to finalize the group definition.

***

#### **Working with Groups**

**Filtering Diagrams by Groups**

After creating a group, you can select it in the toolbar. Only members of the selected group will be displayed in the diagram, making it easier to focus on specific subsets of the repository.

***

#### **Best Practices for Groups**

1. **Logical Organization**: Group objects based on functionality or dependencies to simplify navigation and management.
2. **Use Dependency Inheritance**: Enable inheritance of predecessors and successors to automatically include related objects.
3. **Lock for Consistency**: Lock groups during edits to avoid conflicts in multi-user environments.
4. **Optimize ETL Workflows**: Leverage group-based workflows for efficient and targeted ETL processing.

***

Groups are an essential tool in AnalyticsCreator for managing complex repositories, enabling focused work on subsets of objects, and streamlining ETL tasks. By effectively using groups, you can enhance the organization, clarity, and efficiency of your data warehouse workflows.

4o
