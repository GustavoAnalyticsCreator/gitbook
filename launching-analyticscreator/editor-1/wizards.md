# Wizards

The Wizards in AnalyticsCreator provide a guided and efficient way to perform various tasks related to building and managing a data warehouse. Below is an overview of the eight available wizards and their functions:

#### **1.** [**DWH Wizard**](dwh-wizard.md)

The **DWH Wizard** is designed to quickly create a semi-ready data warehouse. It is particularly effective when the data source has defined table references or manually maintained references.\
**Key Features**:

* Supports various architectures: Classic (Kimball), Data Vault 1 and 2, or mixed.
* Automatically creates imports, dimensions, facts, hubs, satellites, and links.
* Customizable options for field names, calendar dimensions, and SAP DeltaQ sources.

#### **2.** [**Source Wizard**](source-wizard.md)

The **Source Wizard** is used to add new data sources to the repository.\
**Key Features**:

* Supports Table or Query as source types.
* Retrieves relationships for tables and provides SAP-specific attributes.
* Allows users to test queries and configure schema and table filters.

#### **3.** [**Import Wizard**](import-wizard.md)

The **Import Wizard** helps define and manage the import of external data into the data warehouse.\
**Key Features**:

* Configures the source, target schema, table name, and SSIS package.
* Provides options for additional attributes and parameters.

#### **4.**[ **Historization Wizard**](historization-wizard.md)

The **Historization Wizard** manages the historicization of tables or transformations.\
**Key Features**:

* Supports Slowly Changing Dimensions (SCD) types: SCD 0, SCD 1, and SCD 2.
* Configures empty record behavior and the use of Vault IDs as primary keys.
* Supports historization through SSIS packages or stored procedures.

#### **5.** [**Transformation Wizard**](transformation-wizard.md)

The **Transformation Wizard** enables the creation and management of data transformations.\
**Key Features**:

* Supports Regular, Manual, Script, and External transformation types.
* Provides options for handling historicized and non-historicized data.
* Configures table joins, field selections, and transformation persistence.

#### **6.** [**Calendar Transformation Wizard**](calendar-transformation-wizard.md)

The **Calendar Transformation Wizard** is used to create a calendar transformation in the data warehouse.\
**Key Features**:

* Configures parameters such as schema, name, start and end dates, and date-to-ID conversion macros.
* Allows assignment to data mart stars.

#### **7.** [**Time Transformation Wizard**](time-transformation-wizard.md)

The **Time Transformation Wizard** enables the creation of time dimensions for time-based analytics.\
**Key Features**:

* Configures parameters such as schema, name, time period, and time-to-ID conversion macros.
* Allows assignment to data mart stars.

#### **8.** [**Snapshot Transformation Wizard**](snapshot-transformation-wizard.md)

The **Snapshot Transformation Wizard** is used to create snapshot transformations for snapshot-based data analysis.\
**Key Features**:

* Supports the creation of a single snapshot dimension in the data warehouse.
* Configures schema, name, and assignment to data mart stars.

By using these eight wizards, AnalyticsCreator simplifies complex tasks, ensures consistency, and accelerates the development and management of a data warehouse.
