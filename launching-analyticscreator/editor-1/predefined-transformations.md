# Predefined Transformations

Predefined transformations are the field transformations which are based on the field type.&#x20;

For example, there is the definition of predefined transformation which removes the leading and trailing spaces in all fields of type ‘varchar’ and ‘nvarchar’:

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

Check statement used to check if the field corresponds the transformation conditions.&#x20;

Transformation statement contains the transformation definition.&#x20;

There are several predefined transformations defined in advance, but the user can create the user's own predefined transformations.&#x20;

Predefined transformations will be used in regular transformations. When you create a new transformation, the user can select which predefined transformations should be used:

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

Multiple predefined transformations can be applied simultaneously. Below is an example of the result when predefined transformations are applied to a single transformation field:

```sql
[FKART] = RTRIM(LTRIM(ISNULL([T1].[FKART], 'N.A.')))
```

