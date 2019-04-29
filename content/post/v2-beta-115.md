---
categories:
- Updates
date: "2019-04-28"
description: What's new in Wiki.js v2 BETA Build 115...
image: images/unsplash-seamountains.jpg
slug: v2-beta-115
tags:
- updates
title: Wiki.js v2 BETA (Build 115)
---

A new build of Wiki.js v2 BETA is now available: Build 115.

## What's New
### Social + Enterprise Authentication

This build comes bundled with 11 social / enterprise authentication modules in addition to local authentication. This is already more than v1 and we're just getting started. The new modules are:

- Auth0
- Discord
- Dropbox
- Facebook
- GitHub
- Google
- LDAP / ActiveDirectory
- Okta
- SAML 2.0
- Slack
- Twitch

More modules (such as Azure AD, CAS, Firebase, Microsoft and generic OAuth2 / OpenID) will come in future betas.

The admin UI for managing auth modules has also been revamped to be easier to use, without having to go back and forth between tabs.

### Bug fixes / Minor improvements
- Handle Git basic auth URI format with or without protocol
- Timeout indicator animation for alerts
- Auth token now refreshes correctly when the short refresh expires
- Attempting to create a page from reserved paths is now blocked
- General UI improvements

## Links

- [Installation](https://docs-beta.requarks.io/install)
- [Upgrade from previous Beta (Build 91)](https://docs-beta.requarks.io/install/upgrade)

Consider supporting this project by [becoming a Patron](https://www.patreon.com/requarks) or donating to our [Open Collective](https://opencollective.com/wikijs).

Let us know what you think of this release!
