# Macros

macro is a powerful tool used to simplify the transformation definition.\
Every macro has the following components:

* **Name**: The name of the macro.
* **Language**: The programming language used in the macro.
* **Definition Statement**: The logic or functionality defined within the macro.\
  Optionally, a macro can also have a referenced table.

Currently, two languages are supported: **T-SQL** and **SSIS**.

* **T-SQL Macros**: These can be used in transformations, calculated fields, and other database-specific objects.
* **SSIS Macros**: These can be used in SSIS statements to define import constraints or field transformations.

Below is a typical macro definition:

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

**Macro Statement and Parameters**\
Every macro statement contains macro parameters, such as :1, :2, :3, and so on.\
To call a macro, use the macro name with the **@** symbol in front of it, followed by the parameters. For example:\
&#xNAN;**@Date2ID(T1.BUDAT)**

The macro parser processes the macro statement and replaces **:1**, **:2**, etc., with the macro parameters. In the above case, it will be replaced with:

```sql
CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, T1.BUDAT)) + 1, 0)) 
```

**Macro Parameters and NULL Replacement**\
If the number of macro parameters in a macro call is less than the number of defined parameters, the remaining parameters will be replaced by **NULL**. For example, the call **@Date2ID()** will be parsed into:

```sql
CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, NULL)) + 1, 0))
```

**Referenced Table Parameter and Macro Usage**\
The **"Referenced Table"** parameter is used to automatically create a reference between the referenced table and the transformation field using a specific macro.\
A common way to use macros is as a column definition statement in transformations. For example:

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

**Macro Parsing in the Transformation VIEW**\
In the transformation **VIEW**, the macro statement will be parsed as follows:

```sql
[AVal] = [T1].[WKGATR],
[FK_Time] = CONVERT(bigint, ISNULL(DATEDIFF(DD, '20000101', CONVERT(date, T1.BUDAT, 112)) + 1, 0))
```

**Macro Definition Changes and Recalculation**\
If you change the macro definition, all dependent transformations and calculated columns will be recalculated automatically.
