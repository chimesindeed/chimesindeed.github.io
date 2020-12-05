---
layout: post
title:      "Updating State in Redux Store with Object.assign() - Quick Reference"
date:       2020-12-05 04:56:43 +0000
permalink:  updating_state_in_redux_store_with_object_assign_-_quick_reference
---


#### 1) First parameter of Object.assign(0 called target, will receive an empty object.  This is the clean slate your starting with.
#### 2) Having started from scratch with an empty object, the remaining parameters of Object.assign(0 will receive the sources of your pertinent data.

#### Because you're updating a particular variable in your state object, the first data source you want to put in your blank slate is you entire state object.

#### The next data source you want to pass in is the particular variable in state that you're updating.  So if you have a key called counter with an initial value of 0, and you're incrementing the state value, your, last parameter of Object.assign will be {counter: state.counter + 1}

#### So your Object.assign function now looks like this:  Obect.assign({}, state, {counter: state.counter + 1})
