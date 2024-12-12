---
icon: table-tree
---

# Table references

#### **Defining Table Relationships in AnalyticsCreator**

Relationships between tables can be defined to enable combining tables during transformations. These relationships include `N:1` ("1-field" to "1-primary key field") references and more complex associations.

**Defining `N:1` References**

**One-Field to One Primary Key Field**:\
These references can be directly defined within the table definition using the **Referenced Column** attribute.

* Example: A foreign key in one table referencing the primary key of another.

More complex references you can define using “Table references”.

There is the typical table reference definition:

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### Table Reference Properties:

1. **Cardinality:**&#x20;
   1. Unknown
   2. OneToOne
   3. ManytoOne
   4. OneToMany
   5. ManyToMany

{% hint style="info" %}
It is recommended to primarily use **Many-to-One (N:1)** and           **One-to-Many (1:N)** cardinalities.
{% endhint %}

2. **Join:** SQL join type
3. **Table1:** Schema and table name of the first table
4. **Table2:** Schema and table name of the second table
5. **Alias 1:** optional. Alias of the first table. Should be defined if reference statement is used
6. **Alias 2:** optional. Alias of the second table. Should be defined if reference statement is used
7. **Description:** reference name
8. **Auto created:** if checked, the reference was automatically created during synchronization.
9. **Reference statement:** optional. SQL reference statement. Should be used if reference cannot be described using column references only. Table aliases will be used
10. **Columns:** There are columns and statements. Either column or statement should be defined on each reference side.
    1. **Column1:** Column from the first table
    2. **Statement1:** SQL statement.
    3. **Column2:** Column from the second table
    4. **Statement2:** SQL statement.

All defined conditions – both the Reference Statement and column conditions will be combined using AND operator.&#x20;

The above reference would look like:

```sql
F.GJAHR = LEFT(C.DATUM, 4) 
AND F.MANDT = 100 
AND F.ARTNR = C.MATNR 
AND F.BUKRS = C.BUKRS 
AND F.WERKS = C.WERKS
```

The table relations will be inherited into the next DHW layers. For example, if you define the references between two import tables, which will be historicized, the same references will be created between two historicized tables.

\
If you change the reference, the changes will be propagated into the inherited references unless they a used in transformations. Such references will be renamed (suffix “\_changed(N)” will be added) and the new inherited references will be created. Therefore, if you change the “parent” reference, the transformations using inherited reference will be not changed but you can change them manually by select the new inherited reference.

\
The inherited references (flag “Auto created” is set) cannot be changed unless you unmark the “Auto created” flag.

