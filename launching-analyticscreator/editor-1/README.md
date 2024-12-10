---
noIndex: true
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

# AnalyticsCreator Reference guide

The **AnalyticsCreator** is the central storage location for all **metadata** related to your data warehouse projects. It serves as the foundation for organizing and managing the various elements of a data warehouse, ensuring consistency, scalability, and efficient collaboration across teams.

### **What is the AnalyticsCreator Repository?**

The repository stores all database **metadata** information, including details about data sources, transformations, layers, and configurations. It is designed to act as a centralized structure where users can:

* Define and manage data warehouse artifacts.
* Configure and store database objects and workflows.
* Organize elements into logical folders for better accessibility.

While the repository encompasses all **metadata**, not every item within it needs to be actively used, allowing flexibility in managing large and complex projects.

***

#### **Repository Structure**

The repository is organized into folders, with each folder representing a specific **Data Warehouse artifact** or **database object**. These objects include but are not limited to:

1. **Connectors**: Configurations for connecting to external data sources like MSSQL, Oracle, or SAP.
2. **Layers**: Hierarchical structures for organizing data, such as staging, core, and data marts.
3. **Packages**: Collections of related objects or configurations for deployment.
4. **Indexes**: Structures to improve query performance by optimizing data retrieval.
5. **Roles**: Access controls and permissions for users interacting with the data warehouse.
6. **Galaxies, Hierarchies, Partitions, and Parameters**: Components used in data modeling to define relationships, subsets, and configurations.
7. **Macros and Scripts**: Reusable logic and code snippets for data transformations and operations.
8. **Object Scripts**: Scripts tied to specific data objects for precise customizations.
9. **Filters**: Tools for selecting or excluding specific data based on defined conditions.
10. **Predefined Transformations**: Built-in processes to streamline common data processing tasks.
11. **Snapshots**: Static copies or versions of data at specific points in time for auditing or rollback purposes.
12. **Deployments**: Configurations and workflows for deploying changes to the data warehouse.
13. **Groups**: Logical groupings of related objects or users for better management.
14. **Models**: Representations of the structure and relationships within the data warehouse.

***

#### **Types of Repositories**

AnalyticsCreator supports three types of repositories, offering flexibility in storage and collaboration:

1. **SQL Server Repository**
   * Stored in Microsoft SQL Server databases.
   * Ideal for centralized storage and multi-user collaboration in larger projects.
2. **Local File Repository**
   * Stored locally on your system.
   * Suitable for individual users or small-scale projects requiring minimal setup.
3. **AnalyticsCreator Cloud Repository**
   * A cloud-based storage solution.
   * Enables seamless collaboration and remote access, making it ideal for distributed teams.

{% hint style="info" %}
Both the **SQL Server Repository** and **Cloud Repository** are essentially Microsoft SQL Server databases with a predefined schema to store all AnalyticsCreator metadata. No additional software is required for setup.
{% endhint %}

***

#### **Key Benefits of the Repository**

1. **Centralized Management**
   * All metadata is stored in one location, ensuring consistency and reducing redundancy.
2. **Scalability**
   * Supports projects of all sizes, from small, local setups to large, multi-user cloud environments.
3. **Flexibility**
   * Allows users to organize, customize, and manage artifacts based on project requirements.
4. **Collaboration**
   * With SQL Server or Cloud repositories, teams can work collaboratively on shared projects.

***

#### **Best Practices for Using the Repository**

* **Organize Folders**: Group objects logically to reflect the structure and purpose of your data warehouse.
* **Use Appropriate Types**: Select the repository type that best suits your project scale and team collaboration needs.
* **Regular Backups**: For SQL Server and local repositories, ensure regular backups to prevent data loss.
* **Optimize Performance**: Use indexes, filters, and partitions effectively to manage large datasets efficiently.
* **Version Control**: Keep track of changes and maintain versioning to facilitate rollback if necessary.

***

The AnalyticsCreator Repository is a robust and versatile solution for managing metadata, enabling you to build scalable and efficient data warehouses. Its flexibility across storage types and comprehensive feature set make it a cornerstone of AnalyticsCreator's functionality. Let me know if you'd like further enhancements!\






