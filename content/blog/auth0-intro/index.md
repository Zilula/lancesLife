---
title: React 105 -- Intro to Auth0.
date: "2019-03-17"
---

Intro to Auth0

Last week I built a Twitter clone which as you probably could guess is an app that mimics twitters functionally. Beep! (my poorly named app) uses React and Redux on the front end and MongoDB with Mongoose to generate data schemas and store things. The two ends are pulled together using Auth0. Auth0 is a user authorization software who uses OAuth to verify user identities. But what is OAuth? OAuth is a massively popular authorization framework or protocol that allows applications to verify people without having them directly transmit their passwords. 

You've probably used OAuth before without even knowing it. Any time an application allows you to sign in with multiple methods, ie 'Sign up with Facebook!' or 'Login in with your Google+ account' OAuth is probably being used. It works by gaining access to checking your identity against that of the second site you used to log in with. It is also helpful to remember that OAuth is about authorization in particular and not directly about authentication. 
Created by Twitter and promoted by Google, OAuth has sustained popularity since its inception in 2010.  And this comes for a good reason. User authorization using Auth0 can be implemented in an application in a few hours if you have run through the process before. Of course, the complexity of the application comes into play. Simple front-end applications are easier to set-up within Auth0 but chances are if you aren't storing any data, Auth0 probably isn't even necessary. 


This post was to be used a simple intro to Auth0 and the next to be an in-depth article detailing how to actually apply Auth0 to a full stack application. 

Below is a great article detailing some aspects of OAuth.

[Great Article](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)