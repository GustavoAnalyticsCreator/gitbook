# Source Wizard

The **Source Wizard** is used to add new data sources to the repository. To launch the Source Wizard, right-click on the **“Sources”** branch of a connector in the context menu and select **“Add Source.”**

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

The appearance and functionality of the Source Wizard will vary depending on the selected source type (Table or Query):

**Table:**\
When selecting **Table** as the data source, the wizard provides options to configure and view available tables.

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

#### **Configuring a Table Data Source**

When selecting **“Table”** as the data source in the **Source Wizard**, click the **“Apply”** button to display the list of available source tables. Optionally, you can enter a schema or table filter to refine the results.

**Configuration Options**

* **Retrieve Relations**: Enables the retrieval of relationships for the selected source table, if available.
* **SAP Description Language**: Specifies the language for object descriptions when working with SAP sources.
* **SAP DeltaQ Attributes**: For SAP DeltaQ sources, additional DeltaQ-specific attributes must be defined.

#### **Configuring a Query as a Data Source**

When selecting **“Query”** as the data source in the **Source Wizard**, follow these steps:

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

1. **Define Schema and Name**: Specify the schema and name of the source for the repository.
2. **Enter the Query**: Provide the query in the query language supported by the data source.
3. **Test the Query**: Click the **“Test Query”** button to verify its validity and ensure it retrieves the expected results.
4. **Complete the Configuration**: Click the **“Finish”** button to add the new source to the repository. The source definition window will open, allowing further modifications if needed.

The result is&#x20;

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>
