---
layout: post
title:      "Index-Me (Study Aid)"
date:       2020-09-21 23:11:36 +0000
permalink:  index-me_study_aid
---


### I was almost a year down a full stack road, reaching the end of the Flatiron Software Engineering Immersive culminating in a final Single Page Application project to be coded using a React frontend and a Rails backend as an API.  The project is called Index-Me and aims to be an aide for students to organize their ideas on virtual index cards with which they can study from with a few clicks.

### The requirements are that the project have:
> 3 Routes handled by React-Router
> 5 Stateless Components
> 2 Containers
> Redux.js to hold State
> Redux Thunk to give Actions leeway to perform asynchonous requests to the Rails backend
## Functionality
### Three routes wrap Index-Me's functionality: A '/' root route which loads a component to greet the user, a 'createcard' route for a user to create an index card with a front and a back, which will create a card in a SQLite database at the back of a Rails stack, and a 'getcards' route, to wrap funtionality that retrieves all cards from the Rails backend.
### A Redux Store is created to hold 2 reducers, a 'cards' reducer to hold all cards retrieved from the backend and a 'form' reducer to hold the front and back of a created card to pass to a create action to store the card in the database.
## Takeaways
### I like that React architecture is so contained and therefore very modular.  With JSX syntax, HTML and JavaScript are specific to components which can be moved around, swapped out, and edited in an organized fashion without breaking your app, or having to refactor much of your code base.  What I like most about React though is regarding React State that firstly: you're not mutating objects but seemlessly creating new ones which has a very clean feel to it.  Secondly: that when State is bridged to any Component it is passed to a local variable as a property.  What I like about this is that at a Component level you're not dealing with State directly when either rendering State, or using State in conditional logic, etc., which also has a very clean feel to it.  
### Tight coupling regarding passing State from one Component to another initially caused friction in learning because it limited freedom regarding what was declared as State where, and what Components were rendering other Components - but this was thankfully answered by the use of a Redux Store.
