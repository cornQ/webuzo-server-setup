You can use the below provided CRON from Admin teminal to update the visitors count without clicking on `Update now` button from AWS panel.

`/usr/local/apps/perl/bin/perl /usr/local/apps/awstats/tools/awstats_updateall.pl now -awstatsprog=/usr/local/apps/awstats/wwwroot/cgi-bin/awstats.pl -configdir=/usr/local/apps/awstats/wwwroot/cgi-bin/` 
