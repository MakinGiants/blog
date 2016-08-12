---
title: How to Use OneSignal for Push Notifications
layout: post
categories: Android, OneSignal, PushNotifications
---

[OneSignal](https://onesignal.com/) offer Push Notification as a service, an Android SDK and a Public API.

Is possible that your flow looks like:

1. Get push notification _token_ from device
2. Send _token_ to your backend
3. Backend uses _token_ and [OneSignal API][0] to send pushes.
4. Device get the push notification

## Ok, Show me code!

We will use the next dependencies:

```groovy
compile 'com.onesignal:OneSignal:3.0.0@aar'
compile "com.google.android.gms:play-services-gcm:9.2.1"
compile "com.google.android.gms:play-services-analytics:9.2.1"
compile "com.google.android.gms:play-services-location:9.2.1"
```

Lets use OneSignal Android SDK method to get push ids: 

```java
OneSignal.idsAvailable((userId, registrationId) -> {
    // Use any of those ids to send the push from backend/server/something
});
```

  1. `userId`: playerId from _OneSignal_
  1. `registrationId`: Google push token

When you check [OneSignal API][0] you will see that you can use any of those to create pushes with `include_android_reg_ids` and `include_player_ids`, 

**But which one should you use?**

![]( {{ site.path-emoji-hmm }} )

## Try 1 - Using registrationId

From your server you should do a `POST` to https://onesignal.com/api/v1/notifications with:

```json
{
  "app_id": "...",
  "contents": { "en": "Custom Content" },
  "headings": { "en": "Custom Heading" },
  "data": { },
  
  "include_android_reg_ids": [ "registrationIdValue"]
}
```

But **you will notice that after some attemps you will get this error**:

```json
{
  "id": "",
  "recipients": 0,
  "errors": { "invalid_android_reg_ids": [ "registrationIdValue" ] }
}
```

Looks like they are having issues since `OneSignal.idsAvailable` always returns the same but it becomes invalid based on _OneSignal API_ responses.

## Try 2 - using userId (Best Solution)

They said by chat:

> We recommend storing userId and using include_player_ids instead. Our system attempts to keep our OneSignal player / user id the same even if the user fully uninstalls and reinstalls your app.

And from docs you will see `include_player_ids` param: 

> include_player_ids: array of stringsOptional. Targeting parameter. An array of OneSignal user IDs (also known as player IDs)

From your server you should do a `POST` to https://onesignal.com/api/v1/notifications with:

```json
{
  "app_id": "...",
  "contents": { "en": "Custom Content" },
  "headings": { "en": "Custom Heading" },
  "data": { },
  
  "include_player_ids": [ "userIdValue"]
}
```

![]( {{ site.path-emoji-tada }} )

# Thanks to

[Barista Ventures](barista-v.com) and [Sebastian Arcila](https://twitter.com/sarcilav) for the support and help 

[0]: (https://documentation.onesignal.com/v2.0/docs/notifications-create-notification)


