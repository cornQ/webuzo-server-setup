---
title: Configure AWStats Cron Job in Webuzo
description: Complete guide to setting up AWStats cron jobs in Webuzo for automatic website traffic reporting.
focus_keyword: AWStats Cron Setup Webuzo
keywords: Webuzo, AWStats, Cron Job, Webuzo Tutorial, Web Hosting, Server Administration, Linux Hosting
canonical: https://webuzo.cornq.net/webuzo-awstat-cron-setup/
author: CORNQ Technical Team
lastUpdated: 2026-06-20
---

# Set Up AWStats Cron in Webuzo

You can use the below provided CRON from Admin terminal to update the visitors count without clicking on __Update now__ button from AWStats panel.

```bash
/usr/local/apps/perl/bin/perl /usr/local/apps/awstats/tools/awstats_updateall.pl now -awstatsprog=/usr/local/apps/awstats/wwwroot/cgi-bin/awstats.pl -configdir=/usr/local/apps/awstats/wwwroot/cgi-bin/
```
