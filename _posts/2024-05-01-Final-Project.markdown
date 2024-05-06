---
layout: post
title:  "Car accidents in NYC"

carousels:
  - images: 
    - image:  /assets/images/Year.png
    - image:  /assets/images/Month.png
    - image:  /assets/images/Weekday.png
    - image:  /assets/images/Hour.png
  - images: 
    - image:  /assets/images/YearlyNormal.png
    - image:  /assets/images/MonthlyNormal.png
    - image:  /assets/images/WeeklyNormal.png
    - image:  /assets/images/HourlyNormal.png
  - images: 
    - image:  /assets/images/YearlyRain.png
    - image:  /assets/images/MonthlyRain.png
    - image:  /assets/images/WeeklyRain.png
    - image:  /assets/images/HourlyRain.png
  - images: 
    - image:  /assets/images/YearlySnow.png
    - image:  /assets/images/MonthlySnow.png
    - image:  /assets/images/WeeklySnow.png
    - image:  /assets/images/HourlySnow.png  
  - images: 
    - image:  /assets/images/YearlyVO.png
    - image:  /assets/images/MonthlyVO.png
    - image:  /assets/images/WeeklyVO.png
    - image:  /assets/images/HourlyVO.png    
---  
---

<style>
  .container {
    display: flex;        /* Flexbox layout to align children side by side */
    justify-content: center; /* Center the plots horizontally */
    align-items: center;  /* Align the plots vertically */
    gap: 20px;            /* Space between the plots */
  }
  .plot {
    border: 1px solid #ccc; /* Optional border for better visibility */
    padding: 10px;
  }
</style>



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

This initial data exploration does not provide much insight. Some logical daily and weekly trends are apparent, but hte reasoning for these can only be guessed at. The next sections of this website will attempt to model the data with corresponding weather data, to examine if there are apaprent correlatations in accidents in NYC, and the weather of NYC. First each weather type will be examined individually, followed by a comparison of the different weather types. 

<br>

The website will explore three different types of weather data; <strong>Normal Weather</strong>, <strong>Rainy</strong>, and <strong>Snowy</strong>. 'Normal Weather' simply means that there are no current weather conditions that might impair driving ability. So, a cloudy hour and a sunny hour will both be considered 'Normal Weather'. 

 <header>
        <h1>Weather Type: Normal Weather</h1>
 </header>

First, the 'Normal Weather' category is examined. Naturally, there are a much higher number of accidents for this weather type, as it is usually not raining or snowing. This will be taken into account when the data is compared, but first, some simple exploration.

  {% include carousel.html height="50" unit="%" duration="7" number="2" %}

Since normal weather is a year round occurence, and by far the most normal weather condition, the initial barplots do not vary significantly from those that were presented earlier.  

<br>

Now let's look at the areas in which the occurences are happening. The follwing is a bubble-plot, where the bubble size and color indicates the number of reported accidents for each area. 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/bubblemap_normal_weather.html"
           width="1100"
           height="600"
           >
</div>

This plot is a good indicator as to where one should be extra careful, or perhaps, where law enforcement should examine possible changes to counter the higher number of events. 

<br>

To get a more specific look at the happenings, the following plot displays the areas with the most occurences. 


<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Normal_Weather_map.html"
           width="1100"
           height="600"
           >
</div>

These happenins vary from minor bumps to deadly accidents. Naturally, the main focus should be to prevent deadly accidents. The plot below, displays a bubble-plot of places where deadly accidents have occured. 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/deaths_events_bubblemap_normal_weather.html"
           width="1300"
           height="600"
           >
</div>


 <header>
        <h1>Weather Type: Rain</h1>
 </header>


 {% include carousel.html height="50" unit="%" duration="7" number="3" %}

  * Rain

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/bubblemap_rain.html"
           width="1100"
           height="600"
           >
</div>

Much simpler due to fewer instances.

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/deaths_events_bubblemap_rain.html"
           width="1300"
           height="600"
           >
</div>

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Rain_Present_map.html"
           width="1300"
           height="600"
           >
</div>


 <header>
        <h1>Weather Type: Snow</h1>
 </header>

 {% include carousel.html height="50" unit="%" duration="7" number="4" %}


<div class="container">
    <div class="plot">
        <embed 
               type="text/html" 
               src="/assets/html/bubblemap_snow.html"
               width="550"   
               height="600"
               >
    </div>
    <div class="plot">
        <embed 
               type="text/html" 
               src="/assets/html/deaths_events_bubblemap_snow.html"
               width="550"   
               height="600"
               >
    </div>
</div>


<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Snow_Present_map.html"
           width="1100"
           height="600"
           >
</div>

<header>
        <h1>Weather Type: Vision obstruction</h1>
 </header>

{% include carousel.html height="50" unit="%" duration="7" number="5" %}

  * Rain

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/bubblemap_rain.html"
           width="1100"
           height="600"
           >
</div>

Much simpler due to fewer instances.

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/deaths_events_bubblemap_rain.html"
           width="1300"
           height="600"
           >
</div>

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Rain_Present_map.html"
           width="1300"
           height="600"
           >
</div>


 <header>
        <h1>Weather Type: Snow</h1>
 </header>

 {% include carousel.html height="50" unit="%" duration="7" number="4" %}


<div class="container">
    <div class="plot">
        <embed 
               type="text/html" 
               src="/assets/html/bubblemap_snow.html"
               width="550"   
               height="600"
               >
    </div>
    <div class="plot">
        <embed 
               type="text/html" 
               src="/assets/html/deaths_events_bubblemap_snow.html"
               width="550"   
               height="600"
               >
    </div>
</div>


<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Snow_Present_map.html"
           width="1100"
           height="600"
           >
</div>



<br>
<br>
<br>



#### Bubblemap of all collisions in different conditions (Rain, snow etc.) 

**This is a bubble map showing car accidents in new york city:** Note that the size and color changes based on the frequency of crashes at certain locations. 



<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/bubblemap_normal_weather.html"
           width="1100"
           height="600"
           >
</div>

 * Snow



 * Vision Obscuration
<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/bubblemap_vision_obscuration.html"
           width="1100"
           height="600"
           >
</div>


#### Heatemap of all collisions in different conditions (Rain, snow etc.) 

**This is a heatmap showing the density of crashes:** It is very important to note that the amount of crashes at one location has no impact on this visualization. It can purely be used to show the places where crashes are most dense. It makes sense that manhatten is a hotspot, since it is more densely packed with both people and crossings where accidents might happen.

 * Normal Weather

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap_normal_weather.html"
           width="1100"
           height="600"
           >
</div>


 * Rain

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap_rain_present.html"
           width="1100"
           height="600"
           >
</div>

 * Snow

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap_snow_present.html"
           width="1100"
           height="600"
           >
</div>

 * Vision Obscuration
<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap_vision_obstruction_present.html"
           width="1100"
           height="600"
           >
</div>


{% include image-gallery.html folder="/uploads/album" %}


