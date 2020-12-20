---
layout: post
title:      "RetailComp"
date:       2020-12-19 18:31:40 -0500
permalink:  retailcomp
---


### The goal of RetailComp is to facilitate both a more informed and uninterrupted shopping experience for customers as well as a more efficient and productive work-flow for employees, by being an App that displays the store's discount schedule on large screens throughout sales floors with an added feature of a Store locator  should a customer request that information.
### |
## DISCOUNT SCHEDULE
### The Discount Schedule which is the main feature of RetailComp, is coded using the React.js framework and doesn't rely on anything externally as a data source.
### |
### From the perspective of the business model:
* New merchandise is ticketed with one of five colors depending on the week.
* Different colors are put on sale or ragged out depending on how long the merchandise has been on the sales floor.

### Using a utility function calculating days passed, every seven days, a ' week: ' key in a Redux store gets assigned a value between 1 and 5 inclusive and depending on the value of that key, 2 of 10 Presentational Components are rendered - letting customers know what's on sale that week and in a less emphasized way,  reminding employees what color is coming in and what's color(s) are being ragged out.
### An example of what may be rendered on a particular week.

#### WEEKLY DISCOUNTS
* |ic white, ro blue, nw ro pink
* GREEN 50% OFF
* YELLOW 50% OFF
* PINK 99 CENTS!
#### In big bold font would be the weekly discounts and displayed in a smaller font would be the other text reminding employees of what's coming in, and what's being ragged out.
-------------------------------------------------
### This alleviates several pain points. The most important of which is a customer having to continually exit their shopping flow to find where the Board displaying the Discounts is,  or to find an employee to ask who themselves might have forgotton and would have to look at the Board.  Both scenarios lead to a disjointed and less enjoyable shopping experience for customers.
### |
### The second pain point RetailComp alleviates is on the employee end where employees would know at a single glance upward to one of lets say three or four screens, the incoming and ragout information, instead of having to scramble to get the information from a calendar which could easily be misplaced or misread when in a rush, leading to the wrong color tag being put out on the floor or the wrong color tag ragged out from the floor.  Both of these are scenarios that happen countless times over the course of a year as a result of normal human error.
---------------------------------------------------
### |
## STORE LOCATOR
### The Store Locator feature is also coded in the React.js framework but relies on a Rails backend which is accessed as an api.
### |
### At the back of a Rails stack is an SQLite table ' stores ' with columns for things such as Store name, number, location, city, etc.
### Routes are enabled and Controller end-points setup for Create, Read, Update and Delete functionality on Stores which are made available in JSON format for the React frontend to access.
### |
### From the perspective of the business model: A customer didn't find everything they were looking for and asks for a store list.  The employee brings up a store list on a screen and the information is there for the customer to do whatever they want with it.
### |
### The pain point alleviated is an employee having to either provide that information from memory or thumb around for a store list which often runs out.  Having that list available on screen alleviates stress for both customers and employees.
###  |
### A fetch GET request is sent upon mounting of the Stores feature and all stores are retrieved from the Rails index action, funneled into a ' stores ' key in the Redux store, which is mapped to and rendered to the screen for users.
### | 
### Double clicking a store will send a get request to the Rails show action passing in the id of the store as a parameter.  The response is funneled into a ' store ' key in the Redux store which is also mapped to and rendered.  And a similar process is achieved to update the information of a store.  
### React Router is used to create separate Routes for RetailComp's Discounts and Stores features as well as a Route to enable the creation of new stores.






