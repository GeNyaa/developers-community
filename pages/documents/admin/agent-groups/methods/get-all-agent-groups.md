---
title: Get all Agent Groups
keywords:
level1: Documents
level2: Admin
level3: Agent Groups API
level4: Methods


order: 10
permalink: administration-get-all-agent-groups.html

indicator: both
---

This API retrieves a list of agent groups for a specific account.

### Request 

| Method | URL |
| :------- | :----- |
| GET  |/api/account/{accountId}/configuration/le-users/agentGroups |

**Request Headers**

| Header  | Description  |Required |
| :------- | :--------------- | :--- |
| Authorization | Contains token string to allow request authentication and authorization. | Required 
| If-Match | Contains data revision as known by the client. Allows optimization of the backend, networking, and client resources utilization.|  Optional |

**Path Parameters**

| Parameter | Description | Type / Value |
| :---------- | :------------- | :-------------- |
 |accountId | LP site ID | String ^[a-zA-Z0-9_]{1,20}$ |

### Response

**Response Headers**

| Header | Description|
| :------- | :------------- |
 |eTag | Account config object type collection revision |

**Response Body**

[Appendix](administration-agent-groups-appendix.html){:target="_blank"} for Entity Structure and Entity Example.
