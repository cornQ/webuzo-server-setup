---
title: Enable XFS Quotas for Webuzo on AlmaLinux 9
description: Enable XFS user quotas for Webuzo on AlmaLinux 9 by updating GRUB root flags and rebuilding boot configuration.
---

# Enable XFS Quotas for Webuzo on AlmaLinux 9

Follow this Webuzo official Instruction: [Enable XFS Quotas](https://webuzo.com/docs/admin/enable-xfs-quotas/)

Run command 

```bash
nano /etc/sysconfig/grub
```

Append the __rootflags=uquota__ in __GRUB_CMDLINE_LINUX=" .... "__ line

```conf
GRUB_CMDLINE_LINUX="crashkernel=auto rhgb quiet rootflags=uquota"
```

!!! danger
    Keep previous record too inside GRUB_CMDLINE_LINUX= . Don't remove anything without having proper knowledge or replace the whole line

Rebuild the grub configuration file by executing following command.

```bash
grub2-mkconfig -o /boot/grub2/grub.cfg
```

#### Reboot the server


!!! note
    If your OS is __almalinux 9__ and the above solution did not work, then execute the below command as root and reboot the server:

```bash
grubby --args="rootflags=uquota" --update-kernel=ALL
```


!!! tip
    Make a copy of the grub configuration file.

```bash
cp -ax /boot/efi/EFI/almalinux/grub.cfg /boot/efi/EFI/almalinux/grub.cfg.$(date +%s)
```
