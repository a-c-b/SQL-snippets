# SQL-snippets
This repo is to capture examples of SQL code which can be shared to demonstrate ability with Oracle SQL

Most views were created with a call to "Dates" which were the reporting period dates.  I adjusted in individual
views depending upon the health of the data stream.

```{sql}
create or replace view MSC_SUBNET_CONNECTIONS as 

WITH


DATES AS   (
    SELECT DATE1 - 7 as date1  FROM CIQ_DATES
--    SELECT trunc(sysdate-7) as date1 from dual
        )

,SUBNET_BASE AS (select * from (
            select 
```
