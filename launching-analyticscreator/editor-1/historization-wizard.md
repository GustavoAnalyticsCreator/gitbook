# Historization wizard

The **Historization Wizard** is used to historicize a table or transformation.\
To start the **Historization Wizard**, use the object context menu: **"Add" → "Historization"** in the diagram, as shown in the image below:

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

Alternatively, the object context menu in the navigation tree can be used, as shown in the image below:

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

There is a typical **Historization Wizard** window, as shown in the image below:\


<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

1. **Source Table**: The table that should be historicized.
2. **Target Schema**: The schema of the historicized table.
3. **Target Name**: The name of the historicized table.
4. **Package**: The name of the SSIS package where the historization will be done. You can select an existing historization package or add a new package name.
5. **Historizing Type**: You can select between **SSIS package** and **stored procedure**.
6. **SCD Type**: The user can select between different historization types: **SCD 0**, **SCD 1**, and **SCD 2**.
7. **Empty Record Behavior**: Defines what should happen in case of a missing source record.
8. **Use VAULT ID as PK**: If you are using **DataVault** or **mixed architecture**, the user can use **HashKeys** instead of business keys to perform historization.

After clicking **"Finish"**, the historization will be generated, and the diagram will be updated automatically. Then, the user can select the generated historization package and optionally change some package properties (see **"Historizing Package"**).
