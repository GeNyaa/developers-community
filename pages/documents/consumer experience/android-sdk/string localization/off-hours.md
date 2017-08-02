---
title: Date and Time
Keywords:
level1: Documents
level2: Consumer Experience
level3: In-App Messaging SDK for Android
level4: String Localization

order: 274
permalink: android-off-hours.html

indicator: messaging
---

Today and tomorrow off hours message use default SHORT time without date according to the locale (default or custom) and to device setting.

- If device is set to 12 hours format :
  "Thanks for your message. We will be back online today/tomorrow at 3:30pm"
- If device is set to 24 hours format :
  "Thanks for your message. We will be back online today/tomorrow at 15:30"

In case you want special hour format, you can use 
```<string name="lp_time_format"></string>```

With any **time** format. For ex. - "hh:mm a", "HH:mm" etc..

**Date off hours message** (not today/tomorrow) use default LONG date and SHORT time according to the locale (default or custom) and to device setting.

- If device is set to 12 hours format :
  "Thanks for your message. We will be back online January 12, 2017 at 3:30pm"
- If device is set to 24 hours format :
  "Thanks for your message. We will be back online January 12, 2017 at 15:30"

In case you want special date/hour format, you can use 
```<string name="lp_date_time_format"></string>```

With any **date & time format**. For ex. - "MMM d, yyyy hh:mm a", "EEEE dd/mm/yy HH:mm" etc..

###  Timezone 

Off hours can appear in different time zone with this resource ID:
```<string name="lp_ttr_message_off_hours_time_zone_id"></string>```

You can find a list of timezone IDs [here](https://garygregory.wordpress.com/2013/06/18/what-are-the-java-timezone-ids/){:target="_blank"}.

*Example: "US/Pacific", "Europe/Berlin".*
