---
icon: info
description: Checking for Source Changes and Propagating Them to Data Warehouse Objects
---

# Refresh source metadata

The user can check for changes in the source and propagate any detected changes to the data warehouse objects. To check for changes in all connector sources, use the connector context menu and select "Refresh all sources" in the navigation tree.



{% embed url="https://www.analyticscreator.com/hubfs/WikiDocumentation/RefershMetadataFromSource.mp4" %}

To check for changes in imported connector sources only, use the connector context menu and select **"Refresh used sources"** in the navigation tree.

To check for changes in a specific source, use the source context menu and select **"Refresh source"** in the navigation tree.

**Refresh Source Options:**

The following refresh options are available:

* **Detect differences**: This option detects changes in the source but does not modify the repository. If selected, the source changes will be detected, but no changes will be made in the repository.
* **Delete missing sources**: This option deletes any missing sources from the repository.
* **Refresh source descriptions**: This option refreshes the descriptions of the sources.
* **Refresh columns in imported tables**: This option refreshes the columns in the imported tables when there are new or changed source columns.
* **Delete missing columns in imported tables**: This option deletes columns in the imported tables if the corresponding source columns have been deleted.
* **Refresh primary keys in imported tables**: This option refreshes the primary key in the imported tables if the source’s primary key has changed.
* **Refresh descriptions in imported tables**: This option refreshes the descriptions of the imported tables and columns.
