To optimize system resource limits, please add the following lines to your /etc/security/limits.conf file.

Open the limits configuration file by running:

`nano /etc/security/limits.conf`


Add the following lines to set the process limits for your user (replace webuzo_user with the actual username):

`webuzo_user   soft   nproc   4096`
`webuzo_user   hard   nproc   4096`


Additionally, some systems use configuration files under `/etc/security/limits.d/`, which may override the settings.
Check if the file `/etc/security/limits.d/90-nproc.conf` exists.
If it does, add the same entries for your user there as well:

`webuzo_user   soft   nproc   4096`
`webuzo_user   hard   nproc   4096`


This will ensure the process limits are correctly applied.

> Note.: This works for only Terminal (inside Webuzo). It doesn't work for SSH.


Verify the change running by following the command inside the user account,

`ulimit -u`
