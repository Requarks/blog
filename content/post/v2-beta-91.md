---
categories:
- Updates
date: "2019-04-07"
description: What's new in Wiki.js v2 BETA Build 91...
image: images/unsplash-triangles.jpg
slug: v2-beta-91
tags:
- updates
title: Wiki.js v2 BETA (Build 91)
---

A new build of Wiki.js v2 BETA is now available: Build 91.

## What's New
### Git storage module is now feature complete

The git module now supports import and export of existing content. If you created content in Wiki.js before enabling the git module, you can now run the **Add Untracked Changes** button to add all content to source control tracking. You can also do the same for the opposite direction; if you have content in your remote repository that isn't yet in the DB, run the **Import Everything** task to import missing content.

One of the most requested feature was the ability to force a manual sync. This is now possible using the **Force Sync** action. Note that you can also specify the interval at which synchronization occurs.

### Local Disk storage module is now feature complete

The Daily Backup option is now working. It creates an gzipped archive of all content currently on disk, every 24h, in a subfolder named `_daily`. Archives are kept for a full month before being overwritten.

You can also manually trigger a backup with the content currently on disk using the **Create Backup** action. The archive will be created in the `_manual` subfolder.

Just like the git module, if you created content before the storage module was activated, you will have missing content on disk. Use the **Dump all content to disk** action to output all content from the DB to disk.

### Bug fixes / Minor improvements
- Removed external dependencies on Google Fonts
- Dockerfile improvements to run as node user + apk install fix
- The Pages admin section is now listing all pages. (wip)
- The Insert Image overlay UI can now be displayed, but not functional yet. (wip)

## Links

- [Installation](https://docs-beta.requarks.io/install)
- [Upgrade from previous Beta (Build 84)](https://docs-beta.requarks.io/install/upgrade)

Consider supporting this project by [becoming a Patron](https://www.patreon.com/requarks) or donating to our [Open Collective](https://opencollective.com/wikijs).

Let us know what you think of this release!
