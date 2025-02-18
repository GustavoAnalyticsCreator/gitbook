---
icon: gear
---

# Transformations

A transformation is a process used to modify data. The result of a transformation is always either a single VIEW or a single TABLE.&#x20;

To create a new transformation, use the [Transformation Wizard.](transformation-wizard.md)

Each transformation has the following common properties:

1. **Name:** The name of the transformation
2. [**Schema:**](schemas.md) The schema for the transformation
3. **TransType:** The type of transformation
4. [**Stars:**](stars.md)  A list of stars in which the transformation is involved
   1. **Star:** The name of the star
   2. **IsFact:** This should be selected for fact transformations
   3. **Filter:** You can define an additional filter to restrict transformation data for a specific data mart

**AnalyticsCreator supports the following transformation types:**

[Regular transformation](regular-transformation.md)

[Manual transformation](manual-transformation.md)

[External transformation](external-transformation.md)

[Script transformation](script-transformation.md)

[Data mart transformation](data-mart-transformation.md)
