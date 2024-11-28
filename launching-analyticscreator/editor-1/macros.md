---
noIndex: true
icon: laptop-binary
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Macros

**Breadcrumb:**\
Toolbar -> DWH -> Macros\
Navigation tree -> Macros -> Add macro\
Navigation tree -> Macros -> Macro -> Edit macro

**\[\[**_**TOC**_**]]**

**Macro** is a parametrized statement which you can use in transformations, in the definition of table computed columns, OLAP measures and so on.\
A macro is usually a statement containing placeholders.\
Placeholders will be replaced by calling parameters during macro parsing.\
Placeholders look like :1, :2, :3, and so on.\
`:1` placeholder will be replaced by the first macro parameter, `:2` by the second, and so on.\
To call a macro, please use the `@` sign. For example, `@Test(param1, param2...)` will run the "Test" macro.\
For example, you have a macro "Test" with the definition `:1 + :2`. When you call it as `@Test(T1, T2)`, the macro call will be replaced by `T1 + T2`.\
Missing parameters will be replaced by `NULL`: `@Test(T1)` -> `T1 + NULL`.\
You can call macros within macros. For example, you can create a macro `@Test1` as `@Test(:1, :2) + :3`.

#### Add Macros

1. In the **navigation-tree**, right-click **Macros** and click **Add macro**.
2. In the **Macro name** box, type the name of the macro.
3. In the **Description** box, type the description of the macro.
4. In the **Language** list, select the language you want to use for the macro definition.
5. In the **Referenced** table list, select the table.
6. In the **Statement** box, type the code you want to be processed.

**Example:**

```sql
CASE
    WHEN :1 < '19800101' THEN 0 
    WHEN :1 > '20401231' THEN CONVERT(bigint, DATEDIFF(DD, '19800101',  '20401231') + 1)
    ELSE CONVERT(bigint, ISNULL(DATEDIFF(DD, '19800101', CONVERT(date, :1)) + 1, 0))
END
```

#### Import Macros from Cloud

1. In the **navigation-tree**, right-click **Macros** and click **Import macros from cloud**.
2. Select the repository from where you want to import macros.

#### Import Macros from File

1. In the **navigation-tree**, right-click **Macros** and click **Import macros from file**.
2. Select the file from the directory you want to import. All `.AC` files will be shown in the open dialog.
