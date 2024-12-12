---
icon: info
---

# Refresh source metadata

You can check the source for changes and propagate found changes to the data warehouse objects.

To check for changes in all connector sources please use connector context menu “Refresh all sources” in the navigation tree.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

To check for changes in imported connector sources only please use connector context menu “Refresh used sources” in the navigation tree.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

To check for changes in specific source please use source context menu “Refresh source” in the navigation tree.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The refresh source options:

<figure><img src="../../.gitbook/assets/image (6).png" alt="" width="563"><figcaption></figcaption></figure>

#### There are refresh source options:

1. **Detect differences:** without to change repository, if selected, the source changes will be detected but no changes will be made in repository
2. **Delete missing sources:** missing sources will be deleted in repository
3. **Refresh source descriptions:** Source descriptions will be refreshed
4. **Refresh columns in imported tables:** Import table columns will be refreshed in case of new or changed source columns
5. **Delete missing columns in imported tables:** Import table columns will be deleted in case of deleted source columns
6. **Refresh primary keys in imported tables:** primary key of the import table will be refreshed in case of changed source primary key.
7. **Refresh descriptions in imported tables:** Descriptions of import tables and columns will be refreshed
