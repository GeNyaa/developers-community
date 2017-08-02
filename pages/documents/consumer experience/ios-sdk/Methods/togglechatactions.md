---
title: toggleChatActions
Keywords:

level2: Consumer Experience
level3: In-App Messaging SDK for iOS
level4: Methods

order: 50
permalink: consumer-experience-ios-sdk-togglechatactions.html

indicator: messaging
---

This API call is used to open or close the SDK menu. 

* If you’re using [window mode](consumer-experience-ios-sdk-showconversation.html){:target="_blank"}, you won’t need to utilize this method as the SDK will have a dedicated button in the navigation bar to toggle the menu. 
* If you are using [view controller mode](consumer-experience-ios-sdk-showconversation.html){:target="_blank"}, you may call this API to open the SDK menu, or use other APIs to build your own menu. 

`func toggleChatActions(_ accountID: String, sender: UIBarButtonItem? = nil)`

| Parameter | Description | Notes |
| :--- | :--- | :--- |
| accountID | An account ID |
| sender | An optional UIBarButtonItem to use for toggling the chat actions |