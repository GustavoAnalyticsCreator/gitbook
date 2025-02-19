# Time transformation wizard

To create a time transformation, select **"Add" → "Time Dimension"** from the diagram context menu.

As shown in the image below:

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

The **Time Transformation Wizard** will then open, allowing the user to configure a new time transformation.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

#### **Parameters**:

1. **Schema**: The schema of the time transformation.
2. **Name**: The name of the time transformation.
3. **Period (Minutes)**: The period (in minutes) for the time transformation.
4. **Time-to-ID Function**: The name of the macro that transforms a **DateTime** value into the key value for the time dimension. This macro can be used, for example, in fact transformations to convert **datetime** fields into time dimension members.
5. **Stars**: The data mart stars where the time transformation will be included.
