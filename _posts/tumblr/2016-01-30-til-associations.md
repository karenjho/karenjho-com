---
layout: post
title: 'TIL: Associations'
date: '2016-01-30T21:31:08-05:00'
tags:
- til
- today i learned
- bitmaker
- bitmaker labs
- coding
- rails
- associations
- databases
- programming
tumblr_url: http://karenjho.com/post/138380589620/til-associations
---
In an attempt to segregate purely technical posts from the personal posts, I’m introducing a series called Today I Learned (TIL). A TIL will essentially be a summary or rehash of my Bitmaker notes on a particular topic. This first TIL is all about database associations, the relationships between the different models (tables) in the database.Associationsbelongs_to: defined in the “child” model. An instance of a model can “belong_to” only one specific instance of another model, but can also belong to specific instances of other models. A child belongs to a mother (and has only one mother) but also belongs to a father (and has only one father).has_many: defined in the “parent” model. An instance of a model can “have_many” instances of another model.A mother has many children.has_one: defined in the “parent” model. An instance of a model only “has_one” instance of another model.A family member has one room in the house.has_many, through: defined in both models on either side of the relationship. An instance of a model “has_many” instances of another model, “through” a third model.A neighbourhood has many families, through the houses those families live in. A family can live in many neighbourhoods, through the different houses they live in.has_one, through: defined in both models on either side of the relationship. An instance of a model “has_one” instance of another model, “through” a third model.A father has one son-in-law through his daughter. A man has one father-in-law through his wife.has_and_belongs_to_many: defined in both models on either side of the relationship. An instance of a model “has_many” instances of another model, and “belongs_to_many” instances of that model, too—with no tangible link (i.e. a third model) between the two.An athlete “has_many” sports teams, and a sports team “has_many” athletes. Inversely, an athlete “belongs_to_many” sports teams and a sports team “belongs_to_many” athletes.
