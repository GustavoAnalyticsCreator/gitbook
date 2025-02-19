# DWH Wizard

The **DWH Wizard** allows for the rapid creation of a semi-ready data warehouse. It is especially effective when the data source includes predefined table references or manually maintained source references.

**Prerequisites**:

* At least one source connector must be defined before using the DWH Wizard.
* Note:

&#x20;The DWH Wizard does not support CSV connectors. For CSV sources, use the **Source Wizard** instead.

To launch the DWH Wizard, click the **“DWH Wizard”** button in the toolbar.

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

**Instead, the user can use the connector context menu**:

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

**Using the DWH Wizard**\
In the DWH Wizard window, you should select the connector, optionally enter the schema or table filter, and click the **"Apply"** button. Then, the source tables will be displayed.

Optionally, the user can select the **"Existing Sources"** radio button. In this case, the DWH Wizard will not read the external source information. Instead, it will display the sources already defined in the specific connector. This option is particularly useful when using meta connectors.

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

If a specific source table already exists in the repository, the **"Exist"** checkbox will be selected.\
To add specific external tables to the repository, select them (use the **Ctrl** button for multiple selection) and click the  ![](<../../.gitbook/assets/image (64).png>) button.&#x20;

To remove an external table from the repository, select it in the table below and click the ![](<../../.gitbook/assets/image (65).png>) button:



<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

The next window will allow you to configure your Data Warehouse:

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

**DWH Wizard Architecture Options**\
The DWH Wizard can create data warehouses based on different architectures: Classic (Kimball), Data Vault 1 and 2, or a mixed architecture. The available options vary depending on the selected architecture.

* **Classic or Mixed Architecture**: The user can select automatic creation of imports, historization, dimensions, and facts.
* **Data Vault Architecture**: The user can select automatic creation of imports, hubs and satellites, links, dimensions, and facts. If you select **"Auto"**, the DWH Wizard will automatically decide which type of object (hub/sat or link) to create.

Additionally, if you select **SAP DeltaQ sources**, you will need to define some DeltaQ-specific attributes.

As shown in the image below, the available options depend on the architecture selected.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

On the next page, the user can define name templates for different DWH objects:

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

On the next page, the user can set additional parameters:

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

**DWH Wizard Properties**

1. **Field Name Appearance**: You can decide whether the field names remain unchanged or are converted to uppercase or lowercase strings.
2. **Retrieve Relations**: Choose whether the DWH Wizard should attempt to retrieve information about source references from the source.
3. **Create Calendar Dimension**: Select whether the DWH Wizard should create a Calendar dimension (if it hasn’t already been created). If yes, the user can define the start and end dates for the Calendar dimension.
4. **Include Tables in Facts**: If the DWH Wizard detects references between source tables, it can add the referenced tables to the fact transformations. You can choose from the following options:
   * N:1 direct related
   * N:1 direct and indirect related
   * All direct related
   * All direct and indirect related
5. **Use Calendar in Facts**: If selected, reference fields to the calendar dimension will be added to the fact transformations for every date field in every table included in the fact transformation.
6. **SAP DeltaQ Transfer Mode**: For SAP DeltaQ sources, the user can select between IDoc or tRFS mode.
7. **SAP DeltaQ Automatic Synchronization**: Enable or disable automatic synchronization for SAP DeltaQ.
8. **SAP Description Language**: For SAP sources, the user can select the language for object descriptions.
9. **DataVault2: Do Not Create HUBs**: In the case of the DataVault2 architecture, the user can suppress the creation of HUBs.
10. **Historizing Type**: You can select between using an SSIS package or a stored procedure for historization.
11. **Use Friendly Names in Transformations as Column Names**: If friendly names are maintained in the source description (usually for SAP, meta connectors, or manually maintained connectors), the user can use field-friendly names as field names in the transformations instead of technical names.
12. **Default Transformations**: You can select which predefined transformations should be used in dimensions.
13. **Stars**: You can decide whether the created dimensions and facts should belong to the data mart stars.
