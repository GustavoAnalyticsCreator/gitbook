---
icon: gear
---

# Transformations

Transformation is the way to modify the data. The result of the transformation is always a single **VIEW** or a single **TABLE**.&#x20;

To create a new transformation, you should use the [Transformation wizard](transformation-wizard.md) .&#x20;

There are some common properties for each transformation:&#x20;

1. **Name:** transformation name&#x20;
2. [**Schema:**](schemas.md) transformation schema&#x20;
3. **TransType:** transformation type&#x20;
4. [**Stars:**](stars.md) List of stars in which the transformation takes in&#x20;
   1. **Star:** Star name&#x20;
   2. **IsFact:** should be selected for fact transformations&#x20;
   3. **Filter:** You can define additional filter to restrict transformation data for specific data mart

### AnalyticsCreator supports different transformation types:

[Regular transformation](regular-transformation.md)

[Manual transformation](manual-transformation.md)

[External transformation](external-transformation.md)

[Script transformation](script-transformation.md)

[Data mart transformation](data-mart-transformation.md)
