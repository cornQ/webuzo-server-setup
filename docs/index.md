---
title: Webuzo Server Setup, Fixes, Migration and Troubleshooting Guides
description: Practical Webuzo server setup and troubleshooting documentation for OpenLiteSpeed, MySQL, FTP, email, migrations, resource limits, and AlmaLinux fixes.
---

<section class="home-hero">
  <p class="home-eyebrow">CORNQ Webuzo Documentation</p>
  <h1>Practical Webuzo fixes for real server issues.</h1>
  <p class="home-lede">Step-by-step notes for OpenLiteSpeed, MySQL, FTP, email, migrations, resource limits, Backuply permissions, and AlmaLinux server setup.</p>
  <div class="home-actions">
    <a class="home-button home-button--primary" href="webuzo-openlitespeed-suddenly-stopped-working-fix/">Start troubleshooting</a>
    <a class="home-button" href="webuzo-migration-from-cyber-panel/">Migration notes</a>
  </div>
</section>

<div class="guide-grid">
  <a class="guide-card" href="webuzo-openlitespeed-suddenly-stopped-working-fix/">
    <span class="guide-card__label">Web server</span>
    <strong>OpenLiteSpeed stopped</strong>
    <span>Check service status, test configs, inspect logs, and restart safely.</span>
  </a>
  <a class="guide-card" href="webuzo-ftp-file-transfer-issue-solved/">
    <span class="guide-card__label">FTP</span>
    <strong>Passive port issues</strong>
    <span>Fix upload, download, and directory listing failures through CSF ports.</span>
  </a>
  <a class="guide-card" href="webuzo-mailbaby-configuration/">
    <span class="guide-card__label">Email</span>
    <strong>MailBaby relay setup</strong>
    <span>Configure Exim custom code for authenticated outbound delivery.</span>
  </a>
  <a class="guide-card" href="webuzo-disable-sql-full-group-by/">
    <span class="guide-card__label">Database</span>
    <strong>MySQL SQL mode fix</strong>
    <span>Resolve ONLY_FULL_GROUP_BY compatibility issues in Webuzo-hosted apps.</span>
  </a>
</div>

<h2>Quick Links</h2>

<div class="resource-grid">
  <a class="resource-link" href="https://webuzo.com/docs/" target="_blank" rel="noopener">
    <strong>Official Webuzo Docs</strong>
    <span>Vendor reference and admin documentation</span>
  </a>
  <a class="resource-link" href="https://portal.cornq.com/knowledge-base/" target="_blank" rel="noopener">
    <strong>CORNQ Knowledge Base</strong>
    <span>Related hosting and support articles</span>
  </a>
  <a class="resource-link" href="https://github.com/cornQ/webuzo-server-setup/" target="_blank" rel="noopener">
    <strong>Contribute on GitHub</strong>
    <span>Improve or correct these guides</span>
  </a>
  <a class="resource-link" href="https://portal.cornq.com/knowledge-base/index.php?fuse=support&controller=ticket&view=submitticket" target="_blank" rel="noopener">
    <strong>Submit Support Ticket</strong>
    <span>Get help from CORNQ support</span>
  </a>
</div>

!!! note
    This documentation is continuously updated. Solutions are compiled from support tickets, community contributions, trusted internet sources, and the official Webuzo documentation for reference.

!!! danger
    cornQ is not responsible for any issues or damages caused by applying the instructions in this documentation. Proceed at your own risk.
