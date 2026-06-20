---
title: Allow Users to Delete Backuply Backup Files in Webuzo
description: Configure Backuply permissions and allow users to manage or delete backup files safely.
focus_keyword: Backuply Backup Files
keywords: Webuzo, Backuply, Backup Files, Webuzo Hosting Panel, Web Hosting, Server Administration
---

# Allow Webuzo Users to Delete Backuply Backup Files

The end user may take a backup in the Webuzo panel, but is unable to delete the file. In this case, the following solution will work. 

![backuply-delete-dashboard-for-user](img/backuply-delete-dashboard-for-user.png "backuply-delete-dashboard-for-user")


When the user tries to delete his/her backup, he/she gets the following error.

![backuply-user-cannot-delete-warning](img/backuply-user-cannot-delete-warning.png "backuply-user-cannot-delete-warning")


Run the following command to allow delete permission to the user for his/her backup.

```bash
backuply --enable-delete-backups
```

This will enable the delete option for Backuply in the end user panel.

> By default, the backup file deletion for the end user is restricted. 
