---
categories:
- Updates
date: "2018-07-31"
description: This post will be updated as new areas become available for development.
image: images/unsplash-laptop.jpg
slug: developers-wiki
tags:
- updates
title: "Developers: contributing to Wiki.js 2.0"
---

*This post will be updated as new areas become available for development.*

# Getting Started
Read the [Getting Started](https://docs.requarks.io/wiki/v/2.x/developers/getting-started) guide for Wiki.js 2.0 to get all the necessary prerequisites and get the solution running on your dev machine.

You should also familiarize yourself with the new modular concept of Wiki.js 2.0 and how they work by reading the [introduction](https://docs.requarks.io/wiki/v/2.x/developers/modules/introduction) to modules.

# Coordination
If you want to work on a task, you need to let me know on [Gitter](https://gitter.im/Requarks/wiki) so that I can assign the GitHub Issue to you. This will prevent two people wasting time working on the same thing.

# Areas

### Storage Modules

When a page is created, updated, deleted or renamed, one or more storage providers can be configured to act as backup / sync. At the moment, only the local filesystem provider module is functional. However, the idea is to have as many options as possible for users to backup their data, whether its to cloud providers such as AWS, Azure, etc. or to classic solutions like Git or SSH.

Read the [Storage Modules](https://docs.requarks.io/wiki/v/2.x/developers/modules/storage) documentation.

For the moment, only the `created` and `updated` events are being called (when creating a page and saving further modifications). This post will be updated as other events are implemented.

These are the current proposed modules:

- [AWS S3](https://waffle.io/Requarks/wiki/cards/5b40287459838e001b680c86)
- [Azure Blob Storage](https://waffle.io/Requarks/wiki/cards/5b4028ce3b94fe001da4590d)
- [Box](https://waffle.io/Requarks/wiki/cards/5b612df96b3ad1001c6fb80d)
- [DigitalOcean Spaces](https://waffle.io/Requarks/wiki/cards/5b40279729ec9e001bad3ea5)
- [Git](https://waffle.io/Requarks/wiki/cards/5b4026a38f70ca001c509106)
- [SSH (SCP)](https://waffle.io/Requarks/wiki/cards/5b402a17dc70ba001d39cbae)

The following modules would also be great, however they will most likely require some sort of oauth flow where the user must create an app and then browse to it by providing Wiki.js authorization. If someone can figure out a way to use these in a non-interactive way, it would be best!

- [Dropbox](https://waffle.io/Requarks/wiki/cards/5b40294a2757ed001defabff)
- [Google Drive](https://waffle.io/Requarks/wiki/cards/5b40296e2e8c9c001c2cd07f)
- [Microsoft OneDrive](https://waffle.io/Requarks/wiki/cards/5b402986e5f8ca001d1a1368)

If you have a storage provider not listed here that you'd like to work on, let me know on [Gitter](https://gitter.im/Requarks/wiki).

### Authentication Modules

*Coming soon*