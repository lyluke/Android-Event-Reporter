# Android Event Reporter: 

## Business Design
  - To build a LBS(Location-based service) based Android App to help customers explore nearby events on google Map.

## General Instruction
1. Employed **Google Firebase** to managing UGC(User-generated content) including comments, images and descriptions online.
2. Integrated **Google Map API** to display the popular events nearby and event navigation route.
3. Applied Google advertisers with **Google AdMob** and keeping users engaged.
4. Implemented infinite loading list to display list of users' posts using **RecyclerView** with mixed-type adapter.
6. Added automatically sending **push notifications feature** with Firebase Cloud Messaging and Firebase Cloud Function. 

## Android Platform Architecture Review
![Platform Architecture](https://github.com/lyluke/EventReporter/blob/master/Res/Part%20of%20Android%20Platform%20Architecture.png?raw=true)
> Part of Android Platform Architecture

![Android Life Cycle](https://github.com/lyluke/EventReporter/blob/master/Res/Screen%20Shot%202019-10-23%20at%209.04.48%20PM.png?raw=true)
> Android Life Cycle

## Activity Design
### Login Activity
  - Users can register their ID and password on this activity. Log in data will be stored in the firebase. An util class has been created to encrypt the password using MD5 hashing algorithm.
  <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/LogIn.png" width="350">
  </p>

### Event Activity
  - Used event adapter to combine the comments and pics in the list view. Override recylerView to support unlimited ads.
  - Using recylerView could help to avoid slow rending issue. Pics on screen need to be rendered in 16 ms(50Hz). If not, will drop, which looks like stuck pages. To solved it , need to use parallel computering to fast it. Need to use recycle. 
  - Fixed **ANR(applicaiton not response)** issue by using async-task to load pics in the background threads.
  <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/EventListView.png" width="700">
  </p>
  
  - Added map fragoment with google map API to help users to check events on map.
  <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/EventMapFragoment.png" width="350">
  </p>

### Intent Between Activities
  - An Intent provides a facility for performing late runtime binding between the code in different
applications. Its most significant use is in the launching of activities, where it can be thought
of as the glue between activities. It is basically a passive data structure holding an abstract
description of an action to be performed.
  <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/Intent.png">
  </p>
  
 ### User Comment Activity
 - Added some comments for each event is also available.
   <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/Comments.png" width="350">
  </p>
  
 ### Push Notification
 - Firebase Cloud Messaging [(FCM)](https://firebase.google.com/docs/cloud-messaging) is a cross-platform messaging solution that lets you reliably deliver messages at no cost. Using FCM, you can notify a client app that new email or other data is available to sync. You can send notification messages to drive user re-engagement and retention.
   <p align="center"> 
    <img src="https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/Push%20Notice.png" width="350">
  </p>
