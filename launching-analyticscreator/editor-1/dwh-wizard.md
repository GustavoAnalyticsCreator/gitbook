# DWH Wizard

The **DWH Wizard** allows for the rapid creation of a semi-ready data warehouse. It is especially effective when the data source includes predefined table references or manually maintained source references.

**Prerequisites**:

* At least one source connector must be defined before using the DWH Wizard.
* Note: The DWH Wizard does not support CSV connectors. For CSV sources, use the **Source Wizard** instead.

To launch the DWH Wizard, click the **“DWH Wizard”** button in the toolbar.

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

Instead the user can use connector context menu:

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

In the DWH Wizard window you should select the connector, optionally enter the schema or table filter and click on “Apply” button. Then you will see the source tables:&#x20;

Optionally the user can select “Existing sources” radio button. In this case DWH wizard will not read the external source information. Instead it will show you in you the sources already defined in the specific connector. This option is particularly interesting if you use meta connectors.

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

If the specific source table already exists in the repository the “Exist” checkbox will be selected.&#x20;

To add specific external tables to the repository please select them (use ctrl button for multiple selection) and click on ![](<../../.gitbook/assets/image (64).png>) button.&#x20;

To remove external table from the repository select it in the table below and press ![](<../../.gitbook/assets/image (65).png>) button:



<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

The next window wil be

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

DWH Wizard can create data warehouses based on different architectures: Classic (Kimball), Data Vault 1 and 2 or mixed architecture. There are some different options depending on the architecture you selected.&#x20;

If you selected the classic or mixed architecture the user can select the automatically creation of import, historization, dimensions and facts.&#x20;

If you selected the DataVault architecture the user can select the automatically creation of import, hubs and satellites, links, dimensions and facts. If you select “Auto”, DWH Wizard will automatically decide which kind of object (hub/sat or link) it will create.&#x20;

Additionally if you select the SAP DeltaQ sources you should define some DeltaQ-specific attributes.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

On the next page the user can define the name templates for different DWH objects:

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

On the next page the user can set some additional parameters:

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

Proprieties&#x20;

1. Field name appearance: You can decide if the field names remain unchanged or will be converted into upper or lothe documentationr case strings.&#x20;
2. Retrieve relations: If DWH wizard should try to retrieve information about source references from the source.&#x20;
3. Create Calendar dimension: if DWH wizard should create Calendar dimension (in case it isn’t already created). If yes, the user can define the start and end date for the Calendar dimension.
4. Include tables in facts: If DWH wizard can find the references between the source tables it can add the referenced tables to the fact transformations. You can decide between documentationen:&#x20;
   1. N:1 direct related&#x20;
   2. N:1 direct and indirect related&#x20;
   3. All direct related&#x20;
   4. All direct and indirect related&#x20;
5. Use Calendar in facts: If you select this option, the reference fields to the calendar dimension will be added to the fact transformations for every date field in every table included to the fact transformation.&#x20;
6. SAP DeltaQ transfer mode: For SAP DeltaQ sources the user can select between  IDoc or tRFS mode.&#x20;
7. SAP DeltaQ automatic synchronization&#x20;
8. SAP description language: for SAP sources the user can select the language of the object descriptions&#x20;
9. DataVault2: do not create HUBs: In case of DataVault2 architecture the user can suppress the creation of HUBs.&#x20;
10. Historizing type: You can select between  the SSIS package or stored procedure&#x20;
11. Use friendly names in transformations as column names: In case the the friendly names are maintained in the source description (usually SAP, meta connectors or manually maintained connectors) the user can use field friendly names as field names in the transformations instead of technical names.&#x20;
12. Default transformations: You can select which predefined transformations should be used in dimensions.&#x20;
13. Stars: You can select if the created dimensions and facts should belong to the data mart stars.
