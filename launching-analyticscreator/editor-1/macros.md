# Macros

Macro is a very powerful tool to simplify the transformation definition.

Every macro has a Name, language and a definition statement. Optionally a macro can have a referenced table.&#x20;

We support two languages now: T-SQL and SSIS. T-SQL macros can be used in transformations, calculated fields and other database-specific objects. SSIS macros can be used in SSIS statements to define the import constraints or field transformations.&#x20;

There is a typical macro definition:

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Every macro statement contains the macro parameters - :1, :2, :3 and so on.&#x20;

To call Macro you use the macro name with the @ in front of it and the parameters, for example:&#x20;

@Date2ID(T1.BUDAT)&#x20;

The macro parser will take the macro statement and replace the :1 by the macro parameter. In above case it will be:&#x20;

```sql
CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, T1.BUDAT)) + 1, 0)) 
```

If the count of macro parameters in macro call is less than the count of defined parameters, the remaining parameters will be replaced by NULL, for example the call @Date2ID() will be parsed into:&#x20;

```sql
CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, NULL)) + 1, 0))
```

&#x20;The “Referenced table” parameter will be used to automatically create a reference betthe documentationen the referenced table and the transformation field using specific macro. The common way to use macros is to use them as a column definition statement in transformations. For example:

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

In the transformation VIEW the macro statement will be parsed:

```sql
[AVal] = [T1].[WKGATR],
[FK_Time] = CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, T1.BUDAT, 112)) + 1, 0))
```



If you change the Macro definition, all dependent transformations and calculated columns will be recalculated automatically.
