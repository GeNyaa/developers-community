---
title: logOut
Keywords:

level2: Consumer Experience
level3: In-App Messaging SDK for Android
level4: Methods

order: 260
permalink: android-logout.html

indicator: messaging
---

Logout from the SDK - when all user data should be removed.

Calls [unregisterLPPusher](android-unregisterlppusher.html){:target="_blank"}, [shutDown](android-shutdown.html){:target="_blank"} and, in addition, deletes all user data (messages and user details) from the device.

In order to unregister from push, it must be called when there is network available. After logout the SDK is unavailable until re-initiated.

**This method does not require the SDK to be initialized.**

*Note: This does not end the current messaging conversation.*

**Important: This method must not be called when the conversation screen is displayed.**

`public static void logOut(Context context, String brandId, String appId, LogoutLivePersonCallback logoutCallback){`

| Parameter | Description |
| :--- | :--- |
| context | A context from the host app. |
| brandId | An account ID. |
| appId | The host app ID. |
| logoutCallback | An [LogoutLivePersonCallback](android-callbacks-index.html){:target="_blank"} implementation. |





### LogoutLivePersonCallback

```javascript
{
public interface LogoutLivePersonCallback{
    void onLogoutSucceed();
    void onLogoutFailed();
}
```
