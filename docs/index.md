---
title: Webuzo Server Setup, Fixes, Migration and Troubleshooting Guides
description: Practical Webuzo server setup and troubleshooting documentation for OpenLiteSpeed, MySQL, FTP, email, migrations, resource limits, and AlmaLinux fixes.
---

# Webuzo Server Setup, Fixes and Troubleshooting Guides

Welcome to the CORNQ Webuzo documentation hub for server setup, customization, migrations, and common hosting control panel fixes.

These guides cover practical Webuzo administration tasks including OpenLiteSpeed service issues, MySQL configuration, FTP passive port problems, email queue management, MailBaby setup, Backuply permissions, user resource limits, and AlmaLinux quota configuration.

<div class="grid-container">
  <a class="grid-box" href="webuzo-openlitespeed-suddenly-stopped-working-fix/">
    <div class="grid-icon">OLS</div>
    <div class="grid-title">OpenLiteSpeed Fix</div>
    <div class="grid-subtitle">Diagnose stopped services, logs, ports, and restarts</div>
  </a>
  <a class="grid-box" href="webuzo-ftp-file-transfer-issue-solved/">
    <div class="grid-icon">FTP</div>
    <div class="grid-title">FTP Passive Ports</div>
    <div class="grid-subtitle">Fix upload, download, and directory listing issues</div>
  </a>
  <a class="grid-box" href="webuzo-mailbaby-configuration/">
    <div class="grid-icon">SMTP</div>
    <div class="grid-title">MailBaby Setup</div>
    <div class="grid-subtitle">Configure authenticated outbound email relay</div>
  </a>
  <a class="grid-box" href="webuzo-disable-sql-full-group-by/">
    <div class="grid-icon">SQL</div>
    <div class="grid-title">MySQL SQL Mode</div>
    <div class="grid-subtitle">Resolve ONLY_FULL_GROUP_BY compatibility errors</div>
  </a>
</div>

<h2>Quick Links</h2>

<div class="grid-container">
  <a class="grid-box" href="https://webuzo.com/docs/" target="_blank" rel="noopener">
    <div class="grid-icon">Docs</div>
    <div class="grid-title">Official Webuzo Docs</div>
    <div class="grid-subtitle">Vendor reference and admin documentation</div>
  </a>
  <a class="grid-box" href="https://portal.cornq.com/knowledge-base/" target="_blank" rel="noopener">
    <div class="grid-icon">KB</div>
    <div class="grid-title">CORNQ Knowledge Base</div>
    <div class="grid-subtitle">Related hosting and support articles</div>
  </a>
  <a class="grid-box" href="https://github.com/cornQ/webuzo-server-setup/" target="_blank" rel="noopener">
    <div class="grid-icon">Git</div>
    <div class="grid-title">Contribute on GitHub</div>
    <div class="grid-subtitle">Improve or correct these guides</div>
  </a>
  <a class="grid-box" href="https://portal.cornq.com/knowledge-base/index.php?fuse=support&controller=ticket&view=submitticket" target="_blank" rel="noopener">
    <div class="grid-icon">Help</div>
    <div class="grid-title">Submit Support Ticket</div>
    <div class="grid-subtitle">Get help from CORNQ support</div>
  </a>
</div>

!!! note
    This documentation is continuously updated. Solutions are compiled from support tickets, community contributions, trusted internet sources, and the official Webuzo documentation for reference.

!!! danger
    cornQ is not responsible for any issues or damages caused by applying the instructions in this documentation. Proceed at your own risk.
