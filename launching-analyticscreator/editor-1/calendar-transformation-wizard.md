# Calendar transformation wizard

To create a calendar transformation, select **"Add" → "Calendar Dimension"** from the diagram context menu.

As shown in the image below:

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

The **Calendar Transformation Wizard** will open. Typically, only one calendar transformation is required in the data warehouse.

As shown in the image below:

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

**Parameters**:

1. **Schema**: The schema of the calendar transformation.
2. **Name**: The name of the calendar transformation.
3. **Date From**: The start date for the calendar.
4. **Date To**: The end date for the calendar.
5. **Date-to-ID Function**: The name of the macro that transforms a **DateTime** value into the key value for the calendar dimension. This macro can be used, for example, in fact transformations to convert **datetime** fields into calendar dimension members.
6. **Stars**: The data mart stars where the calendar transformation will be included.
