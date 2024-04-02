---
layout: post
title:  "Social Data Analysis and Visualization: Assignment 2"
date:   2024-03-31 14:40:25 +0200
categories: jekyll update
---


 <header>
        <h1>Bar charts displaying evolution of occurences</h1>
</header>
Firstly, we want to look at the different crime categories to determine which category has the most characteristic evolution over the years from 2003 to 2017.
<div style="display: flex; justify-content: center;">
    <img src="/assets/images/newplot.png" alt="Crime occurances">
</div>


We want to look at forgery/counterfeiting. Because this category seems to be decreasing rapidly in recent years. This could be due to the fact that documents are being digitalized more and more and therefore, these are not as easily forged as they were in the past.



To become more specific in our search, let's look at the number of occurences of forgery/counterfeiting per district. 

 <header>
        <h1>Table displaying occurences per district</h1>
</header>
<div style="display: flex; justify-content: center;">
    <table>
        <thead>
        <tr>
            <th>Count</th>
            <th>Category</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1669</td>
            <td>BAYVIEW</td>
        </tr>
        <tr>
            <td>2541</td>
            <td>CENTRAL</td>
        </tr>
        <tr>
            <td>2094</td>
            <td>INGLESIDE</td>
        </tr>
        <tr>
            <td>2764</td>
            <td>MISSION</td>
        </tr>
        <tr>
            <td>2808</td>
            <td>NORTHERN</td>
        </tr>
        <tr>
            <td>1045</td>
            <td>PARK</td>
        </tr>
        <tr>
            <td>1355</td>
            <td>RICHMOND</td>
        </tr>
        <tr>
            <td>5033</td>
            <td>SOUTHERN</td>
        </tr>
        <tr>
            <td>2262</td>
            <td>TARAVAL</td>
        </tr>
        <tr>
            <td>1229</td>
            <td>TENDERLOIN</td>
        </tr>
    </tbody>
    </table>
</div>

This table shows that the district with the most occurrences of Forgery/Counterfeiting is Southern, which is where the financial area is located.

 <header>
        <h1>Heat Map displaying Forgery/Counterfeiting in San Francisco</h1>
</header>

We make a map of San Francisco to show where exactly the forgery/counterfeiting takes place. You can increase the frames per second to 10, to see a more distinct evolution in occurrences over the years. 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/heatmap.html"
           width="1100"
           height="600"
           >
</div>

From this heatmap we clearly see a decrease in occurences of forgery/counterfeiting over time. We see that the southern district has the highest denisty over time. From this map we can also see that the occurences of forgery/counterfeiting in the southern district are in fact happening in the financial area which can be seen on this map: (https://commons.wikimedia.org/wiki/File:SF_Financial_District_map.png) ACAB

 <header>
        <h1>Interactive hourly plot</h1>
</header>

Now, let's look at the total counts for this crime type, for each hour, for each year. Select a couple of years to get a visual comparison between two years. For example, if you select 2003 and 2017 you can see a clear decrease in total counts. Important to notice that the extremely high count at hour 0 might be due to an error in the way that the data is registered by the police. 

<div style="display: flex; justify-content: center;">
    <embed 
           type="text/html" 
           src="/assets/html/forgery_rt.html"
           width="1100"
           height="600"
           >
</div>
