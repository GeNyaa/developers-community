---
title: Modifying Resources
Keywords:
level1: Documents
level2: Consumer Experience
level3: In-App Messaging SDK for Android
level4: Customization and Branding

order: 265
permalink: android-modifying-resources.html

indicator: messaging
---

The SDK utilizes several resources as part of its GUI. To customize those resources, please add appropriate resources to your project:

<table>
  <tr>
    <th>Description</th>
    <th>Resources name</th>
  </tr>
  <tr>
    <td>Default brand avatar on the avatar next to brand bubble (the first brand message) and on agent avatar appearing on the action bar before an agent is assigned. In case you want to define the background color for this avatar - override "brand_logo_background_color" resource id. (This is relevant for bubble brand’s avatar only. Background color of agent avatar on action bar is "agent_avatar_background_color").</td>
    <td>lp_messaging_ui_brand_logo </td>
  </tr>
  <tr>
    <td>Default agent avatar appearing next to an agent’s bubble when no avatar URL is assigned on LiveEngage and on agent avatar appearing on the action bar.  In case you want to define the background color for this avatar, override "agent_avatar_background_color" resource id. </td>
    <td>lp_messaging_ui_ic_agent_avatar</td>
  </tr>
</table>
