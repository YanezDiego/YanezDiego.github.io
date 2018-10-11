---
layout: post
title:      "React & Rails Tips That Helped Me"
date:       2018-10-11 18:17:24 +0000
permalink:  react_and_rails_tips_that_helped_me
---



**We Made It!**

We have finally made it to the end. The final project. The epic conclusion of the past six months in the program.

***React - Redux with Rails Back-end***

I can officially say that personally, this project has been definitely the most challenging of them all, and as Programmers (you included reader) we love taking challenges head-on. For those who are reading this that are close to starting this final projects or just 


For those who are reading this that are close to starting this final projects or just curious about the thought process let me start you off with some tips.

***TIPS***

*Tip numero uno:*
	Probably people do this already but for those who do not This project took me preparation. Meaning that I had to draw it out in a paper of on Sketch App. I am a visual person so, drawing the actions, what component will render what really helped a lot. 

*Tip number 2:*
	For this tip, there's no right/wrong answer. I am just going to suggest what I hoped I knew before starting that eventually made it easier for me to handle both front-end & back-end. 

Before you start your project create your main directory with the classic `mkdir [app_name]`  before you run any `create app` command. this will make it easier to manage your Client & API files. 

After you `CD` inside your new App directory I highly suggest running your `create-react-app [app_name-client]` command. Now I named my front-end 'client'. I thought that repeating the name of the app again was redundant though again, perhaps is better to have the app name in front of  'client'. 

I focused on the client side first, going by my mock-up of how I wanted my components to interact. 

*Finally, Tip 3:*

Rails. Setting up your rails as a back-end API to hold your saved information I found pretty simple. The issue that I ran into was setting PostgreSQL . (That's another post) 

You will want to start your Rails API with `rails new [app_name_api] --api` inside my root directory. 

Do not forget to `bundle install`  

***Conclusion:***

What I took most about this project is that slow and steady wins. Plan, Plan, PLAN! 

There's a lot of moving parts in this kind of project so take it a step at a time. Especially when you're dealing with communicating between your Client & API.
