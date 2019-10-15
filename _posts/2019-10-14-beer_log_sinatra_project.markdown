---
layout: post
title:      "Beer Log (Sinatra Project)"
date:       2019-10-14 19:55:59 -0400
permalink:  beer_log_sinatra_project
---


 This project was an amazing experience for me. I always wanted to be a front end developer but doing this sinatra project got me really testing my web development skills and learning how the web browser url routes work. I always wanted to build an web application where your able to keep your logs about places you go and experience and the beverages or food you have tried all in a web application.

 In my experience there are so many breweries and bars out there it's so hard to keep track and we trying to use notebooks and pencil but it is such a hassle to carry. We or I a beer drinker would love to keep a log of all the beers and review about them. Well I created this Beer Log web where it keeps track of all your logs that you create. To keep track of all the beers you tried. You can signup as a new user or login and create or edit your first or many beer logs and delete the ones you don't need it's all done here on the beer log web. 
						
I further want to enhance my css skills as well as my html I love the aspect of design a website and make look amazing. The backend is fascinating as well where I am able t build encryption password for the user and instead of going to a website and signing in I was able to create a login and singup for a user myself. This open my eyes to the possibilites of what web development can do for me and the things I can create!

# The code below :
- Is where I created a table for Beer Logs and a user where I provided columns and attributes to the database.
						
```
class CreateBlogs < ActiveRecord::Migration
  def change
    create_table :blogs do |t|
      t.string :title
      t.string :brewery
      t.string :name
      t.string :body
      t.integer :user_id
      t.timestamps
    end
  end
end
```

- Here I created to classes where one is a Beer Log class where it belongs to the user and the User class has many   beer logs as well as validation of the attritbute to make sure that uneccessary data doesn't get inputted in. 

```
class Blog < ActiveRecord::Base
    belongs_to :user
    validates :title, :body, presence: true
end 

class User < ActiveRecord::Base
    has_many :blogs
    has_secure_password # allows to do the encryption 

    validates :name, :email, presence: true
end
```
