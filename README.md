# _**PLUGGABLE DATABASE CREATION AND DELETION**_

The following codes ensures that the creation and deletion of a pluggable database and configuration so that it can be accessed through SQL developer

## **Creating Pluggable Database**

### _Creating_

the first step is to create a directory for the datafiles of your pluggable database

```sql
mkdir C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\plsql_class2024db\;
```
next is to create the Pdb

```sql
CREATE PLUGGABLE DATABASE plsql_class2024db
    ADMIN USER yv_plsqlauca IDENTIFIED BY thug1crew
    ROLES = (DBA)
    FILE_NAME_CONVERT = ('C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\PDBSEED\',
   'C:\APP\PREACHER\PRODUCT\18.0.0.1\ORADATA\XE\plsql_class2024db\');
```
![alt text](creation.JPG)

### _Able Usage_

Whne the Pdb is created it cannot be access or used immediately so it is need to be open using the following codes:

```sql

ALTER PLUGGABLE DATABASE plsql_class2024db OPEN;

SELECT name, open_mode from V$PDBS; --- this is to see if it is opened or ready to be used
```
![alt text](openpd.JPG)



