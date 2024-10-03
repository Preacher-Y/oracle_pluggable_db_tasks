# _**PLUGGABLE DATABASE CREATION AND DELETION**_

The following codes ensures that the creation and deletion of a pluggable database and configuration so that it can be accessed through SQL developer

## **Creating Pluggable Database**

the first step is to create a directory for the datafiles of your pluggable database

```sql
mkdir C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\plsql_class2024db\;
```
next is to create the Pdb

```sql
SQL> CREATE PLUGGABLE DATABASE plsql_class2024db
  2  ADMIN USER yv_plsqlauca IDENTIFIED BY thug1crew
  3  ROLES = (DBA)
  4  FILE_NAME_CONVERT = ('C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\PDBSEED\',
  5 'C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\plsql_class2024db\');
```


