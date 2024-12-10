# Source references

Define relations between sources. These relations will be inherited by the data warehouse objects during the synchronization.&#x20;

The N:1 “one field” to “one primary key field” references the user can define directly in the source definition. In this case please use the “Referenced column” attribute.&#x20;

To define more complex references please use “Source references”.&#x20;

There is the typical table reference definition:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

All defined conditions – both the Reference Statement and column conditions will be combined using AND operator. The above reference would look like:&#x20;

```sql
A.WAERS IN (‘EUR’, ‘USD’) 
AND A.BUKRS = B.BUKRS 
AND A.KUNNR = B.KUNNR 
AND A.MANDT = B.MANDT 
AND A.LAND1 = ‘DE’ 
AND A.PERIO = B.PERIO + 1
```

The source relations will be inherited into the next DHW layers.&#x20;

For example, if you define the references between two source tables, which will be imported, the same references will be created between two import tables.&#x20;

If you change the source reference, the changes will be propagated into the inherited references unless they a used in transformations. Such references will be renamed (suffix “\_changed(N)” will be added) and the new inherited references will be created.&#x20;

Therefore, if you change the “parent” reference, the transformations using inherited reference will be not changed but the user can change them manually by select the new inherited reference.
