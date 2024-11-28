---
noIndex: true
icon: rectangle-terminal
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

# Object scripts

Object scripts allow you to make direct changes to metadata in the AnalyticsCreator repository database, providing an easier alternative to using the AC interface. These scripts can be parameterized and used later for various tasks, such as renaming fields or executing other bulk operations directly on the repository database.

#### Add an Object Script

1. In the **navigation tree**, right-click **Object script** and click **Add object script**.
2. In the **Script name** box, enter the name of the script.
3. In the **Description** box, enter a description for the script.
4. In the **Object** dropdown, optionally select the AnalyticsCreator table. If selected, this script will be linked to a specific table and can be run from the context menu of that table in the navigation tree.
   * For example, if you create the object script for the `TRANSFORMATION` table, it can be executed from the "Run script" option in the transformation context menu.
   * Scripts without an object are independent of any table and will be listed under **Object scripts -> Table independent scripts**. These can be run from their respective context menus.
5. In the **Parameters** grid, add parameters:
   * **ParamNr**: Sequence number of the parameter.
   * **Parameter**: Name of the parameter.
   * **Default value**: Default value for the parameter.
6. In the **Statement** box, type or paste the SQL statement you want to use.
7. Press the **Check** button to test the code.
8. Press **Save** to save the script.

#### Folders for Scripts

* **All Scripts**: Right-click **All scripts** in the navigation tree to view all object scripts in your repository.
* **Table-independent Scripts**: Right-click **Table-independent scripts** in the navigation tree to view all scripts that are not tied to a specific table. These can be run from their "Run script" context menu.

#### List Object Scripts

You can view all object scripts in your repository, categorized by the AnalyticsCreator tables they relate to. To run an object script tied to a specific table, use the "Run script" context menu for that table in the navigation tree.

#### Running an Object Script

1. **Table-related Object Script**: Right-click the object in the navigation tree and select **Run script**.
   * For example, to run a script tied to the `TRANSFORMATION` table, right-click that table and select **Run script**.
2. **Table-independent Object Script**: Right-click the specific script under **Table-independent scripts** and select **Run script**.

* The **Run object script** window will appear.
* You can set optional parameters for the script.
* Click **Run script** to execute the script. If the script returns rows, they will be displayed in the result table.

**Note**: For more details, refer to the List and Search Objects section.
