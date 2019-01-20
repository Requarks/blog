---
categories:
- Updates
date: "2019-01-20"
description: The very first beta of Wiki.js v2.0 is finally here...
image: images/unsplash-colortiles.jpg
slug: v2-beta
tags:
- updates
title: Wiki.js v2.0 Beta
---

The very first beta of Wiki.js v2.0 is finally here!

## But first...

THIS IS A **BETA** RELEASE. It is not production-ready and is missing many critical features! It might crash and you might loose data. This is stricly for testing and development purposes.

That being said, you'll be able to easily upgrade between beta releases, up to the final release.

**Note that it is not yet possible to import content from v1.x.** This feature will be available in the final release.

## tl;dr

Instructions to install the beta can be found on the [beta wiki](https://docs-beta.requarks.io/), which obviously runs the new beta!

## What's New in 2.0?

This new version is a complete rewrite from the ground up. It's fully modular, more powerful and customizable than ever.

One of the biggest lesson learned from v1 was how users want to customize their wiki to make it their own. Not only from a visual perspective, but from the technical side as well. The git requirement was cumbersome for many users. Some found the Markdown editor confusing. The search engine didn't work in non-latin languages. The permission system was severily limited.

This all changes with 2.0.

### Groups

Groups are a new addition to Wiki.js. Permissions are no longer tied to users. Instead, users are linked to one or more groups. Groups have global permissions and page rules.

Global permissions lets you define whether a group can read pages, post a comment, upload assets, etc. They are applied at the global level.

Page Rules are the second level of permissions. They apply specific permissions to a specific page or section. For example, you might not want to give read access to the whole site but only on the homepage and any pages under `/foo-bar`. This is possible using Page Rules.

### Modules

Wiki.js v2.0 is fully modular. You have total control on which feature you want for your wiki. Your wiki can use Google authentication, a WikiText editor and have its content stored in AWS S3. Modules are splitted into 6 categories:

#### Authentication

The first version of Wiki.js had pretty good support for a vast array of authentication providers. In 2.0, we added even more:

- Auth0
- Azure AD
- CAS
- Discord
- Dropbox
- Facebook
- GitHub
- Google
- LDAP
- Local (default)
- Microsoft
- Generic OAuth2
- Generic OpenID Connect
- Okta
- SAML 2.0
- Slack
- Twitch

One of the most requested feature for v1 was for users to be able to create their own account. This is now possible! You can also restrict by email domains and automatically enroll new users into a specific group.

Two-Factor Authentication (2FA) is also coming soon.

#### Editors

You are no longer limited to Markdown. You can now choose between a selection of 6 editors when creating a new page:

- **API Docs**: For REST / GraphQL documentation
- **Code**: Raw HTML
- **Markdown**: Default Markdown editor
- **Tabular**: For Grid/Excel-like pages
- **Visual Builder**: WYSIWYG-style editor, with drag-n-drop functionnality.
- **WikiText**: For writing MediaWiki-style content

The default Markdown editor now comes with a live preview panel.

*Only the Code and Markdown editors are available for now. The rest will come later on.*

#### Logging

This one is more for administrators and developers. Logs are no longer limited to the console or some hard to access log files. You can now forward logs to an external service. The following targets will be supported:

- Airbrake
- Bugsnag
- Local Disk
- Event Log *(Windows)*
- Loggly
- Logstash
- NewRelic
- Papertrail
- Raygun
- Rollbar
- Sentry
- Syslog *(Linux)*

You'll also be able to live stream the logs from the administration area in your browser.

#### Rendering

The complete rendering pipeline is now fully exposed and customizable. You can now choose how content is rendered. A detailed article covering content rendering will be published at a later date.

#### Search Engines

The search capabilities were greatly improved in v2. Search will now work with non-latin languages and be much more efficient. The following engines will be supported:

- Algolia
- AWS CloudSearch
- Azure Search
- Internal DB (default)
- Elasticsearch
- Manticore
- Solr
- Sphinx

#### Storage

You are no longer required to use git for storing content. All content is now stored directly in the database. You can still continue to have your pages synced with a git repository should you want to or use one of the many new storage targets:

- Azure Blob Storage
- Box
- DigitalOcean Spaces
- Local Disk / Network Share
- Dropbox
- Google Drive
- Git
- OneDrive
- S3 (AWS)
- SCP (SSH)

You can also choose the sync direction (push, pull or sync) for most targets.

### Locales

There're some great new features when it comes to localization. Translation strings are now kept up-to-date every day, which means you'll always get the latest additions / corrections as they are added by translators. New locales can now be downloaded from the administration area as needed. They are no longer bundled with the app itself.

Another most requested feature was the ability to have multilingual content. This is now possible in 2.0. You can now have content in multiple languages, with the use of locale prefixes. For example, `/en/foo-bar` and `/fr/foo-bar` will now display their content and UI in English and French respectively.

### Navigation

The table of contents has been moved to the right of the page. The left sidebar is now a global navigation, which is fully customizable from the administration area.

All pages (with the exception of the homepage) have a breadcrumb navigation as well. It's now easier than ever to go up a level and quickly understand the page hierarchy.

### Tags

Tags are a new addition to Wiki.js. You can now categorize your pages and quickly find pages with the same or related tags!

### Themes

While you could change the colors of the UI in v1, it was fairly limited. In v2, we introduce themes. You can have total control on how the page is displayed. You can make your wiki look completely different from the default visual if you choose to.

#### Dark Mode

An optional, system-wide Dark Mode. Enough said!

### History

All content changes are now tracked and be viewed / restored from the new history page.

### GraphQL API

The frontend has been completely decoupled, thanks to a new GraphQL API. It's now easier than ever to build custom integrations with your other tools. A detailed article on this API will be published at a later date.

### Mobile / Tablet compatibility

Your wiki pages will now look nice on all devices, no matter their screen size! (*Although the administration area requires a normal screen for now!*)

## And so much more...

There are many features that are not listed there, most of which are simply not developed yet. They will be detailed as they are ready. A few examples include:

- Personal wiki
- Comments
- Ratings
- Profile

*Being developed...*
