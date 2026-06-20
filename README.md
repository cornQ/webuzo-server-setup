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

### Contribute with the Help of AI

This project welcomes AI-assisted contributions. Contributors may use AI tools such as ChatGPT, Codex, Claude Code, Gemini, Cursor, Windsurf, or similar assistants to help create, update, improve, or maintain documentation.

AI can significantly reduce the time required to write documentation, update metadata, review consistency, and maintain project structure. However, contributors remain fully responsible for reviewing and validating all AI-generated changes before submitting a pull request.

#### Before Using AI

Before asking an AI assistant to make changes:

1. Clone the repository.
2. Create a dedicated branch.
3. Review the existing documentation structure.
4. Understand the page or section you want to modify.
5. Identify any related files that may also need updates.
6. Provide sufficient context to the AI assistant.

#### AI Contribution Rules

When using AI, contributors must follow these rules:

- Preserve technical accuracy.
- Preserve existing documentation structure.
- Preserve code blocks unless changes are required.
- Preserve commands unless changes are required.
- Preserve comments and internal notes.
- Avoid marketing language.
- Avoid unsupported technical claims.
- Avoid generating fictional information.
- Avoid introducing unnecessary content.
- Keep documentation clear, accurate, and maintainable.

Any AI-generated content should match the style and structure already used throughout the project.

#### Recommended AI Workflow

1. Clone the repository.
2. Create a new branch.
3. Open your preferred AI assistant.
4. Provide repository context.
5. Explain the task clearly.
6. Review the proposed changes.
7. Verify all affected files.
8. Test locally if applicable.
9. Commit your changes.
10. Push the branch.
11. Open a pull request.

#### Universal AI Contribution Prompt

You can use the following prompt with ChatGPT, Codex, Claude Code, Gemini, Cursor, Windsurf, or similar tools.

```text
You are contributing to an existing technical documentation project.

Repository:
[PASTE REPOSITORY URL]

Task:
[DESCRIBE THE CHANGE]

Requirements:

1. Review the existing project structure before making changes.

2. Follow the existing documentation style and formatting.

3. Do not rewrite unrelated content.

4. Do not modify comments.

5. Do not modify internal notes.

6. Do not modify hidden instructions.

7. Preserve code blocks unless the task explicitly requires changes.

8. Preserve commands unless the task explicitly requires changes.

9. Preserve technical accuracy.

10. If creating a new documentation page:
    - Follow the existing page structure.
    - Follow the existing naming convention.
    - Add required metadata.
    - Add navigation references if required.
    - Update sitemap.xml if required.
    - Update llms.txt if required.
    - Update any navigation, sidebar, index, or configuration files that reference documentation pages.

11. If editing an existing page:
    - Keep formatting consistent.
    - Preserve existing examples.
    - Preserve existing commands.
    - Preserve screenshots and references.

12. If renaming a page:
    - Update all internal links.
    - Update navigation references.
    - Update sitemap entries.
    - Update related documentation references.

13. If deleting a page:
    - Remove navigation references.
    - Remove sitemap references.
    - Remove related links.
    - Ensure no broken references remain.

14. Do not invent files that do not exist.

15. Before making changes:
    - Inspect the repository.
    - Identify all affected files.
    - Create a change plan.

16. After making changes:
    - List all modified files.
    - Explain why each file was modified.
    - Verify that no unrelated files were changed.

17. Maintain consistency across the entire documentation project.

Goal:

Implement the requested documentation change while preserving project quality, technical accuracy, navigation integrity, metadata consistency, and overall maintainability.
```

#### AI Review Checklist

Before submitting a pull request, verify:

- Documentation remains technically accurate.
- No unrelated content was modified.
- Navigation remains functional.
- Internal links work correctly.
- Metadata remains consistent.
- Sitemap entries are correct.
- Documentation structure remains consistent.
- No placeholder content exists.
- No AI-generated filler content exists.
- No unsupported technical claims were introduced.

#### Important Note

AI should assist contributors, not replace contributor responsibility. Every contributor is responsible for reviewing, validating, and testing AI-generated changes before opening a pull request.

Never merge changes that have not been reviewed by a human.

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
