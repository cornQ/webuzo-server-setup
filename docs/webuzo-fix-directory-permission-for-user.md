---
title: Fix Webuzo User Directory Permissions
description: Use Webuzo CLI commands to repair ownership and permissions for all users or a specific hosting account.
---

# Fix Webuzo User Directory Permissions

To fix permissions and ownership for all users, execute the following command:

```bash
webuzo --fix_user_dir --perms 
```

To fix permissions and ownership for a specific user, execute the following command:

!!! info
    Replace `{username}` with the user's username.

```bash
webuzo --fix_user_dir --users={username}
```


