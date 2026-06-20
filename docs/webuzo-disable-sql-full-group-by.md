---
title: Disable SQL_FULL_GROUP_BY in MySQL and MariaDB on Webuzo
description: Fix SQL_FULL_GROUP_BY errors in MySQL and MariaDB servers managed through Webuzo.
focus_keyword: Disable SQL_FULL_GROUP_BY
keywords: Webuzo, MySQL, MariaDB, SQL_FULL_GROUP_BY, Webuzo Hosting Panel, Server Administration
---

# Disable ONLY_FULL_GROUP_BY in MySQL on Webuzo

Sometimes, we may get the following error, which prevents us from running our web app.

![webuzo-disable-sql-full-group-by](img/webuzo-sql-full-group-by-enabled.jpeg "webuzo-disable-sql-full-group-by")


Add/update the following line under the __[mysqld]__ section in `/etc/my.cnf` and then __restart__ the MySQL service.

```conf
SET GLOBAL sql_mode = 'STRICT_TRANS_TABLES,NO_ENGINE_SUBSTITUTION';
```
