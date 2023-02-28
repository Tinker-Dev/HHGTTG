# QueryBand

QueryBand is a way to add session or transaction metadata. You add an extra bit of script to the top of
your query that will place some metadata in a table. This table and then be read by the DBA. Generally
this would be used if there is a runaway script that a DBA would need details on.

QueryBand is stored as Name|Value pairs. 

Example:
```SET QUERY BAND = 'name=value; name2=value2;' FOR SESSION|TRANSACTION```

To review what is stored, if you have the rights.
```SELECT * FROM DBC.DBQLOGTBL```
