---
layout: post
title:      "My Rails Project - MovieApp"
date:       2020-03-16 19:51:23 +0000
permalink:  my_rails_project_-_movieapp
---


It’s project time with Ruby on Rails!  Rails is a web-application framework that includes everything needed to create a database-back web applications according to Model-View-Controller (MVC) framework. It took me a while to grasp the concept of MVC but once I did...WOW!  I have learned the most during this section of the curriculum.  To understand how to build an app is very powerful AND rewarding! 

I feel like we just take the internet for granted and the average person doesn’t really understand how it all works.  
MVC stands for:

* Models
* Views
* Controllers

These work together to navigate your internet experience. 

Models handle data and logic.  In my project, the models contain database information about  Movies, Actors and Roles.  When I create a new movie, actor and role, they are stored in the database and can be queried by the controller. The controller transmits data requests from the user to the model, and then delivers data that is rendered in the view to the user.  A view is the output of the query the user sees on the screen.  

In my MoviesApp you can create, edit and delete movies, actors and roles (CRUD functionality). The resources syntax is a very useful way to have Rails generate each of the CRUD routes for you.  To see your routes run ‘rails routes’ to get the following: 


```
                               Prefix Verb   URI Pattern    Controller#Action
      			             actor_roles GET    /actors/:actor_id/roles(.:format)
                                                  roles#index
                                      POST   /actors/:actor_id/roles(.:format)
                                                  roles#create
                       new_actor_role GET    /actors/:actor_id/roles/new(.:format)
                                                  roles#new
                      edit_actor_role GET    /actors/:actor_id/roles/:id/edit(.:format)
                                               roles#edit
                           actor_role GET    /actors/:actor_id/roles/:id(.:format)
                                                  roles#show
                                      PATCH  /actors/:actor_id/roles/:id(.:format)
                                                  roles#update
                                      PUT    /actors/:actor_id/roles/:id(.:format)
                                                  roles#update
                                      DELETE /actors/:actor_id/roles/:id(.:format)
                                                  roles#destroy
```


I also utilized third-party authentication (OAuth) via GitHub.  There are a few project requirements that needed to be met with this project regarding MVC.

Must include at least one has_many relationship
Must include at least one belongs_to relationship
Must include at least two has_many through relationships
Must include at least one many-to-many relationship
The “through” part of the has_many through includes at least one user submittable attribute, that is to say, some attribute other than its foreign keys that can be submitted by the app’s user

I have the following models:

* Movies
* Actors
* Roles
* Rating
* User

In order to include the above project requirements, In my MoviesApp:

* Movies and Actors have a many-to-many relationship
* Movies have many Actors, through Roles
* Actors have many Movies, through Roles
* Roles belong to an Actor
* Roles belong to a Movie

This has been quite the learning experience.  Once you get the ebb and flow of this, the possibilities are endless!

