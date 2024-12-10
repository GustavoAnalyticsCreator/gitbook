# Calendar transformation wizard

To create calendar transformation please select the diagram context menu “Add-> Calendar dimension”.

Calendar transformation wizard will be opened. Usually you need only one calendar transformation in the data warehouse.

Parameters: Schema: Schema of calendar transformation Name: Name of calendar transformation Date from: Calendar start date Date to: Calendar end date Date-to-ID function: Name of the macro which will transform a DateTime value to the key value of the calendar dimension. You can use this macro, for example, in the fact transformations to convert datetime fields into calendar dimension members. Stars: You can select the data mart stars where the calendar transformation will be present
