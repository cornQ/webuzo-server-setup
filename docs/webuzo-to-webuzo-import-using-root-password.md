---
title: Migrate Webuzo to Webuzo Using Root Password
description: Prepare source and destination Webuzo servers for migration by allowing passive FTP ports in CSF firewall configuration.
---

# Migrate Webuzo to Webuzo Using Root Password

Add the passive port range __30000:50000__ to the `TCP_IN` and `TCP_OUT` sections in the CSF configuration on both servers.

!!! info
    After updating the same in CSF settings, the FTP connection gets successful, and the import will be completed successfully
