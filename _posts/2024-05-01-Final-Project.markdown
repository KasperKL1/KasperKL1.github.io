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
  - images: 
    - image:  /assets/images/NormalCont.png
    - image:  /assets/images/RainCont.png
    - image:  /assets/images/SnowCont.png
    - image:  /assets/images/VOCont.png      
---
<style>
       .tab {
       background-color: #f1f1f1;
       border: none;
       color: black;
       padding: 10px 24px;
       text-align: center;
       text-decoration: none;
       display: inline-block;
       font-size: 16px;
       margin: 4px 2px;
       transition-duration: 0.4s;
       cursor: pointer;
       }

       .tab:hover {
       background-color: #555555;
       color: white;
       }

       .tab.active {
       background-color: #555555;
       color: white;
       }

       .button-container {
       display: flex;
       justify-content: center;
       margin-bottom: 20px;
       }

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

These basic visualizations provides an overview of the data, and examining these plots provides some initial insights. <strong>Yearly</strong>, there is a steady incline up until covid hits in 2020, whereafter there is a steep decline in accidents. <strong>Monthly</strong>, there seems to be more accidents happening in the later months of the year.  <strong>Weekly</strong>, There seems to be a steady incline between monday to friday, before a drop off in the weekends. Intuitively, it makes sense that there are fewer accidents in the weekends, as fewer people will be on the road. Finally, the hourly results tells us that there is a peak in rates around the time people are driving home from work (at 16-17 pm), as well as a smaller peak when people are driving to work (at 8-9 am).

<br>

To get a more detailed look, the weekly data has been divided, so hourly data is available for each day of the week. By choosing the day(s) we wish to examine, we can get a more detailed look into the trends of each weekday. For example, if we look at the days monday-friday and compare them to sunday/saturday, it is apparent that, while there are more accidents in the weekdays, the weekend sees an increase in acidents in the nighttime. Choose the day(s) you want to examine in the plot below: 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Bokeh.html"
           width="1100"
           height="400"
           >
</div>

The same can be done on a yearly basis. Use the Legend to isolate the year(s) you wish to examine. Interesitng patterns to examine here, could be the rise of COVID in 2020, that sees a clear drop in accidents. But overall, there does not seem to be a clear apparent pattern in the montly data. 


<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/Bokeh2.html"
           width="1100"
           height="400"
           >
</div>

This initial data exploration does not provide much insight. Some logical daily and weekly trends are apparent, but the reasoning for these can only be guessed at. The next sections of this website will attempt to model the data with corresponding weather data, to examine if there are apaprent correlatations in accidents in NYC, and the weather of NYC. The website is divided into section, where each section is a different type of plot, and each weather type is plotted. The website will explore four different types of weather data; <strong>Normal Weather</strong>, <strong>Rainy</strong>, <strong>Snowy</strong>, and <strong>Vision Obscurred</strong>. 'Normal Weather' simply means that there are no current weather conditions that might impair driving ability. So, a cloudy hour and a sunny hour will both be considered 'Normal Weather'. Vision Obscurred are the hours with fog or haze, or any vision obstructing phenomena, that is not rain or snow. 


<header>
        <h1>Comparison of instances</h1>
 </header>

First, let's compare the weather data, in an hourly basis to see if there are apparent trends for each weather type and the number of accidents. Use the three buttons below to choose the plot you wish to see. 'All Instances' will display the average number of accidents per hour, regardless of weather. 'Crashes with injuries' will display the average number of accidents per hour, where injuries to one or more persons as a result. 'Fatal Crashes'  will display the average number of accidents per hour, where one or more persons were killed. Further, you can isolate the weather type by clicking them in the legend of each plot. 

<div class="button-container">
  <button class="tab" onclick="openMap(event, 'ComparisonTotal', '/assets/html/ComparisonTotal.html')">All Instances</button>
  <button class="tab" onclick="openMap(event, 'ComparisonInjured', '/assets/html/ComparisonInjured.html')">Crashes with injuries</button>
  <button class="tab" onclick="openMap(event, 'ComparisonKilled', '/assets/html/ComparisonKilled.html')">Fatal Crashes</button>
</div>

<div id="ComparisonTotal" class="map">
  <embed type="text/html" src="/assets/html/ComparisonTotal.html" width="800" height="400">
</div>
<div id="ComparisonInjured" class="map" style="display: none;">
  <embed type="text/html" src="/assets/html/ComparisonInjured.html" width="800" height="400">
</div>
<div id="ComparisonKilled" class="map" style="display: none;">
  <embed type="text/html" src="/assets/html/ComparisonKilled.html" width="800" height="400">
</div>

Combining the findings in each plot provides some understanding of the trends in the data. Let's look at these findings. 
<br>

**Normal Weather:** Normal Weather functions as a baseline throughout this webpage. This data basically provides insight into how the data acts, when weather is not a factor. 

**Snow:** For 'All Instances', all weather types generally follows the same pattern. Snow appears to be the biggest outlier in the morning rush hours, meaning that when people are rushing to work, the slippery roads creates more accidents. Interestingly, these peak in instances do not result in a peak in instances with injuries, and later in the day, when the number of Snow instances are pretty much the same as the other weather types, there are fewer injuries than for the other weather types. This could indicate, that the accidents in snowy weather are less severe, probably due to lower speeds. There is quite a relative peak for fatal injuries, seeing that in the nighttime there is a higher chance of being killed in snowy weather than the other. The numbers are very low for this section however, so it is difficult to provide a definite result. 

**Rain:** Rain follows the trend of Normal Weather pretty well. There are more injuries in the later hours, but for most hours in the total accidents, Rain actually ranks below normal weather. Fatal crashes is once again difficult to read, as there is relatively very few rows where there are fatalities, but the data once again follows Normal Weather nicely, although Normal Weather is much more smoothed, due to a much higher count of that weather type. 

**Vision obscuration:** Vision obsscuration provides more accidents later in the day, and results in an upswing in injuries as well. Meaning in the darker hours, the fog will provide a higher risk of accident and injury. 


In addition to happenings, we can also look at the top contributing factors for each weather type. Meaning, the reported reason for the collision. Note, that we have included 'Unspecified', as it is by far the most common input. 


 {% include carousel.html height="50" unit="%" duration="7" number="6" %}

The factors for each type are very much alike. Slippery pavement for Snow is perhaps the biggest outlier, which is of course a natural cause for accidents in snowy weather. The contributing facors do not provide specific insights. 

 <header>
        <h1>Bubblemap of all instances</h1>
 </header>

After looking at the comparisons of each weather type, let's look at where the accidents happen. The **Bubble-Plot** below displays each location where an accident has happend as a bubble, with the size and color of the bubble indicating number of instances per location. Once again, you can use the buttons to choose weather type. Hover your mouse over a bubble to see the data of that bubble. 

<div class="button-container">
  <button class="tab" onclick="openMap(event, 'bubblemap_normal_weather', '/assets/html/bubblemap_normal_weather.html')">Normal Weather</button>
  <button class="tab" onclick="openMap(event, 'bubblemap_vision_obscuration', '/assets/html/bubblemap_vision_obscuration.html')">Fog/Mist/Haze</button>
  <button class="tab" onclick="openMap(event, 'bubblemap_rain', '/assets/html/bubblemap_rain.html')">Rain</button>
  <button class="tab" onclick="openMap(event, 'bubblemap_snow', '/assets/html/bubblemap_snow.html')">Snow</button>
</div>

<div id="bubblemap_normal_weather" class="map">
  <embed type="text/html" src="/assets/html/bubblemap_normal_weather.html" width="800" height="650">
</div>
<div id="bubblemap_rain" class="map" style="display: none;">
  <embed type="text/html" src="/assets/html/bubblemap_rain.html" width="800" height="650">
</div>
<div id="bubblemap_snow" class="map" style="display: none;">
  <embed type="text/html" src="/assets/html/bubblemap_snow.html" width="800" height="650">
</div>
<div id="bubblemap_vision_obscuration" class="map" style="display: none;">
  <embed type="text/html" src="/assets/html/bubblemap_snow.html" width="800" height="650">
</div>

This plot is useful to identify specific spaces in the city, where you might want to be extra careful when manourvering in the different types of weather. It might also be relevant in identifying places in the city, where risk is apparent due to, perhaps, some unsafe traffic constellation. As there is a big difference in number of hours for each weather type, there is also a big differnece in instances. Notice therefor the legend to the right of each plot, indicating the number that each bubble represents. Looking at the vizualizations, the locations are very similar for each weather type. The busy intersections, are the leading culprite for all weather types. 

<br>

#### Heatmap of all collisions in different conditions (Rain, snow etc.) 

This is a **heatmap** displays the density of crashes. This gives an indication of the areas where the accidents occur. It is very important to note that the amount of crashes at one location has no impact on this visualization, like it did in the Bubble-plot. It can purely be used to show the places where crashes are most dense. It makes sense that Manhatten is a hotspot, as it is more densely packed with both people and crossings where accidents might happen.

<div class="button-container">
  <button class="tab" onclick="openMap(event, 'heatmap_normal_weather', '/assets/html/heatmap_normal_weather.html')">Normal Weather</button>
  <button class="tab" onclick="openMap(event, 'heatmap_vision_obstruction_present', '/assets/html/heatmap_vision_obstruction_present.html')">Fog/Mist/Haze</button>
  <button class="tab" onclick="openMap(event, 'heatmap_rain_present', '/assets/html/heatmap_rain_present.html')">Rain</button>
  <button class="tab" onclick="openMap(event, 'heatmap_snow_present', '/assets/html/heatmap_snow_present.html')">Snow</button>
</div>

<div id="heatmap_normal_weather" class="map">
  <embed type="text/html" width="800" height="650">
</div>
<div id="heatmap_rain_present" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="heatmap_snow_present" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="heatmap_vision_obstruction_present" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>

Once again, the plots displays the same trends, regardless of weather. 


#### Number of collisions at same location that resulted in at least 1 injury

Now let's look at where the instances happen, that results in one or more injuries. Once again, you can use the buttons to display the map for each weather type. The map is a Bubble-plot, with the same functions as earlier. 

<div class="button-container">
  <button class="tab" onclick="openMap(event, 'injury_events_bubblemap_normal_weather', '/assets/html/injury_events_bubblemap_normal_weather.html')">Normal Weather</button>
  <button class="tab" onclick="openMap(event, 'injury_events_bubblemap_vision_obstruction', '/assets/html/injury_events_bubblemap_vision_obstruction.html')">Fog/Mist/Haze</button>
  <button class="tab" onclick="openMap(event, 'injury_events_bubblemap_rain', '/assets/html/injury_events_bubblemap_rain.html')">Rain</button>
  <button class="tab" onclick="openMap(event, 'injury_events_bubblemap_snow', '/assets/html/injury_events_bubblemap_snow.html')">Snow</button>
</div>

<div id="injury_events_bubblemap_normal_weather" class="map">
  <embed type="text/html" width="800" height="650">
</div>
<div id="injury_events_bubblemap_rain" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="injury_events_bubblemap_snow" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="injury_events_bubblemap_vision_obstruction" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>

For normal weather, the plot displays some areas with a more dense bubble-population than the previous bubble plot, in the southeast and the north of the plot. This indicates, that there are areas where less accidents happen, but these accidents are more likely to result in injury. These maps are once again useful, to look at specific location and identify, where there might be room for improvement. An example is the large red dot on the Verrazano Bridge during Fog/Mist/Haze. This indicates, that for this location, there is a real risk factor during foggy weather, and the accidents that happen are severe enough to result in injuries. 

#### Number of collisions at same location that resulted in at least 1 fatality

Now that we've looked at insatcnes and injuries, this bubble-map displays the places where fatalities happen. Fatalities are, relatively rare, and the larger bubbles are typically stand alone instances where multiple people have died. 

<div class="button-container">
  <button class="tab" onclick="openMap(event, 'deaths_events_bubblemap_normal_weather', '/assets/html/deaths_events_bubblemap_normal_weather.html')">Normal Weather</button>
  <button class="tab" onclick="openMap(event, 'deaths_events_bubblemap_vision_obstruction', '/assets/html/deaths_events_bubblemap_vision_obstruction.html')">Fog/Mist/Haze</button>
  <button class="tab" onclick="openMap(event, 'deaths_events_bubblemap_rain', '/assets/html/deaths_events_bubblemap_rain.html')">Rain</button>
  <button class="tab" onclick="openMap(event, 'deaths_events_bubblemap_snow', '/assets/html/deaths_events_bubblemap_snow.html')">Snow</button>
</div>

<div id="deaths_events_bubblemap_normal_weather" class="map">
  <embed type="text/html" width="800" height="650">
</div>
<div id="deaths_events_bubblemap_rain" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="deaths_events_bubblemap_snow" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>
<div id="deaths_events_bubblemap_vision_obstruction" class="map" style="display: none;">
  <embed type="text/html" width="800" height="650">
</div>

<br>

The plot is most useful in 'Normal Weather' as the sample size simply is not very large for the other weather types. 

<br>



<br>
<br>
<br>

<script>
function openMap(evt, mapName, mapSrc) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("map");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
    tabcontent[i].innerHTML = '';
  }
  tablinks = document.getElementsByClassName("tab");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  document.getElementById(mapName).style.display = "block";
  document.getElementById(mapName).innerHTML = '<embed type="text/html" src="' + mapSrc + '" width="800" height="400">';
  evt.currentTarget.className += " active";
}
</script>