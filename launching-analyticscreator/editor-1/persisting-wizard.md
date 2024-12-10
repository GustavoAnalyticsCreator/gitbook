# Persisting wizard

You can store the content of any regular or manual transformation in the table. Usually you should do it to speed up access to the complex transformations. Persisting of transformation will be made in SSIS package. To persist a transformation please use the object context menu “Add->Persisting” in the diagram:

Persisting wizard:

Transformation: Name of transformation to persist Persist table: Name of the persisting table. Table will be created in the same schema as a transformation. Persist package: Name of the SSIS package to make persisting.
