# Predefined Transformations

**Predefined Transformations**\
Predefined transformations are field transformations based on the field type.\
For example, here is the definition of a predefined transformation that removes leading and trailing spaces from all fields of type **'varchar'** and **'nvarchar'**:

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

**Check and Transformation Statements**\
The **Check Statement** is used to verify if a field meets the transformation conditions.\
The **Transformation Statement** contains the definition of the transformation.

Several predefined transformations are defined in advance, but users can also create their own predefined transformations.\
Predefined transformations are used in regular transformations. When creating a new transformation, the user can select which predefined transformations should be applied.



| Predefined Transformation | Description                                                                                 |
| ------------------------- | ------------------------------------------------------------------------------------------- |
| Trim                      | Removes leading and trailing spaces from string fields (e.g., **varchar**, **nvarchar**).   |
| StringNULLToNA            | Converts **NULL** values in string fields to "NA".                                          |
| StringMaxT08000           | Trims string fields to a maximum length of 8000 characters.                                 |
| NumberNULLToZero          | Converts **NULL** values in numeric fields to zero.                                         |
| XmlToString               | Converts XML data type fields to string format.                                             |
| HierarchyToString         | Converts hierarchical data into a string representation.                                    |
| TimeToDatetime            | Converts time fields into datetime fields by appending a default date (e.g., "1900-01-01"). |
| BinaryToStr               | Converts binary data to a string format.                                                    |
| Anonymization             | Anonymizes data by replacing sensitive fields with generic or masked values.                |

**Applying Multiple Predefined Transformations**\
Multiple predefined transformations can be applied simultaneously. Below is an example of the result when multiple predefined transformations are applied to a single transformation field:

```sql
[FKART] = RTRIM(LTRIM(ISNULL([T1].[FKART], 'N.A.')))
```

