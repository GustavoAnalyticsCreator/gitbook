# Sources

Source contains the description of is the external data. Each source belongs to the connector. Each source has columns. You can define the references between sources.

To open source definition please use source context menu “Edit source” in navigation tree or in diagram.

To add new source please use source context menu “Add new source” in navigation tree or in diagram.

There is the typical source definition:

![](<../../.gitbook/assets/image (1).png>)\


Depend on the connector type and the source type sources can have different properties.

There are three source types:&#x20;

1. TABLE
2. &#x20;VIEW
3. SAP\_DELTAQ and QUERY

In case of QUERY source type, the source window will have additional tab containing query definition.

You cannot create a source manually. To add a new source, you should use either [DWH Wizard](dwh-wizard.md) or [Source Wizard.](source-wizard.md) The only source you can create manually is the CSV source.

Additionally, you can define the source constraints. These constraints will be used due the data import to filter the wrong data or to generate warnings.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

In this example the data with **StartDate < EndDate** will be not imported and the message **StartDate** greater than **EndDate** will be added to the log table. The data with **StartDate = EndDate** will be imported but according log table entry will be generated.

###
