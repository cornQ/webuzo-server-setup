---
title: Fix OpenLiteSpeed Not Working in Webuzo
description: Troubleshoot and fix OpenLiteSpeed server issues in Webuzo with step-by-step recovery methods.
focus_keyword: OpenLiteSpeed Not Working
keywords: Webuzo, OpenLiteSpeed, Webuzo Hosting Panel, Linux Hosting, VPS Management, Web Hosting, Server Administration
---

# Fix OpenLiteSpeed Service Stopped in Webuzo

**Problem:**
OpenLiteSpeed service is shown as "stopped" in the Webuzo admin panel, and trying to restart or start it from the panel does not work. This can happen suddenly, possibly due to a configuration change or server issue. Here's how to resolve it using the command line.

## Steps to Resolve

### 1. **Check Service Status**
The first step is to check the status of OpenLiteSpeed. This will tell you if the service is truly stopped or if there's a miscommunication between Webuzo and the actual server service.

```bash
systemctl status lsws --no-pager || systemctl status lshttpd --no-pager
```

* **Explanation**: This command checks the status of the OpenLiteSpeed service. Depending on your setup, it could be named `lsws` or `lshttpd`. The `--no-pager` option ensures that the output is shown directly in the terminal, without needing pagination.

### 2. **Test Configuration**

Before restarting the service, test the OpenLiteSpeed configuration to ensure there are no errors in the configuration files that could prevent it from starting.

```bash
/usr/local/lsws/bin/openlitespeed -t
```

* **Explanation**: This command tests the OpenLiteSpeed configuration for errors. If there’s an issue with the configuration, this will help you identify it before attempting a restart.

### 3. **Check Logs**

Next, check the logs for any errors or clues as to why the service isn't starting.

```bash
journalctl -u lsws -n 80 --no-pager || journalctl -u lshttpd -n 80 --no-pager
```

* **Explanation**: This command shows the last 80 log entries related to the OpenLiteSpeed service. You can look for any error messages that might explain why the service isn't running.

### 4. **Check for Port Conflicts**

Check if any other process is using the default OpenLiteSpeed ports (80, 443, or 7080), as this could prevent OpenLiteSpeed from starting.

```bash
ss -ltnp | egrep ':80|:443|:7080'
```

* **Explanation**: This command checks if ports 80, 443, or 7080 are being used by any other processes. If these ports are already in use, you might need to stop the conflicting service or change OpenLiteSpeed's ports.

### 5. **Restart the Service**

If everything looks fine, you can now restart the OpenLiteSpeed service using the following command:

```bash
systemctl restart lsws || systemctl restart lshttpd
```

* **Explanation**: This command restarts the OpenLiteSpeed service. If `lsws` doesn’t work, it will try `lshttpd`. This is necessary because OpenLiteSpeed uses a systemd service, and a manual restart might be needed if Webuzo’s restart button fails to work.

## Final Notes

If Webuzo’s admin panel fails to restart the OpenLiteSpeed service, running the above commands manually will usually resolve the issue. The problem may occur due to a configuration issue, port conflict, or temporary service miscommunication.

After following these steps, your OpenLiteSpeed service should be up and running again!
