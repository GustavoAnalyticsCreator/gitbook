# Source Wizard

You can use Source Wizard to add a new source to the repository. Co launch Source Wizard please use context menu “Add Source” of the “Sources” branch of connector:

Based on the source type you selected (Table or Query) the Source Wizard looks differently. Table:

If you select “Table” as data source you should on “Apply” button to see the list of the source tables. Optionally the user can enter the schema and table filter. There are some options the user can set: Retreive relations: If the relations of the selected source table should be retrieved (if possible) SAP description language: For SAP sources the language of the object descriptions Additionally if you select the SAP DeltaQ sources you should define some DeltaQ-specific attributes. Query:

If you select the Query as data source you should define the schema and name of the source for repository. Then you should define the Query. Query language should be supported by data source. To test the query you should click on “Test query” button. At the end please click on “Finish” button. The new source will be added and source definition will be opened:
