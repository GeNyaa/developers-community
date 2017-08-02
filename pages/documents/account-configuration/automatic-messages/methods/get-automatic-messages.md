---
title: Get Automatic Messages
keywords:
level1: Documents
level2: Account Configuration
level3: Automatic Messages API
level4: Methods

order: 10
permalink: account-configuration-automatic-messages-get-automatic-messages.html

indicator: both
---

Retrieves a list of Automatic Messages for a specific account.

### Request

| Method | URL |
| :-------- | :------ |
| GET | api/account/{accountId}/configuration/engagement-window/auto-messages |

### Response

**Response Codes**

| Code | Description |
| :----- | :------------ |
| 304 | Not Modified |
| 401 | Not Authenticated |
| 403 | Not Authorized |
| 500 | Internal Server Error |

**Response Body**

    {
        {
            "id": 1,
            "deleted": false,
            "enabled": true,
            "messageEventId": "CHAT_STARTED",
            "templateId": "CHAT_STARTED",
            "data": [
                {
                    "msg": "You are chatting with {agent name}",
                    "lang": "en-us",
                     "isDefault":true
                },
                {
                    "msg": "Que está conversando {nombre del agente}",
                    "lang": "ca-ES",
                    "isDefault":true 
                }
            ]
        },
        {
            "id": 2,
            "deleted": false,
            "enabled": true,
            "messageEventId": "On-hold message #1",
           "templateId": "On-hold message #1",
            "data": [
                {
                    "msg": "I'll be right with you.",
                    "lang": "en-us",
                    "isDefault":true 
                },
                {
                    "msg": "Que está conversando {nombre del agente}",
                    "lang": "ca-ES",
                    "isDefault":false 
                }
            ],
            "attributes": [
                {
                    "name": "timer",
                    "value": "60"
                }
            ]
        }
    {
