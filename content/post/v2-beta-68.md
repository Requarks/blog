---
categories:
- Updates
date: "2019-03-17"
description: What's new in Wiki.js v2 BETA Build 68...
image: images/unsplash-valleyfog.jpg
slug: v2-beta-68
tags:
- updates
title: Wiki.js v2 BETA (Build 68)
---

A new build of Wiki.js v2 BETA is now available: Build 68.

## What's New
### Search
Search is now available in this build! Start typing in the search bar to quickly find your pages. This release includes 4 engines:

- Azure Search
- AWS CloudSearch
- DB - Basic
- DB - PostgreSQL

Check out the [docs](https://docs-beta.requarks.io/search) for the setup instructions.

![](/images/wikijs-searchresults.png)

### SQLite Support
SQLite is now supported and will no longer throw an error during setup. This brings to 5 the number of supported database engines!

### Git Change Processing
Any changes made in the remote git repository will now be picked up and reflected in the wiki. Note that any pages created before enabling Git will not be pushed to the remote repository. This will be addressed in an upcoming release. In the meantime, simply saving the page again fixes this issue.

### HTTP to HTTPS Redirect
You can now listen on HTTP and redirect all requests to HTTPS as an option. See the SSL section in the `config.sample.yml` file.

### Bug fixes / Minor improvements
- Fixed HTTPS server crash
- Show last sync date in Storage status panel
- Dedicated Dev Flags page in Admin area

## Links

- [Installation](https://docs-beta.requarks.io/install)
- [Upgrade from previous Beta (Build 42)](https://docs-beta.requarks.io/install/upgrade)

Consider supporting this project by [becoming a Patron](https://www.patreon.com/requarks) or donating to our [Open Collective](https://opencollective.com/wikijs).

Let us know what you think of this release!
