---
title: Programming
layout: page
content:
    - index
---

MY-SQL
=====

Creating tables with many varchar fields kann lead to the following error:

ERROR Reason: liquibase.exception.DatabaseException: (conn=9) Row size too large (> 8126). Changing some columns to TEXT or BLOB may help. In current row format, BLOB prefix of 0 bytes is stored inline.

https://mariadb.com/kb/en/troubleshooting-row-size-too-large-errors-with-innodb/

```
SET SESSION innodb_strict_mode=OFF;
```

SNIPPETS
========

Calculate duration from two timestamps.

https://stackoverflow.com/questions/4759248/difference-between-two-dates-in-mysql/20419537

```
select count(*), TIMESTAMPDIFF(SECOND, started, finished) as 'duration in seconds' from TABLE_NAME
```
