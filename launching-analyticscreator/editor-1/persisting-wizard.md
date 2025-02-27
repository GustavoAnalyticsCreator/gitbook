# Persisting wizard

The content of any regular or manual transformation can be stored in a table, typically to improve access speed for complex transformations. Persisting the transformation is managed through an SSIS package. To persist a transformation, the user should select **"Add" → "Persisting"** from the object context menu in the diagram.

As shown in the image below:

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

**Persisting wizard**\
As shown in the image below:

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

* **Transformation**: The name of the transformation to persist.
* **Persist Table**: The name of the table where the transformation will be persisted. The table will be created in the same schema as the transformation.
* **Persist Package**: The name of the SSIS package used to handle the persisting process.
