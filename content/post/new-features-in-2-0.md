---
categories:
- Updates
date: "2018-06-02"
description: This page will be updated regularly with new content until 2.0 is released. Check back often!
image: images/unsplash-spikes.jpg
slug: new-features-in-2-0
tags:
- updates
title: New Features in 2.0
---

This page will be updated regularly with new content until 2.0 is released. Check back often!

## Editor
### Side-by-side Live Preview
This was one of the most requested feature. The editor now features a live, side-by-side preview pane (which can be turned off).

### Modular editors
While 2.0 comes with a single editor (at least for now, WYSIWYG coming in a later release!), it is possible for developers to build their own editor. Users may switch editors should they prefer one over the other.

More technical users can now use a code-based editor while the average joe may prefer a visual editor.

## Groups & Permissions
*todo*

## Authentication
### Modular + extensible
Wiki.js comes with a long list of authentication providers built-in and some new ones have been added:
 - Auth0
 - Azure Active Directory
 - Discord
 - Dropbox
 - Facebook
 - Generic OAuth2
 - GitHub
 - Google ID
 - LDAP / Active Directory
 - Local (database)
 - Microsoft Account
 - Slack
 - Twitch

It's very simple to add providers thanks to the new modular system.

### Two-Factor Authentication (2FA)
*todo*
### Self-registration
*todo*
### Domain restrictions
*todo*

## Storage
In 1.x, Git was a requirement and the only option to store and backup your content. This is no longer the case in 2.0. Git is now **optional** and you can use virtually any storage target available.

In addition to git, you'll be able to sync your content to cloud services, network storage and more:
- Amazon S3
- Azure Blob Storage
- DigitalOcean Spaces
- Dropbox
- Git
- Google Drive
- Local disk / Network shares
- OneDrive
- SCP (SSH)

Just like authentication, storage is built on a **modular** model, which means you can develop your own storage module for new solutions (and hopefully share that module with the community!).

## Search
Much like the majority of the 2.0 codebase, search was rewritten from scratch to address the many issues users were facing in 1.x.

### Non-latin languages support
Cyrillic, arabic, syllabaries/logographies and other non-latin languages are now supported in search results.

### Permission-based results
Pages the user don't have access to will no longer be listed in the search results.

### Faster + more robust
*todo*

### Modular + external options
In addition to the built-in search engine (which relies on the database engine), you can now use external engines such as **Algolia**, **Azure Search**, **Elasticsearch** and **Solr**.