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

# Advanced Features

AnalyticsCreator provides a rich set of advanced features to help you configure, customize, and optimize your data warehouse projects. These features extend the tool’s capabilities beyond standard operations, enabling more precise control and flexibility.

***

#### **Scripts**

Scripts in AnalyticsCreator allow for detailed customization at various stages of data warehouse creation and deployment. They enhance workflow flexibility and enable advanced repository configurations.

**Types of Scripts**

1. **Object-Specific Scripts**
   * Define custom behavior for individual objects, such as tables or transformations, to meet specific requirements.
2. **Pre-Creation Scripts**
   * Execute tasks prior to creating database objects.
   * Example: Define SQL functions to be used in transformations.
3. **Pre-Deployment Scripts**
   * Configure processes that run before deploying the project.
   * Example: Validate dependencies or prepare the target environment.
4. **Post-Deployment Scripts**
   * Handle actions executed after deployment is complete.
   * Example: Perform cleanup tasks or execute stored procedures.
5. **Pre-Workflow Scripts**
   * Manage operations that occur before initiating an ETL workflow.
   * Example: Configure variables or initialize staging environments.
6. **Repository Extension Scripts**
   * Extend repository functionality with user-defined scripts.
   * Example: Add custom logic to redefine AnalyticsCreator repository objects.

***

#### **Historization**

The historization features in AnalyticsCreator enable robust tracking and analysis of historical data changes, supporting advanced time-based reporting and auditing.

**Key Components**

1. **Slowly Changing Dimensions (SCD)**
   * Automate the management of changes in dimension data.
   * Supports various SCD types, including Type 1 (overwrite), Type 2 (versioning), and more.
2. **Time Dimensions**
   * Create and manage temporal structures to facilitate time-based analysis.
   * Example: Build fiscal calendars or weekly rollups for time-series analytics.
3. **Snapshots**
   * Capture and preserve specific states of the data warehouse.
   * Use cases: Audit trails, historical reporting, and rollback points.

***

#### **Parameters and Macros**

These tools provide centralized control and reusable logic to optimize workflows and streamline repetitive tasks.

**Parameters**

* **Dynamic Management**: Centralize variable definitions for consistent use across scripts, transformations, and workflows.
* **Reusable Configurations**: Update values in one place to apply changes globally.
* **Use Cases**: Set default values for connection strings, table prefixes, or date ranges.

**Macros**

* **Reusable Logic**: Create parameterized scripts for tasks that need to be repeated across different projects or workflows.
* **Streamlined Processes**: Use macros to enforce consistent logic in transformations and custom calculations.
* **Example**: Define a macro to calculate age based on a birthdate and reference it across transformations.

Scripts in AnalyticsCreator enable precise customization for various stages of the data warehouse creation and deployment process. They provide flexibility to tailor workflows and extend repository functionality:

* **Object-Specific Scripts**: Define custom behavior for individual objects to meet specific requirements.
* **Pre-Creation Scripts**: Execute tasks before the creation of database objects.
* **Pre-Deployment Scripts**: Configure processes that run prior to deploying your project.
* **Post-Deployment Scripts**: Handle actions executed after deployment is complete.
* **Pre-Workflow Scripts**: Manage operations that occur before initiating workflows.
* **Repository Extension Scripts**: Extend repository capabilities with user-defined scripts for advanced customization.

**Historization**

Historization features in AnalyticsCreator help maintain and track changes in your data warehouse over time, enabling robust historical data analysis:

* **Slowly Changing Dimensions (SCD)**: Automate the management of changes in dimension data with support for various SCD types.
* **Time Dimensions**: Define and manage temporal structures to facilitate time-based analytics.
* **Snapshots**: Capture and preserve specific states of your data warehouse for auditing, reporting, or rollback purposes.

**Parameters and Macros**

Enhance flexibility and reusability across your projects:

* **Parameters**: Centralize and dynamically manage variables used across scripts and workflows.
* **Macros**: Create reusable logic to streamline repetitive tasks and ensure consistency.

These features provide a powerful set of tools to customize, optimize, and manage your data warehouse with precision and efficiency.



