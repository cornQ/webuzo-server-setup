---
title: How to Clean Email Queue in Webuzo
description: Manage and clear email queues in Webuzo to resolve stuck or delayed outgoing emails.
focus_keyword: Clean Email Queue Webuzo
keywords: Webuzo, Email Queue, Email Configuration, Webuzo Hosting Panel, Web Hosting, Server Administration
canonical: https://webuzo.cornq.net/webuzo-email-queue-clean/
author: CORNQ Technical Team
lastUpdated: 2026-06-20
---

# Clean Email Queue in Webuzo

### From panel

Go to **Webuzo Admin Panel > Email > Email Queue Manager**.

There you can:

- Select emails and click **Delete Selected**
- Or click **Delete All** to clear the whole queue

### From command line as root

Run the following CLI command for clearing the email queue.

```bash
webuzo --delete_email_queue
```

!!! danger 
    Deleting queue entries is irreversible and cannot be undone!

Running the following command will show how many messages are in the queue.

```bash
exim -bpc
```
