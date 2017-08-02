---
title: Overview
level1: Documents
level2: Data
level3: Engagement History API

level-order: 6
order: 1
permalink: data-engagement-history-overview.html
root-link: true
indicator: chat
---
### Introduction

Brands can now search, filter and keep copies of chat transcripts and related data, for example surveys, to later integrate and further analyze their data with third-party tools (DWH, CRM systems, etc.). 99.5 % of chat transcript data is available within 5 minutes. All other chat transcript data (including metadata like Engagement Attributes) is available for up to 2 hours after a chat has ended, and is stored for 13 months. The Engagement History API is based on the REST architecture style.

### Getting Started

A few things you'll need to get started with this API:

1. **Retrieve your domain**. Use the [LivePerson Domain API](agent-domain-domain-api.html){:target="_blank"} to retrieve this information by providing the following service name:

	* engHistDomain

2. This API requires authorization using API key.

	* [Follow these instructions](guides-gettingstarted.html){:target="_blank"}, to create and use an API key.

3. [Here are the API terms of use](https://www.liveperson.com/policies/apitou){:target="_blank"}.



### Use Cases

* Extract all chat transcripts and accompanying data in order to integrate with any 3rd party application or database

* Extract a type of conversation (e.g. low CSAT score) and take an action on them.

View of Engagement History within LiveEngage:

![EngagementHistory](img/engagementhistory1.png)

Example of dashboard created using the API:

![EngagementHistory](img/engagementhistory2.png)
