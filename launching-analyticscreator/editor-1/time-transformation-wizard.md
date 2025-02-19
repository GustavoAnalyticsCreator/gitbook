# Time transformation wizard

To create a time transformation, select **“Add -> Time Dimension”** from the diagram context menu.

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

The **Time Transformation Wizard** will then open, allowing the configuration of a new time transformation.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

### Parameters:&#x20;

1. Schema: Schema of time transformation&#x20;
2. Name: Name of time transformation
3. Period (minutes): Period (in minutes) of time transformation&#x20;
4. Time-to-ID function: Name of the macro which will transform a DateTime value to the key value of the time dimension. You can use this macro, for example, in the fact transformations to convert datetime fields into time dimension members.&#x20;
5. Stars: You can select the data mart stars where the time transformation will be present
