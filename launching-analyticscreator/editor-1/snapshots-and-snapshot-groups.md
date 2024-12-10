# Snapshots and snapshot groups

Snapshots are the predefined dates which will be calculated during the ETL process and used in the Snapshot-Transformations to combine the historicized data. There is always at least one Snapshot called “Actual date” – the value of this Snapshot is the current timestamp. You can define more snapshots. There is a typical snapshot definition:

Each snapshot name should be unique. The SQL statement will be used to calculate the snapshot value. There is one predefined variable @ActDate which the user can use in this statement – the value of this variable is the current timestamp. Several snapshots can be combined in snapshot groups:

If you work with several snapshots the user can define the Snapshot-Dimension and use it as a common dimension in the data mart layer. To create snapshot dimension, please use according context menu:

Snapshots are used in the regular snapshot transformations:

You can use as both snapshot groups and snapshots. All selected snapshots will be used in transformation.
