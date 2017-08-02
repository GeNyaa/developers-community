---
title: Change User's Password
keywords:
level1: Documents
level2: Admin
level3: Users API
level4: Methods


order: 80
permalink: administration-change-users-password.html

indicator: both
---

This API changes a user’s password.

### Request

| Method|      URL  |
 |:--------|  :---  |
 |PUT | /api/account/{accountId}/configuration/le-users/users/{userId}/changePassword |

**Request Headers**

 |Header|         Description  |
 |:------ |       :--------  |
 |Authorization  |Contains token string to allow request authentication and authorization.  |

**Request Body**
 
       {
            "newPassword": "newPassword",
            "confirmPassword": "newPassword",
            "oldPassword": "oldPassword"
        }

**Path Parameters**

 |Parameter|  Description|  Type/Value| 
 |:------    |:--------    |:--------|
 |accountId|  LP site ID|   String ^[a-zA-Z0-9_]{1,20}$|
 |userId|  User ID|   Positive long number greater than zero|

### Response

**Response Body**

[Appendix](administration-users-appendix.html){:target="_blank"} for Entity Structure and Entity Example.


