# Historization wizard

Historization wizard will be used to historicize a table or transformation.

To start Historization wizard use object context menu “Add->Historization” in diagram:

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

Alternatively, the object context menu in the navigation tree can be used.

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

There is a typical Historization wizard window:

<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

### Options

1. Source table: Table which should be historicized&#x20;
2. Target schema: schema of the historicized table&#x20;
3. Target name: name of the historicized table&#x20;
4. Package: name of SSIS package where the historization will be done. You can select the existing historization package or add a new package name.
5. Historizing type: You can select between SSIS package and stored procedure
6. SCD Type: the user can select between different historization types: SCD 0, SCD 1 and SCD 2&#x20;
7. Empty record behavior: You can define what should happen in case of missing source record.&#x20;
8. Use VAULT ID as PK: If you use DataVault or mixed architecture the user can use HashKeys instead of business keys to perform historization.&#x20;
9. After you click on “Finish” the historization will be generated and diagram will be updated automatically. Then the user can select the generated historizing package and optional change some package properties (see “Historizing package”).

