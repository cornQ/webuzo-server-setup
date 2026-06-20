---
title: Fix User Directory Permissions in Webuzo
description: Resolve directory permission issues for hosting accounts in Webuzo with correct ownership settings.
focus_keyword: Fix Directory Permissions Webuzo
keywords: Webuzo, Directory Permissions, Webuzo Hosting Panel, Linux Hosting, Web Hosting, Server Administration
canonical: https://webuzo.cornq.net/webuzo-fix-directory-permission-for-user/
author: CORNQ Technical Team
lastUpdated: 2026-06-20
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

