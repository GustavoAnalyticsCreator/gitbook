# Calendar transformation wizard

To create calendar transformation please select the diagram context menu “Add-> Calendar dimension”.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

The **Calendar Transformation Wizard** will open. Typically, only one calendar transformation is required in the data warehouse.

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

Parameters:&#x20;

1. Schema: Schema of calendar transformation&#x20;
2. Name: Name of calendar transformation&#x20;
3. Date from: Calendar start date&#x20;
4. Date to: Calendar end date&#x20;
5. Date-to-ID function: Name of the macro which will transform a DateTime value to the key value of the calendar dimension. You can use this macro, for example, in the fact transformations to convert datetime fields into calendar dimension members.&#x20;
6. Stars: You can select the data mart stars where the calendar transformation will be present
