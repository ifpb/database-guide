# Admin

<!-- 
TODO Architecture MySQL
![]() 
-->

## Commands
---

### security recommendations

```
$ mysql_secure_installation
```

### Connection (mysql cli)

**mysql -u [username] -p**
```
$ mysql -u root -p
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 56
Server version: 5.5.59-0ubuntu0.14.04.1 (Ubuntu)

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

**mysql -h[host] -P[port] -u[username] -p[password]**
```
$ mysql -h127.0.0.1 -P3306 -uroot -pabc123
mysql: [Warning] Using a password on the command line interface can be insecure.
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 57
Server version: 5.5.59-0ubuntu0.14.04.1 (Ubuntu)

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

### Backup

#### Export

**mysqldump -u [username] -p [database] > [database]_backup.sql**
```
$ mysqldump -u root -p monitor_db > monitor_db_backup.sql
```

```
$ mysqldump -u root -p --no-create-info monitor_db > monitor_db_backup.sql # data only
$ mysqldump -u root -p --no-data monitor_db > monitor_db_backup.sql # structure only
$ mysqldump -u root -p --all-databases > database_backup.sql # database
```

#### Import

**mysql -u [username] -p [database] < database_backup_backup.sql**
```
$ mysql -u root -p database < database_backup_backup.sql
```

## [VSCode MySQL](https://marketplace.visualstudio.com/items?itemName=formulahendry.vscode-mysql)
---

![](https://github.com/formulahendry/vscode-mysql/raw/master/images/connection.png)

## [MySQL Workbench](https://www.mysql.com/products/workbench/)
---

### Design

### Admin

### Export

### Import