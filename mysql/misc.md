# MySQL misc notes

## Disable foreign keys during DELETE

```
SET FOREIGN_KEY_CHECKS = 0;
 
DELETE ...

SET FOREIGN_KEY_CHECKS = 1;
```

## Calcultate database size

A specific database with a specific engine 

```
select table_schema, sum(round(data_length/1024/1024,2)) as total_size_mb from information_schema.tables where table_schema like 'gobbleguts' and engine like 'innodb' group by table_schema;
```

All databases

```
select table_schema, sum(round(data_length/1024/1024,2)) as total_size_mb from information_schema.tables group by table_schema;
```
