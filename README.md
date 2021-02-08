### learn-traffic-crashes
## Learn Python Data Analytics by Example - Chicago Traffic Crashes

[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)

### Introduction

While working towards my Master's in Business Analytics, I found that learning by example is the best way for me to learn Python data analytics.  Being given a dataset and a set of coding tasks is much more beneficial than reading a textbook or listening to a professor.  

I want to share this method of learning with others who will also benefit.  All you need is a Python development environment (I recommend [Jupyter Notebook](https://jupyter.org/)) and a willingness to learn and have fun.

Included in this article is a list of data analytics tasks, followed by a detailed walkthrough of how to complete the tasks.  Please try to complete the tasks yourself before reading through the walkthrough - you will get more out of it that way.  Do keep in mind that there are many many ways to solve coding problems, so your code likely will not match mine word for word and that is okay.

### Project Description

For this project we will use a dataset with a combined 1.5 million records, which represent traffic crashes reported in Chicago from 2013 to 2021 and the vehicles involved in them.  The dataset was created in February 2021 and contains data sourced from the [City of Chicago](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3).

You will need to install the [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/), [seaborn](https://seaborn.pydata.org/index.html) and [Folium](https://python-visualization.github.io/folium/) libraries, if you do not already have them.


### Data Analytics Tasks

Please perform the following tasks in Python using the *crashes.csv* and *crashes_vehicles.csv* datasets available from this [drive](https://1drv.ms/u/s!AoQYKisAOe1libRT6GTcLP6n_B75hA?e=yTTaEr).  Also refer to this [GitHub repo](https://github.com/nickdcox/learn-traffic-crashes).
1. Read the CSV files containing the Chicago traffic crash data.  Identify the column common to both files and merge them together on that column.  Then display the total number of reported crashes.
2. Change the ‘CRASH_DATE’ column to a date format.  Drop observations that did not occur in 2017, 2018 or 2019 (other years have incomplete data).
3. Display a plot showing the number of crashes that occur for each hour of the day.
4. Name the make of vehicle that was involved in the most daylight crashes in August 2018.  Remember that a crash can involve multiple vehicles.
5. Determine which weather condition was most prevalent for each type of crash.
6. Plot the primary contributing cause of reported crashes, from highest to lowest.
7. Display the 10 state license plates involved in the most crashes.  Remember that a crash can involve multiple vehicles.
8. Display the proportion of crashes in each month of 2019 where alcohol was determined to be the primary contributing cause.
9. Determine whether snowmobiles or recreational off-highway vehicles were involved in more crashes.
10. Display a cluster map showing the locations of crashes involving a hit and run.


### Data Dictionary

**crashes.csv:** Each row in the dataset represents a traffic crash reported in Chicago.

| Column Name | Description |
| :--- | :----------- |
| CRASH_RECORD_ID | A unique identifier for a crash. |
| CRASH_DATE | The date that the crash occured. |
| WEATHER_CONDITION | The weather at the time the crash occurred. |
| LIGHTING_CONDITION | The lighting condition at the time the crash occurred. |
| FIRST_CRASH_TYPE | The type of crash. |
| HIT_AND_RUN_I | An indicator (Y or N) as to whether the crash was a hit and run. |
| PRIM_CONTRIBUTORY_CAUSE | The primary cause of the crash. |
| LATITUDE / LONGITUDE | The coordinates where the crash occured. |

**crashes_vehicles.csv:** Each row in the dataset represents a vehicle involved in a crash reported in Chicago.

| Column Name | Description |
| :--- | :----------- |
| CRASH_RECORD_ID | A unique identifier for a crash. |
| CRASH_DATE | The date that the crash occurred. |
| VEHICLE_ID | A unique identifier for each vehicle involved in a crash, in lieu of not having the license plate data. |
| MAKE | The make of each vehicle involved in the crash. |
| LIC_PLATE_STATE | The state where each vehicle involved in a crash is registered. |
| VEHICLE_TYPE | The type of each vehicle involved in the crash. |
