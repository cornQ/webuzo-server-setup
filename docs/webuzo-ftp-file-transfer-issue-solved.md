---
title: Fix FTP File Transfer Issues in Webuzo
description: Troubleshoot FTP connection, passive mode, timeout, and file transfer problems in Webuzo.
focus_keyword: FTP Issues Webuzo
keywords: Webuzo, FTP Troubleshooting, FTP Issues, Webuzo Hosting Panel, Web Hosting, Server Administration
canonical: https://webuzo.cornq.net/webuzo-ftp-file-transfer-issue-solved/
author: CORNQ Technical Team
lastUpdated: 2026-06-20
---

# Fix Webuzo FTP Passive Port File Transfer Issues

Add the passive port range __30000-50000__ or __30000:50000__ to the `TCP_IN` and `TCP_OUT` sections in the CSF configuration.

This will solve the issue.

!!! note
    Sometimes, enabling the `30000:50000` port doesn't work. In that case, allow the following port range too.

__55000–60000__ or __55000:60000__
