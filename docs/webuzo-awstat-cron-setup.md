---
title: Set Up AWStats Cron in Webuzo
description: Add a Webuzo AWStats cron command to update visitor statistics automatically from the admin terminal.
---

# Set Up AWStats Cron in Webuzo

You can use the below provided CRON from Admin terminal to update the visitors count without clicking on __Update now__ button from AWStats panel.

```bash
/usr/local/apps/perl/bin/perl /usr/local/apps/awstats/tools/awstats_updateall.pl now -awstatsprog=/usr/local/apps/awstats/wwwroot/cgi-bin/awstats.pl -configdir=/usr/local/apps/awstats/wwwroot/cgi-bin/
```
