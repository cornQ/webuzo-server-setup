---
title: Migrate Webuzo to Webuzo Using Root Access
description: Transfer hosting accounts between Webuzo servers using root credentials and migration tools.
focus_keyword: Webuzo to Webuzo Migration
keywords: Webuzo, Webuzo Migration, VPS Management, Web Hosting, Webuzo Hosting Panel, Server Administration
---

# Migrate Webuzo to Webuzo Using Root Password

Add the passive port range __30000:50000__ to the `TCP_IN` and `TCP_OUT` sections in the CSF configuration on both servers.

!!! info
    After updating the same in CSF settings, the FTP connection gets successful, and the import will be completed successfully
