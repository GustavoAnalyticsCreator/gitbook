# Transformation wizard

The **Transformation Wizard** should be used to create a new transformation. To start the **Transformation Wizard**, use the object context menu: **"Add" → "Transformation"** in the diagram.

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

**Typical Transformation Wizard Window**\
Here is a typical **Transformation Wizard** window, as shown in the image below:

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

AnalyticsCreator supports different transformation types:

1. Regular transformations described in the tabular form. Based on the description AnalyticsCreator generates the VIEW&#x20;
2. Manual transformations are the hand created VIEWs&#x20;
3. Script transformations are the SQL scripts. Using SQL Scripts you can call stored procedures.
4. External transformations are manually created SSIS packages. Transformatino wizard has the following options:

Transformatino wizard has the following options:

Main page:

1. Type: transformation type
   1. Dimension: a regular transformation usually used to create dimensions. The default settings for a dimension are:
      1. Historizing type: FullHist
      2. Create empty member: yes
      3. Table JoinHistType: Actual
      4. Fields: all fields
   2. Fact: a regular transformation usually used to create facts. The default settings for a dimension are:
      1. Historizing type: Snapshot
      2. Create empty member: no
      3. Table JoinHistType: Historical\_to
      4. Fields: all key fields
   3. Other: a regular transformation. The default settings for a dimension are:
      1. Historizing type: FullHist
      2. Create empty member: no
      3. Table JoinHistType: Historical\_to
      4. Fields: all fields
   4. Manual: a manually defined VIEW. Default settings are irrelevant
   5. External: external transformation
   6. Script: script transformation
   7. Schema: transformation schema
   8. Name: transformation name
   9. Historizing type: defines how to work with historicized data
      1. FullHist: Fully historicized transformation with result contains \[SATZ\_ID], \[DAT\_VON\_HIST] and \[DAT\_BIS\_HIST] fields. Usually used to define dimensions.
      2. SnapshotHist: Fully historicized transformation with data for predefined snapshot dates only. Usually used to define dimensions.
      3. Snapshot: Transformation using predefined snapshot dates to combine historicized data. Usually used to define fats
      4. ActualOnly: To combine historicized data only actual data will be used. Can be used to create dimensions and facts.
      5. None: Should be used to work with not historicized data.
   10. Main table: main table used in transformation. Relevant for regular transformations only
   11. Create unknown member: usually used in dimensions. Adds to the transformation a new row with surrogate ID = 0 and default values for the fields. Usually is used as a dimension member in case the according dimension member is not found during the fact processing.
   12. Persist transformation: if selected, the content of VIEW will be stored in the table to speed up access to the transformation results. Relevant for the regular and manual transformations.
   13. Persist table: name of the table to persist transformation results.
   14. Persist package: name of the SSIS package to persist transformation results
   15. Result table: Relevant for external or script transformations. The name of the table where the transformation result will be stored
   16. SSIS Package: Relevant for external or script transformations. The name of the SSIS package where the transformation will be launched

**Table Selection Page**: This page allows the selection of additional tables to be used in the transformation. These tables must be directly or indirectly referenced to the main transformation table.

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

### Parameters:

1. Table JoinHistType: is relevant for the historicized tables only. There are always two tables: the joined table and the anchor table – the table which the joined table join on.
   1. None: No additional conditions will be added to the JOIN statement
   2. Actual: most actual data will be selected from the joined table
   3. &#x20;Historical\_from: only the data which were valid at the start of validity period of the anchor table will be selected from the joined table.
   4. Historical\_to: only the data which were valid at the end of validity period of the anchor table will be selected from the joined table.
   5. Full: the full history of changes in both tables will be reproduced. This is most complete but also most complex join type for two historicized tables.
2. All N:1 direct related: all tables directly referenced to the main table with cardinality “Many-to-one” will be added
3. &#x20;All direct related: all tables directly referenced to the main table with any cardinality
4. All N:1 related: all tables directly and indirectly referenced to the main table with cardinality “Many-to-one” will be added
5. All related: all tables directly and indirect referenced to the main table with any cardinality
6. Use hash keys if possible: if there are hash key references in addition to the business key references, they will be used.

Parameter Page: This page allows the configuration of additional transformation parameters, applicable only to regular transformations.

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Parameters:

1. Fields: which fields will be added to the transformation
   1. None: no fields will be added. You should define transformation fields manually
   2. All key fields: Key fields from all transformation tables will be added. Usually this option will be used in fact transformations.
   3. All fields: All fields from all transformation tables will be added. Usually this option will be used in dimension transformations.
2. Field names: field name in case of duplicated names
   1. Field\[n]:  the sequential number will be added to the field name (for example “Descrition1”)
   2. Table\_Field: - table name will be added to the field name (for example “Department\_Descrition”)
3. Field names appearance
   1. No changes: field names remain unchanged
   2. Upper case: field names will be converted in upper case
   3. Lower case: field names will be converted in lower case
4. Key fields NULL to zero: if selected, the NULL values in key fields will be converted into 0. Is useful for the fact transformations to join with default member in dimensions  in case of missing dimension members.
5. Use friendly names as column names: In case there are friendly column names in the transformation tables, they will be used as field names.

**Stars Page**: This page allows you to define the stars to which the transformation belongs and specify any predefined transformations.

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

1. **Stars**: Specifies the data mart stars where the transformation will be included.
2. **Default Transformations**: Defines the use of predefined transformations for the transformation.
   1. **No Defaults**: No predefined transformations are applied, typically used for fact transformations.
   2. **All Defaults**: All predefined transformations are applied, commonly used for dimension transformations.
   3. **Selected Defaults**: Specific predefined transformations can be chosen using the provided list boxes.
3. This page allows the user to manage the tables that depend on the current transformation. As shown in the image below:

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

This feature is relevant for external transformations. Here, the user should add the tables that the transformation depends on.

**Script Page**\
This page is specifically for script transformations. It allows the user to enter the SQL script that defines the transformation logic.

As shown in the image below:

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>
