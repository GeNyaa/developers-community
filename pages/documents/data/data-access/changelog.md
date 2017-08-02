---
title: Changelog
level1: Documents
level2: Data
level3: Data Access API (BETA)

order: 62
permalink: data-data-access-changelog.html

---
This document describes changes made to the Data Access API. Entries will appear under a relevant date and will detail changes made to either the documentation or the API itself. All changes should be backwards compatible but where they are not or extra work is needed to make sure that backwards compatibility is maintained, the Changelog will mention this.

All future dates found in this documentation reflect approximations for upcoming additions or corrections and are subject to change.

### June 18th, 2017

**Bug Fixes**

Fixed a bug where some of the conversation records created by the Data Access job had missing conversation IDs.

**Data Access Schema (version 1.0.0.34)**  

The `isInteractive` boolean field was added to the transfer section. This field indicates whether the transfer part of the conversation is interactive or not. _To clarify_, the `isInteractive` field in the main conversation section relates to the last part of the conversation.

### Visualping Test

I'm trying to test VisualPing's notifications. Hopefully, I'll be notified of this addition. Let's see if it works.
