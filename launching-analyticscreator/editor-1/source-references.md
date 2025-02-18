---
icon: file-plus-minus
---

# Source references

Defining Relations Between Sources Relations between sources are defined and will be inherited by the data warehouse objects during synchronization.&#x20;

The N:1 relation, which refers to a "one field" to a "one primary key field" reference, can be defined directly in the source definition by using the "Referenced column" attribute.&#x20;

For more complex references, use "Source references."

Below is a typical table reference definition:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**Inheritance of Source Relations Across DWH Layers**&#x20;

Source relations will be inherited into subsequent DWH layers. For example, if references are defined between two source tables that are imported, the same references will be automatically created between the corresponding import tables.&#x20;

If a source reference is changed, the changes will propagate into the inherited references, unless those references are used in transformations. In such cases, the references will be renamed by adding the suffix "\_changed(N)" and new inherited references will be created.&#x20;

Therefore, if a "parent" reference is changed, transformations using the inherited reference will not be updated automatically. However, the user can manually update them by selecting the new inherited reference.
