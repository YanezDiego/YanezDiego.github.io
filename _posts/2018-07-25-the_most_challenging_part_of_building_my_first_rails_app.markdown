---
layout: post
title:      "The Most Challenging Part of Building My First Rails App."
date:       2018-07-26 00:28:03 +0000
permalink:  the_most_challenging_part_of_building_my_first_rails_app
---


Hello Reader, I see you are back. While you read the following blog post about my application note this:

**Though it was fun and I am proud of what I have accomplished so far. It was a difficult battle. A battle where hair has been pulled and heads banged against the table in despair.**

OK. Ready?

Building my first rails application has been an amazing experience. It has shown me how much I have grown as a ruby/rails developer and how much there is still out there to learn. It also has brought me peace knowing that I will not remember everything and google is my **BFF**. 

Before starting, I sat down and thought about what is something I wanted my application to have, and how I wanted it to function. 

I knew right off the bat that I needed to have a User and the User needs to be able to log in or sign up if its the first time to the app. So I created Notes and started to write things out. 

*note that bellow shows early stages of planning and does not resemble finished product*

```
  --- What My APP Should Do ---
  Authenticate Users through GitHub(for now)
[X]  A user can create/login to its profile.
[X]    users/new <= Sign up

        Switch User#Show (pets info) => Pets#index for user to see all its pets

[X]    login route
      get '/login' => sessions#new
      post '/login' => sessions#create
      get '/logout' => sessions#destroy


[X]    User can see his/her pets list and add pets

      pets have a show - edit - delete pages


  A user can add pets to its profile
      users/1/pets/ (shows all the pets associated to that user.)
      users/1/pets/new (renders pets#new form to add pet(s))
      users/1/pets/pets_id (individual pet with food diet.)
```

After writing things down it started to show a pattern, and a flow to follow. I started with what I considered easy for me. I began with the user signup form and sessions login. With that, I knew that I needed to start setting my routes for User and Sessions, then generate the controllers for both, and generate the User model with its corresponding table. I knew I wanted to give my User the ability to login with Github so I added a 'uid' row to my database. 

The flow consisted of writing code => check it => commit => check notes => repeat. When I reach an endpoint. I decided to go back and re-read my code to make sure there are things I can refactor. 

With that said, I leave you here reader. Thank You for your time. 


