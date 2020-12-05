---
layout: post
title:      "React Cheat Sheet"
date:       2020-12-05 05:23:03 +0000
permalink:  react_cheat_sheet
---


#### React from 'react'
##### to recognize JSX and integrate React Lifecycle methods

#### ReactDOM from 'react-dom'
##### To recognize ReactDOM.render method to render all virtual dom to HTML page.
#### { Provider } from 'react-redux'
##### In index.js - Wrap all of App in < Provider > Element to allow for any Component to connect to your Redux store.
#### { connect } from 'react-redux'
##### map any variable in your redux store to a prop in your Component listening for changes.  Dispatch actions to your redux store updating state.
#### { Switch, BrowserRouter, Route } from 'react-router-dom'
##### Wrap your app in < BrowserRouter > tag.  Declare your routes with < Route > tag.  Use < Switch > to declare one route at a time.
#### { createStore } from 'redux'
##### Pass your reducer to createStore method to implement a Redux Store.
