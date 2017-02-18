---
title: Trying Firebase 3.0 Realtime Database for 1-1 chat in Kotlin
layout: post
categories: Android, Firebase
---

The idea is expose some code to have a reference on how to _query_ and _push_ things to [Firebase Realtime Database][0] to create a 1-1 chat with:

1. List of channels with me and someone involved.
2. Channel with all messages between me and other user

_Channel: 1-1 chat_

# Dependencies

{% gist caipivara/0f870979de12cfaa880c03d9ca9e7ea3 deps.gralde %}

_Note: Firebase DB UI is really cool and simple to list Firebase database objects and queries, check it out_

# Firebase Database usage

## Structure

[Firebase Realtime Database][0] use _JSON_ to define the database structure (yeah, at the end it will be a **BIG** _JSON_). So our database will look like:

{% gist caipivara/0f870979de12cfaa880c03d9ca9e7ea3 database.json %}

Check [Structure Data Guide][1]

## Database usage
We can query messages, channels and push messages into a channel with the next code:

{% gist caipivara/0f870979de12cfaa880c03d9ca9e7ea3 MyFirebaseDatabase.kt %}

_Note: we used some extensions to make Firebase calls and zip all the results in a easy way (will be better to use Firebase transactions instead ?)_

{% gist caipivara/0f870979de12cfaa880c03d9ca9e7ea3 FirebaseExtensions.kt %}

### Notes

1. For mesasges I used `push` from [Firebase Realtime Database][0] to avoid id conflicts 
1. If you want to make queries you should use any of `orderBy` functions.
1. Because the database is a _JSON_, `FirebaseDatabase.getInstance().reference.child("messages")`,  will get a `DatabaseReference` for all the messages **but as the direct child of messages is an _id_** (remember note 1.), you should use `.orderByChild("channelId")` and `.equalTo("channelIdValue")` to get all the children inside _messages_ that have `channelId == "channelIdValue"` (query by _children_ of _children_ attributes)
1. Databases are created with _just users authenticated with firebase auth_
 _read/write_ permissions, but you can make it public for read/write too, **it's ultra insecure, please dont**. 
1. To show the items you can use `FirebaseRecyclerAdapter` from `Firebase Database UI` package, check [Full post gist](https://gist.github.com/caipivara/0f870979de12cfaa880c03d9ca9e7ea3) for a sample.

# Thanks

[Barista Ventures](barista-v.com) and [Oscar Rendon](https://twitter.com/orendon) for the support and help.

# Guides
- [How to Structure Data][1]
- [Google IO Playlist- Deep dive into Realtime Database](https://www.youtube.com/watch?v=cYinms8LurA&index=8&list=PLl-K7zZEsYLlAyGS6_paVoGJ9YKC7J3NN)

[0]: https://firebase.google.com/docs/database/
[1]: https://firebase.google.com/docs/database/android/structure-data