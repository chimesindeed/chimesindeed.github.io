---
layout: post
title:      "Ruby Red Road"
date:       2020-09-05 23:22:52 -0400
permalink:  ruby_red_road
---


### THE BEGINNING
There I was 2 months into a Software Engineering immersive staring at the requirements of our first project due:
> Write an app in Ruby that provides a Command Line Interface with which a User can access to data from a web page.
> The data provided must go at least one level deep where a user can make a choice and get detailed information about their choice.
## _
The app I decided on, "Alotacookies," would be a CLI app that would scrape data from a Wikipedia site listing interesting and delicious cookies from around the globe, and at the user's request display cookie details, such as ingredients and country of origin.  Appealing to the child in me, I thought to myself that...my first project on this new road to becoming a Software Engineer would be tribute to my most favorite childhood...Cookie Monster, and I imagined the delight in Cookie's googly rolly eyes when he played with an app like "Alotacookies" on his smartphone. I imagine he'd be in cookie heaven.

### THE NITTY GRITTY

I opened a terminal in Ubuntu, used the bundle gem to setup the project skeleton, and created a file whose purpose would be to scrape data, requiring both the Open-uri and Nokogiri gems. Open-uri would be used to retrieve the Wikipedia site's HTML and store it as a file.  With Nokogiri, the raw HTML of the website would be parsed into XML objects, a format easier to address with Ruby code.

Firing-up the developer's console in the browser and moving the mouse around the page revealed that cookie data on this Wikipedia site was stored in 'tr' elements of a table.  Knowing that, I could now iterate over each 'tr' element and extract cookie name, country of origin, and cookie description which were stored in 'td' elements.

To make sure data was only scraped once, the only call to the scraper class was placed in the apps bin/executable file.  At end of the scraper class a call was placed to the main classe's - create - method which instantiated cookie objects for all cookies scraped and pushed them on to a Ruby class array.

With the functionality I needed to retrieve cookie data from Wikipedia working correctly, and the functionality to store that data app-side working correctly, the last step was to create a user-facing class to greet the user with a command line menu displaying app name, a brief description, options to display cookies and to exit app.

And there ya have it. "Alotacookies" was now complete. Cookie Monster, eat your heart out!
