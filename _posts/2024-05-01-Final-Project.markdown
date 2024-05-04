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

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap.html"
           width="1100"
           height="600"
           >
</div>

INSERT BOKEH HVOR MAN KAN VÆLGE UGEDAGE OG FÅR TIMEVÆRDIER FOR UGEDAGENE. 
INSERT BOKEH HVOR MAN KAN VÆLGE ÅR OG FÅ MÅNEDER Bign

<br>








### HeatMap of all collisions in different conditions (Rain, snow etc.) 
<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/ny_map.html"
           width="1100"
           height="600"
           >
</div>