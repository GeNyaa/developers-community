---
title: Accept a Chat
Keywords:
level1: Documents
level2: Agent Interactions
level3: Chat Agent API
level4: Methods

order: 80
permalink: agent-accept-chat.html

indicator: chat
---

This method accepts the next chat request.

*Note: You should verify the results to see if there are any chat requests before accessing the resource.* 

### Request

| Method|  URL| 
 |:---|  :--- |
 |POST|  https://{domain}/api/account/{accountId}/agentSession/agentSessionId/incomingRequests?v=1&NC=true |

**Request Headers**

 |Header| Description |
 |:---  |:--- |
| Authorization Bearer| {bearer-from-login}| 
 |Content-Type  |application/json |
 |Accept|  application/json |

**Formats**

The body media type must have one of the following formats:

- XML
- JSON

**Body**

No body parameters should be posted.

### Response

If a chat request exists, the request will return an existing chat session.

**Elements in the response**

 |Name|  Description|  Type/Value|  Notes| 
 |:----  |:-----  |:----  |:--- |
 |chatId|  The ID of the agent chat|  string|  Found in the @href element|

**Response Codes**

| Code|  Response| 
 |:---  |:--- |
 |201|  Created| 

Response example for JSON:

    {
     "chatLocation": {
       "link": {
         "@href": "https://{domain}/api/account/{accountId}/agentSession/{agentSessionId}/chat/{chatId}",
         "@rel": "location"
       }
     }
    }