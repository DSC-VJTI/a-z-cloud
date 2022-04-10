---
title: "G"
linkTitle: "G"
weight: 4
description: >
  ## Geographic Information System
---

A geographic information system (GIS) is a system that creates and manages geographic data (data for which location is relevant), analyzes this geographic data, and maps it. Hence the four main ideas of such as system are:

- Create geographic data

- Manage it in a database

- Analyze and find patterns

- Visualize it on a map

You can find the use of GIS in a food delivery tracker in a mobile app where the location of your meal is continually fethced from an API providing geographic data. This data is then analyzed to give you an estimated time of delivery and all of this is being mapped and visualized in the mobile app in real-time.

### How does cloud computing come into the picture?

- Geographic data such as location or coordinates along with spatial data such as the shapes that make up a geography such as a point, line, polygon, etc. These data together form geospatial data which is complex in nature and takes up a lot more space than the traditional relational data. Hence cloud is leveraged to store copious amounts of such data and analysis is carried out using Big Data services such as BigQuery.

- With the COVID-19 pandemic, it became essential to create visualizations of real-time changes in COVID cases. To manage such real-time changes, data from several APIs needs to be consumed to produce a new change and hence, services such as Cloud Pub/Sub can be seen here.
