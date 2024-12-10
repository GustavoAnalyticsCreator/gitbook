# Refresh source metadata

You can check the source for changes and propagate found changes to the data warehouse objects. To check for changes in all connector sources please use connector context menu “Refresh all sources” in the navigation tree.

To check for changes in imported connector sources only please use connector context menu “Refresh used sources” in the navigation tree.

To check for changes in specific source please use source context menu “Refresh source” in the navigation tree.

The refresh source options:

There are refresh source options: Detect differences without to change repository – if selected, the source changes will be detected but no changes will be made in repository Delete missing sources: missing sources will be deleted in repository Refresh source descriptions: Source descriptions will be refreshed Refresh columns in imported tables: Import table columns will be refreshed in case of new or changed source columns Delete missing columns in imported tables: Import table columns will be deleted in case of deleted source columns Refresh primary keys in imported tables: primary key of the import table will be refreshed in case of changed source primary key. Refresh descriptions in imported tables: Descriptions of import tables and columns will be refreshed
