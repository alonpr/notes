### alert log
```
select * from V$DIAG_INFO;
```
```
select * from X$DBGALERTEXT;
```
```
$ adrci
> show alert
> show problem
> show incident
```

### autotrace
```
SET AUTOTRACE OFF             - No AUTOTRACE report is generated. This is the default. 
SET AUTOTRACE ON EXPLAIN      - The AUTOTRACE report shows only the optimizer execution path. 
SET AUTOTRACE ON STATISTICS   - The AUTOTRACE report shows only the SQL statement execution statistics. 
SET AUTOTRACE ON              - The AUTOTRACE report includes both the optimizer execution path and the SQL statement execution statistics. 
SET AUTOTRACE TRACEONLY       - Like SET AUTOTRACE ON, but suppresses the printing of the user's query output, if any. If STATISTICS is enabled, query data is still fetched, but not printed. 

recursive calls                            - Number of recursive calls generated at both the user and system level. Oracle Database maintains tables used for internal processing. When Oracle Database needs to make a change to these tables, it internally generates an internal SQL statement, which in turn generates a recursive call. 
db block gets                              - Number of times a CURRENT block was requested. 
consistent gets                            - Number of times a consistent read was requested for a block 
physical reads                             - Total number of data blocks read from disk. This number equals the value of "physical reads direct" plus all reads into buffer cache. 
redo size                                  - Total amount of redo generated in bytes 
bytes sent through SQL*Net to client       - Total number of bytes sent to the client from the foreground processes. 
bytes received through SQL*Net from client - Total number of bytes received from the client over Oracle Net. 
SQL*Net round-trips to/from client         - Total number of Oracle Net messages sent to and received from the client 
sorts (memory)                             - Number of sort operations that were performed completely in memory and did not require any disk writes 
sorts (disk)                               - Number of sort operations that required at least one disk write 
rows processed                             - Number of rows processed during the operation 
```