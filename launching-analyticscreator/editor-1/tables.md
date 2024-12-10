# Tables

#### **Tables in AnalyticsCreator**

A **table** represents a database table or view within the data warehouse, and each table belongs to a specific schema. Tables are created automatically when defining a data import, historization, or persisting process. Views are created when defining a transformation. Additionally, tables can be manually created to store results of external or script transformations.

For most tables, several properties can be configured, including calculated columns, primary keys, identity columns, and indexes.

There is the typical table definition:

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Properties:&#x20;

1. &#x20;**Table name:** table name&#x20;
2. **Table schema:** table schema&#x20;
3.  **Table type:** type of the table&#x20;

    1. Import table: Table which is filled by the external data using SSIS package.
    2. Historicized table: Table containing historicized data. Every historicized table contains 3 mandatory fields (names are configurable): \
       SATZ\_ID (bigint) – surrogate primary key \
       DAT\_VON\_HIST (datetime) – start of a validity period \
       DAT\_BIS\_HIST (datetime) – end of a validity period
    3. View without history: Result of transformation containing no historicized data&#x20;
    4. View with history: Result of transformation containing historicized data&#x20;
    5. Persisted table without history: Table used to persist the result of non-historicized transformation&#x20;
    6. Persisted table with history: Table used to persist the result of historicized transformation&#x20;
    7. Data mart dimension view without history: Result of non-historicized data mart dimension transformation&#x20;
    8. Data mart dimension view with history: Result of historicized data mart dimension transformation&#x20;
    9. Data mart fact view without history: Result of non-historicized data mart fact transformation&#x20;
    10. Data mart fact view with history: Result of historicized data mart fact transformation o Externally filled table without history: Table filled by non-historicized external or script transformation&#x20;
    11. Externally filled table with history: Table filled by historicized external or script transformation o Data vault hub table with history: Historicized table containing data vault hub records&#x20;
    12. Data vault satellite table with history: Historicized table containing data vault satellite records o Data vault link table with history: Historicized table containing data vault link records&#x20;


4. Friendly name: if defined, will be used in OLAP cubes instead of table name. Friendly name will be inherited by depending objects
5. Compression type: table compression type. DEFAULT (settable using parameter TABLE\_COMPRESSION\_TYPE), NONE, RAW, PAGE&#x20;
6. Description: table description. Will be inherited by depending objects&#x20;
7. Hist of table, Persist of table, Hub of table, Satellite of table, Link of table: name of according table&#x20;
8. Has primary key: if checked, the PRIMARY KEY COSTRAINT will be added to the table&#x20;
9. Primary key name: name of primary key.
10. PK clustered: if checked, the clustered primary key will be created&#x20;
11. Columns: table columns&#x20;

    1. Column name: name of column
    2. Data type, MaxLength, NumPrec, NumScale, Nullable: SQL column properties
    3. PKOrdinalPos: column position in primary key (1,2…)
    4. Default: SQL DEFAULT statement (for example GETDATE())&#x20;
    5. Friendly name: if defined, will be used in OLAP cubes instead of column name. Friendly name will be inherited by depending objects.
    6. Referenced column: here you can define the “one-field” N:1 references to the primary keys in another tables.&#x20;
    7. References: comma-separated list of referenced columns. Is read-only&#x20;


12. Identity column: if defined, the identity columns will be added to the table&#x20;
    1. Name, type, seed, increment – SQL IDENTITY properties&#x20;
    2. PK pos: column position in primary key (usually – 1)&#x20;

For the normal tables (not views) you can optional define identity column and calculated columns (Calculated columns – tab).

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Properties:

1. Column name: name of column
2. Statement: SQL Statement. You can use AnalyticsCreator macros (see Macros). You can use predefined @GetVaultHash – macro to create hash keys.
3. Persisted: if checked, calculated column will be persisted
4. PKOrdinalPos: column position in primary key (1,2…)
5. Friendly name: if defined, will be used in OLAP cubes instead of column name. Friendly name will be inherited by depending objects
6. Referenced column: here you can define the “one-field” N:1 references to the primary keys in another tables.
7. References: comma-separated list of referenced columns. Is read-only

