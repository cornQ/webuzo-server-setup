---
title: Fix Webuzo FTP Passive Port File Transfer Issues
description: Resolve Webuzo FTP upload, download, and directory listing problems by allowing passive FTP port ranges in CSF firewall configuration.
---

# Fix Webuzo FTP Passive Port File Transfer Issues

Add the passive port range __30000-50000__ or __30000:50000__ to the `TCP_IN` and `TCP_OUT` sections in the CSF configuration.

This will solve the issue.

!!! note
    Sometimes, enabling the `30000:50000` port doesn't work. In that case, allow the following port range too.

__55000–60000__ or __55000:60000__
