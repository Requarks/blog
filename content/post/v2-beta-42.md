---
categories:
- Updates
date: "2019-02-20"
description: What's new in Wiki.js v2 BETA Build 42...
image: images/unsplash-spikes.jpg
slug: v2-beta-42
tags:
- updates
title: Wiki.js v2 BETA (Build 42)
---

A new build of Wiki.js v2 BETA is now available: Build 42.

## What's New
### MySQL, MariaDB and MSSQL support
The initial beta had issues with DBs that were not PostgreSQL. This is now fixed. MariaDB, MySQL, MSSQL and PostgreSQL are now fully supported. Note that SQLite requires some more development and should be working in the next beta!

### Redis is no longer necessary
The Redis requirement has been removed. You now only need a database to run Wiki.js! Redis ended up not being used enough to warrant having it as a dependency. The few parts that were relying on it were re-engineered to use in-memory mechanisms instead.

### Delete Page feature
You can now delete any page from the dropdown menu found at the top left of the page (if you have access). Even though the history feature is not yet available, deleted pages are still kept in the DB and you'll be able to restore them when the feature is ready!.

### Theme Code Injection (CSS/JS)
You can now inject your own CSS or Javascript tags in all pages of your wiki from the **Administration Area**. Located in the **Themes** section, use the CSS Override, Head HTML Injection or Body HTML Injection fields to insert your code.

### Local disk + Git integration *(work in progress)*
The **Local File System** and **Git** storage module are now available for use.

The **Local File System** module simply writes content as files on the local disk. Note that the daily backups option is not yet working. This module is limited to push synchronization only for now, meaning it won't pick up changes made outside Wiki.js.

The **Git** module offers full integration with remote Git repositories (as found in v1). However, v2 goes a step further and is more resilient to various configurations. For example, you can now use an uninitialized repository or specify a branch other than master. While all synchronization options are planned for this module, this beta is limited to the push operations only. You can still choose Sync (default) or Pull when configuring the module, but any changes made outside Wiki.js will not be picked up. Additionally, existing pages will not be pushed until you save them again from the editor. Full functionality is expected for the next beta!

### HTTPS Support
Due to popular request, Wiki.js can now listen on the HTTPS port with your own SSL certificates, eliminating the need for a reverse proxy for most scenarios. Look at the [sample config.yml](https://github.com/Requarks/wiki/blob/2.0.0-beta.42/config.sample.yml#L53-L67) for all possible options. Note that if you're using Docker, you'll need to mount your own config.yml file as the HTTPS options are not yet available as environment variables.

### Many bug fixes...
- Fixed root admin refresh token fail
- Fixed error page metadata title warning
- Fixed telemetry
- Await page render job to complete before resolving
- Added rate limiting to login mutations
- Moved Insert Media button in Markdown editor
- Use semver for DB migrations ordering
- Dev locale .yml files in `server/locales` are now loaded

## Links

- [Installation](https://docs-beta.requarks.io/install)
- [Upgrade from previous Beta (Build 11)](https://docs-beta.requarks.io/install/upgrade)

Consider supporting this project by [becoming a Patron](https://www.patreon.com/requarks) or donating to our [Open Collective](https://opencollective.com/wikijs).

Let us know what you think of this release!
