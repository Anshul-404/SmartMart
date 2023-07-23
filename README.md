IMPORTING DATABASE:
--------------------

-> Copy "smartmart.dmp" file to bin folder of your system's Oracle directory.

-> Use the following commands on Oracle SQL

```
create user grocery identified by grocery
grant resource,connect,dba to grocery
```

-> Use the following commands on Command Prompt (Administrator) -


```
cd path/to/oracle/bin/
imp grocery/grocery

Import data only (yes/no): no > no

Import file: EXPDAT.DMP > smartmart.dmp

Enter insert buffer size (minimum is 8192) 30720> 30720

Export file created by EXPORT:V11.02.00 via conventional path

Warning: the objects were exported by GROCERY, not by you

import done in WE8MSWIN1252 character set and AL16UTF16 NCHAR character set
import server uses AL32UTF8 character set (possible charset conversion)
List contents of import file only (yes/no): no > no

Ignore create error due to object existence (yes/no): no > no

Import grants (yes/no): yes > yes

Import table data (yes/no): yes > yes

Import entire export file (yes/no): no > yes
```
