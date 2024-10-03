# Ngabo-Angelos-pluggable-database

```sql
[UploaMicrosoft Windows [Version 10.0.22621.4037]
(c) Microsoft Corporation. All rights reserved.

C:\Users\ngabo>sqlplus / as sysdba

SQL*Plus: Release 21.0.0.0.0 - Production on Thu Oct 3 18:38:37 2024
Version 21.3.0.0.0

Copyright (c) 1982, 2021, Oracle.  All rights reserved.


Connected to:
Oracle Database 21c Enterprise Edition Release 21.0.0.0.0 - Production
Version 21.3.0.0.0

SQL> create pluggable database plsql_class2024db
  2  admin user pdbadmin identified by admin
  3  file_name_convert=('C:\Users\ngabo\OneDrive\Desktop\oradata\ORCL\pdbseed\','C:\Users\ngabo\OneDrive\Desktop\oradata\ORCL\plsql_class2024db\');

Pluggable database created.

SQL> alter session set container=plsql_class2024db;

Session altered.

SQL> create user ng_plsqlauca identified by ngabo;
create user ng_plsqlauca identified by ngabo
*
ERROR at line 1:
ORA-01109: database not open


SQL> alter pluggable database plsql_class2024db open;

Pluggable database altered.

SQL> alter pluggable database plsql_class2024db save state;

Pluggable database altered.

SQL> create user ng_plsqlauca identified by ngabo;

User created.

SQL> grant all privileges to ng_plsqlauca;

Grant succeeded.

SQL> alter session set container=cdb$root;

Session altered.

SQL> create pluggable database ng_to_delete_pdb
  2  from orclpdb
  3  file_name_convert=('C:\Users\ngabo\OneDrive\Desktop\oradata\ORCL\orclpdb\','C:\Users\ngabo\OneDrive\Desktop\oradata\ORCL\ng_to_delete_pdb');

Pluggable database created.

SQL> alter pluggable database ng_to_delete_pdb open;

Pluggable database altered.

SQL> alter pluggable database ng_to_delete_pdb close immediate;

Pluggable database altered.

SQL> alter pluggable database ng_to_delete_pdb unplug into 'C:\Users\ngabo\OneDrive\Desktop\admin\orcl\dpdump\ ng_to_delete_pdb.xml';

Pluggable database altered.

SQL> drop pluggable database ng_to_delete_pdb;

Pluggable database dropped.

SQL> show pdbs;

    CON_ID CON_NAME                       OPEN MODE  RESTRICTED
---------- ------------------------------ ---------- ----------
         2 PDB$SEED                       READ ONLY  NO
         3 ORCLPDB                        READ WRITE NO
         4 PLSQL_CLASS2024DB              READ WRITE NO![Per](https://github.com/user-attachments/assets/ea48054c-7085-4a91-95d2-c916f9f9f40c)

```
![Per](https://github.com/user-attachments/assets/429c7207-e815-4627-a6e3-b922df05400e)
![Per 2](https://github.com/user-attachments/assets/261be972-66ec-4b58-95b8-2139ce5a5115)



