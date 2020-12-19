---
layout: post
title:      "Updating State in Redux Store with Object.assign() - Quick Reference"
date:       2020-12-04 23:56:44 -0500
permalink:  updating_state_in_redux_store_with_object_assign_-_quick_reference
---

### Object.assign(target, source1, souce2)
#####
#### First parameter of Object.assign - called target, will receive an empty object.
#####
#### This is a clean slate.  You're starting from scratch.
#####
#### The remaining parameters of Object.assign - are the sources of your pertinent data.
#####
#### The first data source you want to put in your blank slate is you entire state object.
#####
#### So things look like this | ->  Obect.assign({}, state)
#####
##### Your keys and values in your first source,  'state' -> are passed in to the blank object.
##### 
#### The next source you want to pass in -> is the particular key in state that you're updating.
#####
##### If you have a key called ' counter: ' which you want to increment . . . .
#####
##### {counter: state.counter + 1} would be the third parameter of Obect.assign() which would now look like,
#####
#### Object.assign( {}, state, { counter: state.counter + 1 }
#####
##### Note: Whatever the value of the ' counter: ' key is -> you're adding 1 to it ->
#####
##### assigning that value to a NEW ' counter:  ' key which then REPLACES the ' counter: ' key
##### 
##### in the ' state ' obejct you previously passed in as a source to your Object.assign() function.
#####
##### no data is getting mutated.
