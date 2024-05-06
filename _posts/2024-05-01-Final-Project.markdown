---
layout: post
title:  "Car accidents in NYC"

carousels:
  - images: 
    - image:  /assets/images/Year.png
    - image:  /assets/images/Month.png
    - image:  /assets/images/Weekday.png
    - image:  /assets/images/Hour.png
---



 <header>
        <h1>Exploring hotspots for car accidents in NYC between 2012 and 2023</h1>
 </header>
This website will explore reported car accidents in NYC in the years 2012 to 2023, and see if there are any locations that might be more endangering than others. The website will mainly focus on <strong>weather</strong> as a contributing factor, and examine if there are trends and coorelations to be spotted in accidents happening and weather conditions. 

First, some initial vizualization. Use the arrows to view the 4 different plots, displaying totals for yearly, monthly, weekly and hourly data.

<br>

  {% include carousel.html height="50" unit="%" duration="7" number="1" %}

<br>

These basic visualizations provides an overview of the data, and examining these plots provides some initial insights. <strong>Yearly</strong>, there is a steady incline up until covid hits in 2020, whereafter there is a steep decline in accidents. 2012 is low, as data doesn't begin until July of that year.  <strong>Monthly</strong>, there seems to be more accidents happening in the later months of the year.  <strong>Weekly</strong>, There seems to be a steady incline between monday to friday, before a drop off in the weekends. Intuitevly, it makes sense that there are fewer accidents in the weekends, as fewer people will be on the road. Finally, the hourly results tells us that there is a peak in rates around the time people are driving home from work (at 16-17 pm), as well as a smaller peak when people are driving to work (at 8-9 am).

<br>

To get a more detailed look, the weekly data has been divided, so hourly data is available for each day of the week. By choosing the day(s) we wish to examine, we can get a more detailed look into the trends of each weekday. For example, if we look at the days monday-friday and compare them to sunday/saturday, it is apparent that, while there are more accidents in the weekdays, the weekend sees an increase in acidents in the nighttime. 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Bokeh.html"
           width="1100"
           height="600"
           >
</div>

The same can be done on a yearly basis. Use the Legend to isolate the year(s) you wish to examine. Interesitng patterns to examine here, could be the rise of COVID in 2020, that sees a clear drop in accidents. But overall, there does not seem to be a clear apparent pattern in the montly data. 


<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Bokeh2.html"
           width="1100"
           height="600"
           >
</div>

This initial data exploration does not provide much insight. Some logical daily and weekly trends are apparent, but hte reasoning for these can only be guessed at. The next sections of this website will attempt to model the data with corresponding weather data, to examine if there are apaprent correlatations in accidents in NYC, and the weather of NYC. 

<br>

The website will explore three different types of weather data; Normal Weather, Rainy, and Snowy. 'Normal Weather' simply means that there are no current weather conditions that might impair driving ability. So, a cloudy hour and a sunny hour will both be considered 'Normal Weather'. 

 <header>
        <h1>Weather Type: Normal Weather</h1>
 </header>












### HeatMap of all collisions in different conditions (Rain, snow etc.) 
<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/ny_map.html"
           width="1100"
           height="600"
           >
</div>