---
layout: post
title:      "Authorization ('Authentication')"
date:       2019-10-22 19:46:42 +0000
permalink:  authorization_authentication
---

In the Beer Log Web Development we created two users which is User A and User B, we used authentication and what authentication is doing is saying is this user who they claim to be. Meaning is this User A if so this user can only edit and modify there info and User B wouldn't be able to edit User A info. 

Within our code we use a method called `has_secure_password` and what this does is it sets and authenticate against BCrypt password. Which also need to use `password_digest` attribute with this method.

`user && user.authenticate(params[:password])` Here we are using a method called authenticate meaning is the user and the password match up then will return `true` but if either of them is wrong will return `false`
# Sessions 
Are cookies they have two type of cookies, session and persistent. Session allows a website to keep track of your movement from page to page for that specific session. Session allows you to navigate through the site without repeatedly having to authenticate yourself on every page. Session only expire if you logout or navigate away from the website. The persistent allows a website to remember you user information and other preferences for future access of the web. The difference is a session cookie is stored temporarily stored on your web browser and a persistent cookie is stored on your computer.

## In my Beer Log Web 
I use sessions in order to create cookie and when a user for visit the site you must first create a login with email and password and this information will continue to save on the web browser and keep the user login unless you logout to expire the session.
# Parameters
Parameters are hashes that stores the key value pairs that were encoded inside of HTTP request. Params is a way to access data that is passed around through our encoded HTTP requests.

