# Webuzo Server Setup Documentation

Public Webuzo server setup, troubleshooting, migration, mail, FTP, database, OpenLiteSpeed, and server administration guides by CORNQ.

Live documentation: https://webuzo.cornq.net

## Topics

### Home

- [Webuzo Server Setup, Fixes and Troubleshooting Guides](docs/index.md)

### System Setup

- [Enable CPgroups v2 in Alma9](docs/webuzo-enable-cpgroups-v2.md)
- [Enable XFS Quotas Alma9](docs/webuzo-enable-xfs-quotas-almalinux9.md)
- [Change Hostname Default Page](docs/webuzo-hostname-default-page-changing.md)
- [Awstats Cron Setup](docs/webuzo-awstat-cron-setup.md)
- [OpenLiteSpeed Suddenly Stopped Working](docs/webuzo-openlitespeed-suddenly-stopped-working-fix.md)
- [Install PHP Composer Manually](docs/webuzo-install-php-composer.md)

### Database & Cache

- [Disable SQL Full Group](docs/webuzo-disable-sql-full-group-by.md)
- [Increase SQL Upload Size](docs/webuzo-increase-sql-upload-size.md)
- [Clear OLS Cache](docs/webuzo-openlitespeed-cache-clean.md)

### User & Resources

- [Check User Resource Limits](docs/webuzo-check-resource-limit-from-end-user-terminal.md)
- [Increase Terminal Max Processes](docs/webuzo-increase-terminal-max-processes-for-a-specific-user.md)
- [Fix User Directory Permissions](docs/webuzo-fix-directory-permission-for-user.md)
- [Enable User to Delete Backup Files](docs/webuzo-allow-user-to-delete-backuply-backup-files.md)

### Mail & FTP

- [MailBaby Configuration with Webuzo](docs/webuzo-mailbaby-configuration.md)
- [Webmail Default URL](docs/webuzo-webmail-default-login-url.md)
- [Fix FTP Issues](docs/webuzo-ftp-file-transfer-issue-solved.md)
- [Email Queue Cleaning](docs/webuzo-email-queue-clean.md)

### Migrations

- [Migrate from CyberPanel](docs/webuzo-migration-from-cyber-panel.md)
- [Migrate from Webuzo via root](docs/webuzo-to-webuzo-import-using-root-password.md)

### Others

- [Webuzo Mirror Network](docs/webuzo-mirror-network-info.md)

## Contributing

Contributions are welcome and appreciated. If you find a typo, outdated command, missing safety note, unclear explanation, or a Webuzo issue that should be documented, please open a pull request.

Helpful contributions include:

- correcting commands or screenshots
- improving step-by-step explanations
- adding tested fixes from real support cases
- updating links to official Webuzo documentation
- adding new troubleshooting pages that match the existing style

Your contribution can help other Webuzo users solve server issues faster.

### Project Structure

Use the existing project files when contributing:

- `docs/*.md` - documentation pages
- `docs/index.md` - documentation homepage
- `mkdocs.yml` - MkDocs configuration, sidebar navigation, theme settings, and plugins
- `docs/sitemap.xml` - published sitemap for `https://webuzo.cornq.net/sitemap.xml`
- `docs/llms.txt` - published AI discovery file for `https://webuzo.cornq.net/llms.txt`
- `llms.txt` - repository-level AI discovery file
- `docs/robots.txt` - robots file with sitemap reference
- `docs/img/` - screenshots, favicon, and image assets
- `docs/css/style.css` - custom site styling
- `docs/CNAME` - custom GitHub Pages domain
- `.github/workflows/deploy.yml` - GitHub Pages deployment workflow

### Fork and Clone

1. Fork the repository on GitHub if you do not have write access.
2. Clone your fork or the main repository:

```bash
git clone https://github.com/cornQ/webuzo-server-setup.git
cd webuzo-server-setup
```

3. If you cloned a fork, keep the upstream repository available:

```bash
git remote add upstream https://github.com/cornQ/webuzo-server-setup.git
git fetch upstream
```

### Create a Branch

Create a new branch before editing files:

```bash
git checkout -b docs/short-description
```

Recommended branch naming:

- `docs/add-topic-name`
- `docs/update-topic-name`
- `docs/fix-topic-name`
- `seo/update-metadata-topic-name`
- `assets/add-screenshot-topic-name`

Examples:

- `docs/add-webuzo-ssl-guide`
- `docs/update-mailbaby-config`
- `docs/fix-ftp-passive-ports`
- `seo/update-openlitespeed-metadata`

### Create a New Documentation Page

1. Create a new markdown file in `docs/`.
2. Use lowercase words separated by hyphens.
3. Add SEO front matter at the top.
4. Add the page to `mkdocs.yml` under the correct `nav` section.
5. Add the page URL to `docs/sitemap.xml`.
6. Update `docs/llms.txt` and `llms.txt` if the new page introduces a new major topic.
7. Update `docs/index.md` only if the new page should be featured on the homepage.

Sample filename:

```txt
docs/webuzo-example-topic.md
```

Complete sample documentation file:

````md
---
title: Example Webuzo Documentation Page
description: Short description of the Webuzo task, issue, or setup covered by this page.
focus_keyword: Example Webuzo Topic
keywords: Webuzo, Webuzo Documentation, Webuzo Tutorial, Server Administration
canonical: https://webuzo.cornq.net/webuzo-example-topic/
author: CORNQ Technical Team
lastUpdated: 2026-06-20
---

# Example Webuzo Documentation Page

Briefly describe the issue, task, or setup this page covers.

## Steps

1. First step.
2. Second step.
3. Third step.

```bash
example-command
```

!!! note
    Add safety notes only when they are useful and accurate.
````

### Edit an Existing Documentation Page

1. Open the relevant file in `docs/`.
2. Keep commands, paths, screenshots, warnings, notes, and examples accurate.
3. Do not change technical guidance unless you have tested or verified the change.
4. If the page title, URL, or intent changes, update the front matter metadata.
5. If screenshots change, place replacement images in `docs/img/` and update image references.

### Rename a Documentation Page

1. Rename the markdown file in `docs/`.
2. Update the matching page entry in `mkdocs.yml`.
3. Update the old URL in `docs/sitemap.xml`.
4. Update any links in `README.md`, `docs/index.md`, or other docs pages that point to the old file.
5. Update the page `canonical` value in the markdown front matter.
6. Update `docs/llms.txt` and `llms.txt` if the renamed page changes a major topic label.

### Delete a Documentation Page

Only delete a page when the information is obsolete, duplicated, unsafe, or intentionally retired.

1. Delete the markdown file from `docs/`.
2. Remove the page from `mkdocs.yml`.
3. Remove the URL from `docs/sitemap.xml`.
4. Remove links to the page from `README.md`, `docs/index.md`, and any other docs pages.
5. Update `docs/llms.txt` and `llms.txt` if the deleted page represented a major topic.

### Update Navigation and Sidebar

The sidebar is controlled by the `nav` section in `mkdocs.yml`.

When adding, renaming, moving, or deleting a page:

1. Find the correct section in `mkdocs.yml`.
2. Add or update the page label and markdown filename.
3. Keep labels short and clear.
4. Do not create a new section unless the topic does not fit an existing section.

Current navigation sections:

- `Home`
- `System Setup`
- `Database & Cache`
- `User & Resources`
- `Mail & FTP`
- `Migrations`
- `Others`

### Update sitemap.xml

The sitemap file is `docs/sitemap.xml`.

When adding a page, add a new URL entry:

```xml
<url>
  <loc>https://webuzo.cornq.net/webuzo-example-topic/</loc>
  <lastmod>2026-06-20</lastmod>
  <priority>0.8</priority>
</url>
```

When renaming or deleting a page, update or remove the matching `<url>` block.

### Update llms.txt

This project has two AI discovery files:

- `docs/llms.txt` for the published website
- `llms.txt` for the repository

Update both files only when a contribution adds, removes, or renames a major documentation topic. Do not add every small page title to `llms.txt`.

### Update Documentation Index Files

The documentation homepage is:

```txt
docs/index.md
```

Update it only when:

- a new page should be featured under homepage cards
- a resource link changes
- the homepage description no longer reflects the docs

The image folder also has:

```txt
docs/img/README.md
```

Do not edit it unless you are documenting image assets.

### Test Locally

Install MkDocs Material if needed:

```bash
pip install mkdocs-material
```

Build the site:

```bash
mkdocs build --strict
```

Run a local server:

```bash
mkdocs serve
```

Open:

```txt
http://127.0.0.1:8000
```

Before submitting, check:

- the page appears in the sidebar
- internal links work
- code blocks render correctly
- screenshots load correctly
- sitemap changes are valid XML
- no unrelated files changed

### Commit Message Examples

Use short, specific commit messages:

```txt
Add Webuzo SSL documentation
Update MailBaby configuration guide
Fix FTP passive port instructions
Add screenshot for Backuply delete option
Update sitemap for new Webuzo guide
Fix metadata for OpenLiteSpeed page
```

### Create a Pull Request

1. Push your branch:

```bash
git push origin docs/short-description
```

2. Open a pull request on GitHub.
3. In the pull request, explain:
   - what page changed
   - why the change is needed
   - whether commands or screenshots were tested
   - which files were added, renamed, or deleted
4. Wait for review and address feedback.

### Contributor Checklist

Before opening a pull request, confirm:

- [ ] I edited only the files required for this change.
- [ ] I used the existing `docs/` structure.
- [ ] I added or updated front matter metadata when needed.
- [ ] I updated `mkdocs.yml` if navigation changed.
- [ ] I updated `docs/sitemap.xml` if URLs changed.
- [ ] I updated `docs/llms.txt` and `llms.txt` if major topics changed.
- [ ] I updated `docs/index.md` only if the homepage needed the change.
- [ ] I placed images in `docs/img/` if screenshots were added.
- [ ] I verified commands and technical guidance where possible.
- [ ] I ran `mkdocs build --strict` or explained why I could not.
- [ ] I checked that no unrelated files were modified.
