---
categories:
- Updates
date: "2019-03-24"
description: What's new in Wiki.js v2 BETA Build 84...
image: images/unsplash-metalpolygons.jpg
slug: v2-beta-84
tags:
- updates
title: Wiki.js v2 BETA (Build 84)
---

A new build of Wiki.js v2 BETA is now available: Build 84.

## What's New
### Additional Search Engines
This release includes 2 new search engines:

- Algolia
- Elasticsearch

Check out the [docs](https://docs-beta.requarks.io/search) for the setup instructions.

![](/images/wikijs-searchresults.png)

### Bug fixes / Minor improvements
- Fixed error when saving navigation in admin area
- Fixed guest search failing because of missing global permissions
- Fixed PostgreSQL search engine indexing issues
- Improved search suggestions from sanitized content
- Search engine deactivate handler is now being called on engine switch
- Markdown editor UI improvements for insert actions (wip)

## Breaking Changes

If you are using, or have used the PostgreSQL search engine at least once in the past, you must follow the following procedures to recreate the index tables correctly:

1. Make sure the **Database - PostgreSQL** search engine is enabled. Select it and click **Apply** if that's not already the case.
2. Select the **Database - Basic** search engine and click **Apply**. This will trigger the deactivation procedure for the PostgreSQL engine, effectively dropping the index tables.
3. Select the **Database - ProgreSQL** search engine again and click **Apply**. This will recreate the index tables correctly.
4. Finally, click **Rebuild Index** to add all existing content to the index.

## Links

- [Installation](https://docs-beta.requarks.io/install)
- [Upgrade from previous Beta (Build 68)](https://docs-beta.requarks.io/install/upgrade)

Consider supporting this project by [becoming a Patron](https://www.patreon.com/requarks) or donating to our [Open Collective](https://opencollective.com/wikijs).

Let us know what you think of this release!
