---
title: Enable cGroups v2 in Webuzo on AlmaLinux
description: Enable cGroups v2 for Webuzo and run the Webuzo cron command when the official instructions do not fully apply the change.
---

# Enable cGroups v2 in Webuzo on AlmaLinux

Follow this Webuzo official Instruction: [How to enable cGroups v2](https://webuzo.com/docs/how-tos/how-to-enable-cgroups-v2/)

!!! tip
    If the instruction doesn't work, then follow the same guide and after that execute the following command :

```bash
/usr/local/emps/bin/php /usr/local/webuzo/cron.php 
```
