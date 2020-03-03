---
layout: page
title: "Weather station! Winter project"
date: 2020-01-10 15:00:00 -0000
categories: CATEGORY-1 CATEGORY-2
---

Weather station! Winter project
I got a weather station for Christmas, and as a little mini project i wanted to see if i could get the values on my PC. And as it turned out i could!


### The hardware
My wife bought me a Bresser 5 in 1 weather station for Christmas which ive fitted in my back garden. Collects values such as temperature, windspeed, wind direction etc. You then view the values in a little receiver display. After some googling i can see that it is possible to pick the signal up. The weather station broadcasts the signals a radio signal at 868Mhz. You can buy USB radio receivers that can pick up this signal. I bought out of these: https://www.amazon.co.uk/gp/product/B01GDN1T4S/ref=ppx_yo_dt_b_asin_title_o09_s00?ie=UTF8&psc=1

### The software
Once i knew it was possible to get the values, next steps were how to actually get them, store them and view them.
## Collecting values
Looking around i found this repo https://github.com/merbanan/rtl_433. This is exactly what i wanted an executably that someone has already written which can collect the actual values and output them. I setup a Windows Scheduled Task to run it once every 5 minute. You can specify various different output formats and with a bit of luck it can already output to influxdb. Here are my exact parameters:

## Storing values
I already have an influxdb server which i use to store various stats for my homelab, and already have grafana to view that data. 
