---
title: Delete Agent Groups
keywords:
level1: Documents
level2: Admin
level3: Agent Groups API
level4: Methods


order: 70

permalink: administration-delete-agent-groups.html

indicator: both
---

This API deletes agent groups from a specific account.

### Request

| Method | URL |
| :--------- | :---------- |
 |DELETE | /api/account/{accountId}/configuration/le-users/agentGroups |

**Request Headers**

 |Header | Description|
 |:------ | :-------------- |
 |Authorization | Contains token string to allow request authentication and authorization. 
 |If-Match | Contains data revision as known by the client. Allows optimization of the backend, networking, and client resources utilization. 

**Request Body**

`["987654321", "1232455"]`

**Query Parameters**

 |Parameter | Description  |Type / Value|  Required |
 |:----------- | :------------- | :-------------- | :--- |
| v| API version number | Double. Default Value: 1.0 | Required |
| select|  Dynamic selection of the response fields | YOGA 'gdata' dialect. Non-existing field: no error, blank in response. Supported fields: any in response body| Optional |

**Path Parameters**

|Parameter | Description | Type / Value |
 |:----------- | :------------- | :------------- |
| accountId  | LP site ID  String ^[a-zA-Z0-9_]{1,20}$ 

### Response

**Response Headers**

| Header | Description |
| :-------- |:------------- |
 |eTag | Account config object type collection revision. |

**User Entity Structure**

[Appendix](administration-agent-groups-appendix.html){:target="_blank"}{:target="_blank"} for Entity Structure and Entity Example.
