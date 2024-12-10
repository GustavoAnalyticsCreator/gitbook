# Historization wizard

Historization wizard will be used to historicize a table or transformation. To start Historization wizard use object context menu “Add->Historization” in diagram:

Instead the user can use object context menu in navigation tree:

There is a typical Historization wizard window:

Options: Source table: Table which should be historizised Target schema: schema of the historizised table Target name: name of the historizised table Package: name of SSIS package where the historization will be done. You can select the existing historization package or add a new package name. Historizing type: You can select betthe documentationen SSIS package and stored procedure SCD Type: the user can select betthe documentationen different historization types: SCD 0, SCD 1 and SCD 2 Empty record behavior: You can define what should happen in case of missing source record. Use VAULT ID as PK: If you use DataVault or mixed architecture the user can use HashKeys instead of business keys to perform historization. After you click on “Finish” the historization will be generated and diagram will be updated automatically. Then the user can select the generated historizing package and optional change some package properties (see “Historizing package”).
