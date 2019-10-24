# Android Event Reporter: 

## Business Design
  - To build a LBS(Location-based service) based Android App To help customers explore nearby events on google Map.

## General Instruction
1. Employed Google Firebase to managing UGC(User-generated content) including comments, images and descriptions online.
2. Integrated Google Map API to display the popular events nearby and event navigation route.
3. Applied Google advertisers with Google AdMob and keeping users engaged.
4. Implemented infinite loading list to display list of users' posts using RecyclerView with mixed-type adapter.
6. Added automatically sending push notifications feature with Firebase Cloud Messaging and Firebase Cloud Function. 

## Android Platform Architecture Review
![Platform Architecture](https://github.com/lyluke/EventReporter/blob/master/Res/Part%20of%20Android%20Platform%20Architecture.png?raw=true)
> Part of Android Platform Architecture

![Android Life Cycle](https://github.com/lyluke/EventReporter/blob/master/Res/Screen%20Shot%202019-10-23%20at%209.04.48%20PM.png?raw=true)
> Android Life Cycle

## Activity Design
### Login Activity
  - Users can register their ID and password on this activity. Log in data will be stored in the firebase. An util class has been created to encrypt the password using MD5 hashing algorithm.
![Login](https://github.com/lyluke/Android-Event-Reporter/blob/master/Res/LogIn.png?raw=true)
> Login Activity Layout
