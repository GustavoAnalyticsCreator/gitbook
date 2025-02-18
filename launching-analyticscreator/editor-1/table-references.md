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

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### Table Reference Properties:

1. **Cardinality:**&#x20;
   1. Unknown
   2. OneToOne
   3. ManytoOne
   4. OneToMany
   5. ManyToMany

{% hint style="info" %}
It is recommended to primarily use **Many-to-One (N:1)** and **One-to-Many (1:N)** cardinalities.
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

**Inheritance of Table Relations Across DWH Layers**

\
Table relations will be inherited into subsequent DWH layers. For example, if references are defined between two import tables that are historicized, the same references will be automatically created between the corresponding historicized tables.

If a reference is changed, the changes will propagate into the inherited references unless those references are used in transformations. In such cases, the references will be renamed by adding the suffix "\_changed(N)", and new inherited references will be created.

\
Therefore, if a "parent" reference is changed, transformations using the inherited reference will not be updated automatically. However, you can manually update them by selecting the new inherited reference.

The inherited references, where the "Auto created" flag is set, cannot be modified unless you uncheck the "Auto created" flag.

