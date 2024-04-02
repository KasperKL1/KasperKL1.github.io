---
layout: post
title:  "Social Data Analysis and Visualization: Assignment 2"
date:   2024-03-31 14:40:25 +0200
categories: jekyll update
---
Firstly, we want to look at the different crime categories to determine which category has the most characteristic evolution over the years from 2003 to 2017.

![Placeholder Screenshot](/assets/images/newplot.png)


We want to look at forgery/counterfeiting. Because this category seems to be decreasing rapidly in recent years. This could be due to the fact that documents are being digitalized more and more and therefore, these are not as easily forged as they were in the past.

        |   Count  |  Category  |
        |----------|------------|
        |   1669   |  BAYVIEW   |
        |   2541   |  CENTRAL   |
        |   2094   | INGLESIDE  |
        |   2764   |  MISSION   |
        |   2808   | NORTHERN   |
        |   1045   |    PARK    |
        |   1355   |  RICHMOND  |
        |   5033   |  SOUTHERN  |
        |   2262   |  TARAVAL   |
        |   1229   | TENDERLOIN |


We make a map of SF to show where the forgery/counterfeiting takes place.

<embed 
       type="text/html" 
       src="/assets/html/heatmap.html"
       width="1100"
       height="600"
       >

From this heatmap we clearly see a decrease in occurences of forgery/counterfeiting over time. We see that the southern district has the highest denisty over time. From this map we can also see that the occurences of forgery/counterfeiting in the southern district are in fact happening in the financial area which can be seen on this map: (https://commons.wikimedia.org/wiki/File:SF_Financial_District_map.png)

![Heatmap of San Fransisco Financial Districs](/assets/images/SF_Financial_District_map.png)


<embed 
       type="text/html" 
       src="/assets/html/forgery_rt.html"
       width="1100"
       height="600"
       >

From this plot we clearly see the decrease in occurrences over the years. Furthermore, we see that the most occurrences take place at midnight. This might be due to bad time notation.