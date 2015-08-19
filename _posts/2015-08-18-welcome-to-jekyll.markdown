---
layout: post
title:  "JobMapper for Viking Code School"
date:   2015-08-18 09:21:45
categories: interning
author: Alex Sell
permalink: viking-intern
image: /job-mapper-image.png
excerpt: An application I worked on while interning for Viking Code School.
---
This is an application that I built for [Viking Code School](http://www.vikingcodeschool.com/), an online software development training program.

The application gives Viking Code School's registered students a chart that visualizes employment opportunities throughout the country, featuring 16 different technologies and over 500 U.S cities.

An automated rake task is set up to scrape [Indeed.com](http://www.indeed.com/), an employment-related search engine. Using the scraping gem 'Mechanize', each individual technology is queried alongside each city and the relevant search results are then collected and stored into the database. Heroku scheduler then ensures that this task functions every week, thereby preventing stale data.

With the data set in place, it is then formatted as JSON from a 'search_results' controller. Google Developers Visualization: Geochart is then implemented to present the data on a map of the United States. Built as a single page web application, a user can now click on a button, which will trigger an AJAX request to the appropriate JSON file, thus rendering a new map, all without a single page reload.

It has been an awesome experience working with the guys from Viking.

Technologies Implemented:

[Mechanize](https://github.com/sparklemotion/mechanize)

[Google Developers Visualization:Geochart](https://developers.google.com/chart/interactive/docs/gallery/geochart?hl=en)

[Bootstrap](http://getbootstrap.com/)

[PostgreSQL](http://www.postgresql.org/)

[Heroku Scheduler](https://addons.heroku.com/scheduler)
