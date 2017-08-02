---
title: Release Notes
Keywords:
level1: Documents
level2: Consumer Experience
level3: In-App Messaging SDK for iOS

order: 243
permalink: consumer-experience-ios-sdk-release-notes.html
indicator: messaging
---
### In-App Messaging SDK Version 2.5.0

These are the main feature releases available in the In-App Messaging SDK version 2.5 for iOS.

Version 2.5 roll-out: July 2nd 2017

### New functionalities

### Custom fonts

in order for consumers to enjoy the full brand experience while messaging in-app, brands are able to configure certified operating system fonts to appear in the messaging window. The fonts can be used across all elements, or only for the font within the message bubble.

The SDK also supports the use of a brand’s own customized fonts (although these are not certified).

Custom fonts are not supported for Native iOS properties such as:
* Activity mode - Overflow menu
* Popup messages

###### Related properties: Custom fonts

The following additional conditions and configurations are required:*



| Backend update  | Backend enablement  | Backend configuration  | SDK enablement  | SDK configuration  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| N/A | N/A | N/A | N/A | Yes |

### Tablet supportability
To ensure that consumers using tablets can connect with brands while enjoying the tablet experience, in-app messaging is now supported on these devices, in window mode and activity mode, and in both portrait and landscape layouts.

All supported devices have gone through automation tests and all certified devices have gone through both automation and manual testing.

| Device | iOS 8.x | iOS 9.x | iOS 10.x |
| ------------ | ------------ | ------------ | ------------ |
| iPad 5 (2017) | N/A  | N/A | Certified |

A full list of supported and certified devices can be found in the LiveEngage System Requirements document.

### Connectivity improvements
The user experience when connecting to the app has been significantly improved. When users first log-in, and during all subsequent attempts, the login process is now much smoother and faster.

In addition, other aspects such as feature and conversation history will also be more rapid as a result of the improvements.

The following additional conditions and configurations are required*:

| Backend update  | Backend enablement  | Backend configuration  | SDK enablement  | SDK configuration  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| N/A | N/A | N/A | N/A | N/A |

### Default Agent Avatar
The SDK now offers brands a to use a default agent avatar of their own.

Related properties: User avatar

The following additional conditions and configurations are required*:

| Backend update  | Backend enablement  | Backend configuration  | SDK enablement  | SDK configuration  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| N/A | N/A | N/A | N/A | Yes |

* Key for items as follows:
Backend update: This feature requires an update to the backend.
Backend enablement: This feature requires items to be toggled on in the backend.
Backend configuration: This feature requires configuration in the backend.
SDK enablement: This feature requires items to be toggled on in the SDK.
SDK configuration: This features requires items to be configured in the SDK.

### Photo Sharing Button Colors
Brands now have the ability to set camera button colors in addition to the Send button colors.

Related properties: Photo sharing

The following additional conditions and configurations are required*:

| Backend update  | Backend enablement  | Backend configuration  | SDK enablement  | SDK configuration  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| N/A | N/A | N/A | N/A | Yes |

## New properties
The following properties of the secure form bubble on the agent side can now be configured:

#### Custom Fonts

| Name | Description  | Example | Default |
| ------------ | ------------ | ------------ | ------------ |
| customFontNameConversationFeed: String? = nil | The font name for all elements of the conversation feed. | ![CustomFonts](https://raw.githubusercontent.com/LP-Messaging/iOS-Messaging-SDK/gh-pages/images/customFontConversationFeed.png) | Empty (use the device font) |
| customFontNameNonConversationFeed: String? = nil | The font name for all elements that are not in the conversation feed. | ![CustomFonts](https://raw.githubusercontent.com/LP-Messaging/iOS-Messaging-SDK/gh-pages/images/customFontNonConvrsationFeed.png) | Empty (use the device font) |

#### Photo Sharing
Configuring Camera's button colors

| Name | Description | Example | Default |
| ------------ | ------------ | ------------ | ------------ |
| cameraButtonEnabledColor | The camera button color when in enabled mode in the conversation screen. The button will be presented only if the photo sharing feature is enabled. | ![CameraColor](https://raw.githubusercontent.com/LP-Messaging/iOS-Messaging-SDK/gh-pages/images/cameraButtonEnabledColor.png) | #0362AC |
| cameraButtonDisabledColor | The camera button color when in disabled mode in the conversation screen. The button will be presented only if the photo sharing feature is enabled. | ![CameraColor](https://raw.githubusercontent.com/LP-Messaging/iOS-Messaging-SDK/gh-pages/images/cameraButtonEnabledColor.png) | #8B8A8F |

#### User Avatar
Configuring Camera's button colors

| Name  | Description  | Default  |
| ------------ | ------------ | ------------ |
| remoteUserDefaultAvatarImage | The default avatar image of the remote user. When assigned, this image will disable remoteUserAvatarBackgroundColor and remoteUserAvatarIconColor configurations. If the remote user has an avatar image in his profile, this attribute will be ignored. | nil |


### In-App Messaging SDK Version 2.3.1

In-App Messaging SDK v2.3.1 for iOS contains the following bug fix:

**Symptom**:

For one minute after the consumer had navigated away from the conversation window, any arriving messages would not display. They would only appear in the conversation window after the minute had passed.

### Fix:
The following capability which was first introduced in v2.3 has been disabled to avoid this bug : “Presence enablement for photo sharing - beta*”.

### In-App Messaging SDK Version 2.3.0

These are the main feature releases available in the **In-App Messaging SDK version 2.3 for iOS**.


#### iOS Developer Enhancements

The LiveEngage in-app SDK is fully compatible with the most recent versions of Apple’s developer tools, XCode 8.3 and Swift 3.1.

The SDK is also compatible with [CocoaPods](https://cocoapods.org/){:target="_blank"}, a dependency manager for Swift and Objective-C Cocoa projects. CocoaPods has thousands of libraries and is used in over 2 million apps. It can help you scale your projects elegantly and provides a standard format for managing external libraries.

Note: Sample Apps are now using CocoaPods.

**CocoaPods Installation**

1.	Install cocoapods using the following command:

    $ gem install cocoapods

2.	Navigate to your project folder and init new pod using the following command:

    $ pod init

3.	Podfile should be created under your project’s folder.

    To integrate Liveperson Messaging SDK into your Xcode project using CocoaPods, specify it in your Podfile:

      source 'https://github.com/LivePersonInc/iOSPodSpecs.git'
        platform :ios, '8.0'
      	use_frameworks!

      	target '<Your Target Name>' do
      	    pod 'LPMessagingSDK'
      	end

4.	Run the following command in the terminal under your project folder:

    $ pod install

5.	In project settings, navigate to the Build Phases tab, and click the + button to add a New Run Script Phase. Add the script below in order to loop through the frameworks embedded in the application and remove unused architectures (used for the simulator). This step is a workaround for the [known iOS issue](http://www.openradar.me/radar?id=6409498411401216){:target="_blank"} and is necessary for archiving your app before publishing it to the App Store.

```shell
bash "${SRCROOT}/Pods/LPMessagingSDK/LPMessagingSDK/LPInfra.framework/frameworks-strip.sh"
```


#### Secure form for in-app messaging


The secure form gives consumers the confidence to submit sensitive information, such as credit card data and social security numbers, while messaging in-app. The form also enables agents to safely carry out secure processes, such as payment, identification and authorisations.

The form can be tailored to match the in-app messaging experience and has a time-out expiry, for added security.

_This feature requires consulting services support. For more information, please refer to the LiveEngage [secure form for messaging documentation](https://s3-eu-west-1.amazonaws.com/ce-sr/CA/security/Secure+form+for+messaging.pdf){:target="_blank"}_.

![Release Notes Secure Form](img/releasenotessecureform.png)

**Related properties**: Agent PCI bubble
**Related strings**: PCI


#### List of certified and supported devices extended

The following devices are now also supported and/or certified to host our in-app messaging SDK:

**iPhone**

|                 |    Operating system    |                 |
|-----------------|------------------------|-----------------|
|    Device       |    iOS 9.x             |    iOS 10.x     |
|    iPhone SE    |    Supported           |    Supported    |

**iPad**

|                       |    Operating system    |                 |                 |
|-----------------------|------------------------|-----------------|-----------------|
|    Device             |    iOS 8.x             |    iOS 9.x      |    iOS 10.x     |
|    Air 2 (2014)       |    Supported           |    Supported    |    Supported    |
|    Mini 4 (2015)      |    N/A                 |    Supported    |    Supported    |
|    iPad Pro (2016)    |    N/A                 |    Supported    |    Supported    |
|    iPad 5 (2017)      |    N/A                 |    N/A          |    Supported    |



### Presence enablement for photo sharing - beta*
Presence enablement for photo sharing provides consumers with the ability to receive notifications while uploading a photo, whether they remain within the app or keep it running in the background.

The Web Socket remains open for a maximum of 60 seconds (using Background Task) when the app or conversation window moves to the background. This scenario is also applicable for non photo sharing flows.

*Photo sharing is a beta feature.




### In-App Messaging SDK Version 2.0

These are the main feature releases available in the In-App Messaging SDK version 2.0.


#### Photo sharing for iOS and Android (Beta)

Consumers can now add photos directly into a messaging conversation, enabling them to describe an item and share it with their agent. Photo sharing supports multiple image sizes, and all shared images are logged in All Connections. This feature is available for Facebook messenger, web messaging, and in-app messaging, on both Android and iOS.

![Release Notes Photo Sharing](img/releasenotessharing.png)


#### Accessibility for messaging


The In-App Messaging SDK now supports accessibility WCAG Level A and Level AA and CATO.

![Release Note Accessibility](img/releasenotesaccessibility.png)


#### Configure regular expressions to create hyperlinks in messages


Brands can now configure their own regular expressions to create hyperlinks which link directly to relevant pages or actions.

Expressions can be configured for the following commands:

*	Call
*	Email
*	URL

![Release Notes Hyperlinks](img/releasenotes1.png)


#### In-conversation shortcut to new messages


A shortcut can now be configured to appear within the conversation when there are new messages available. This saves the consumer time when scrolling within messaging conversations. Clicking on the shortcut navigates the visitor straight to the new messages so they can quickly and easily continue the conversation.

![Release Note In-conversation](img/releasenotesinconversation.png)


#### Set icon for send button


Brands now have the ability to replace the Send button in a messaging conversation with a paper plane (Android) or arrow (iOS). This icon can be customized to match the brand’s colors.

![Release Notes Set Icon](img/releasenotesseticon.png)


#### Link preview within conversation


When sending a link within an in-app messaging conversation, a preview of the link page will display within the thread, giving the consumer a useful overview of the link content.

![Release Notes Link Preview](img/releasenoteslinkpreview.png)


#### Ability to remove resolved divider in thread


Brands are now able to configure the removal of the resolved divider within a thread. The divider usually appears underneath the system message noting that the conversation has been resolved. This creates the feel of one ongoing, undisrupted conversation for consumers using messaging.

![Release Notes Ability to Remove](img/releasenotesability1.png) ![Release Notes Ability to Remove](img/releasenotesability2.png)


#### Add callback to SDK for agent picture click


In order to provide brands with greater insight into consumer activity within the messaging window, LiveEngage will provide a callback when a consumer clicks on the agent’s picture in the conversation. The brand can then decide what action they would like to take, for example opening an agent profile or enlarging the picture.

![Release Notes Add Callback](img/releasenotescallback.png)


#### Enhancement: Configure CSAT Timeout


Brands can now configure for how long a CSAT form will be displayed to the consumer after the messaging conversation is resolved by the agent. This applies to consumers who exit the conversation before it is resolved.

Brands can select from the following options:
-	The CSAT form never times out, and will be displayed to the consumer when they reopen the conversation regardless of the amount of time that has passed since the conversation was resolved.

-	The number of minutes from when the conversation was resolved to when the form will no longer be displayed.
