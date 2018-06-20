---
layout: post
title:      "Gateway Sinatra"
date:       2018-06-20 15:47:01 +0000
permalink:  gateway_sinatra
---


Hi again, It's been a while. 

Let me talk to you about a little app i built called...you guessed it **Gateway Sinatra**
this app gives its users a platform for them to interact. 

How? well they ask questions. Originally it was ment for them to as about programing questions but then realized that what is to stop them from asking other questions? *sigh* Life...

**Early Process**

At the begining I knew what I wanted my app to be. What had me stumpted was how to approach it.
I came up with three models. 

1. User
2. Question
3. Comment

Now since I am not experienced enough I googled a vertual white board where I can draw out how I was going to associate them. 

from the very beginning I knew that a User will have many Questions and Comments. 
```
class User < ActiveRecord::Base
  has_many :questions
  has_many :comments
```

Then I knew that Questions will belong to a User but what about Comments. I cannot leave that little guy out...
that's when looking at some inspirations online plus thte help of that white board and my third grade drawing I figured out that Question will have many Comments and belong to a User. While my Comment model belongs to both a User and a Question. 

My Schema ended looking like this. 

```
create_table "comments", force: :cascade do |t|
    t.string  "content"
    t.integer "user_id"
    t.integer "question_id"
  end

  create_table "questions", force: :cascade do |t|
    t.string   "content"
    t.datetime "time_created"
    t.integer  "user_id"
  end

  create_table "users", force: :cascade do |t|
    t.string "username"
    t.string "email"
    t.string "password_digest"
  end
```

Having figured out my associations and testing them on Tux I was ready to begin. 



**...To The End**

I have been coding for two days straight.... no sleep just me, coffee, and my cat. 

kidding I slept. 

I was just having an issue with associating my comment routes to my questions. Plus trying to figure out if I wanted my comment form to appear bellow the the question being asked. 

this is becoming a long post. So how about this: [Gateway Sinatra](http://https://github.com/YanezDiego/Gateway-Sinatra) Check it out. tell me your thoughts and what you would add take away. 

Slack me @sebas 

Catch you next time. 


