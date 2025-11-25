Instructions: https://webuzo.com/docs/admin/enable-xfs-quotas/

Run command 

` nano /etc/sysconfig/grub`

Append the "rootflags=uquota" in "GRUB_CMDLINE_LINUX=" line

> GRUB_CMDLINE_LINUX="crashkernel=auto rhgb quiet rootflags=uquota"

#### Note.: Keep previous record too inside GRUB_CMDLINE_LINUX= . Don't remove anything without having proper knowledge.

Rebuild the grub configuration file by executing following command.

` grub2-mkconfig -o /boot/grub2/grub.cfg` 

Reboot the server

If your OS is almalinux 9 and the above solution did not work, then execute the below command as root and reboot the server:

`grubby --args="rootflags=uquota" --update-kernel=ALL`


# Note.
Make a copy of the grub configuration file.

`cp -ax /boot/efi/EFI/almalinux/grub.cfg /boot/efi/EFI/almalinux/grub.cfg.$(date +%s)`

