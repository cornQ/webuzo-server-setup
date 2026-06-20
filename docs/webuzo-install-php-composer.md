---
title: Install PHP Composer in Webuzo Server
description: Learn how to install and configure Composer for PHP applications on a Webuzo server.
focus_keyword: Install Composer Webuzo
keywords: Webuzo, PHP Composer, Webuzo Tutorial, Linux Hosting, VPS Management, Web Hosting, Server Administration
---

# Install PHP Composer Manually in Webuzo

### How do I install PHP Composer in Webuzo?
Currently, it's not possible to install the PHP Composer from the __App Install__ function in Webuzo. However, it's possible to install it manually on the server using the following commands.

Step 01: Download the composer's files through the following command,

```bash
curl -sS https://getcomposer.org/installer | php
```

Step 02: Move the downloaded files to the proper place,

```bash
mv composer.phar /usr/bin/composer
```
Step 03: Create symlink

```bash
ln -s /usr/bin/composer /etc/alternatives/composer
```

Verify the installation with:

```bash
composer -V
```

### Is it safe to install PHP Composer in a shared hosting environment with Webuzo? 

Yes, Composer is safe to use in a shared hosting environment and is commonly used for managing PHP dependencies.
