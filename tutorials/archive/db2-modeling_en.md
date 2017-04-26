<!---
layout: default
title: Database Modeling
--->



## Database Modeling

During this session we'll learn how to model the data inside your database. There are few approaches when it comes to model the database architecture. 

When modeling data, you can choose an approach best suited to the nature of the work to be done. The approaches to data modeling include the following: designing a new database, developing a design for an existing database, or performing maintenance on an existing database design:

* __Top-Down Modeling__: for designing a new database

* __Bottom-Up Modeling__: for creating a database based on extracting metadata from an existing database or using the DDL code obtained from an implementation of an existing database

* __Targeted Modeling__: for adapting a database to new requirements

We will consider only the first one: __Top-Down Modeling__, for simplicity, let's refer to that as __Modeling__.

### The __Top-Down Modeling__

So we have a task to create a database that will fit the needs of our project. This database has to gather information about business requirements and the internal environment, and proceeds to define processes, a logical model of the data, one or more relational models, and one or more physical models for each relational model. 

In other words, in order to be able to create a good enough DB architecture from the very beggining, we have to clearly understand:

* What the specifics of our project are? 
* What is the data that we will operate with?
* What are the technical limitations?

Answering these questions will help us find the right way to represent the data inside the DB.

Let's recall the `Product Engineering` session. We have created a schematic representation of our projects.

_[All the teams will need to have the drawn schema from `Product Engineering` session in front of them. During maximum 10 minutes the teams, and the mentors will prepare a short description of the features in the form of bullet points.]_

_[During another 15 minutes, we'll discuss these features. And on the example of Users we'll have a practical session of creating the Logigal model of a User.]_

Let's first of all define one of our Users. 

_[Work on user auth here]_