# Surfs Up
## Overview

### Tools
This project uses Pythons **SQLAlchemy** library to create SQL queries that can work for any flavor of SQL databases. In our case, we use **SQLite** to quickly and conveniently setup a database engine without requiring a server. SQLAlchemy’s methods include create_engine, automap_base(), and Session(), which we utilize within a **Jupyter Notebook** session to explain the structures, interactions, and types of data within a dataset. Finally, to display our analysis on a website in real time we will use **Flask**.

### Project
W. Avy, a potential investor in a Surf Shop in Hawaii, asks us to run weather analysis on a weather database of Hawaii. This database includes data collected from thirteen weather stations across Hawaii and spans several years. Using Python and its libraries this proves to be a simple task. After importing all relevant dependencies, we must create an engine through SQLAlchemy, and then create a base class for an automap schema. This base class is our foundation allows us to build existing databases onto a model and reflect the databases tables. After saving references to each table, we are ready to extract, filter, and display our analysis.

## Analysis
### June
How does the weather look like in June? After filtering the given database to retrieve weather data collected within the month of June, we use **pandas** describe() method to retrieve statistical information. The mean temperature in Hawaii in June is 74.9 degrees Fahrenheit, with a high of 85 degrees and a low of 64 degrees. The 25 percentile rests at 73 degrees, and the 75 percentile rests at 77 degrees.

![image](https://user-images.githubusercontent.com/68082808/94349293-25968e80-0011-11eb-9502-44be2bf086bd.png)

### December
It is also important to analyze the weather in December. This way we can have a better understanding of how the weather in Hawaii is year-round. After using a similar technique to filter the data in December, we have our statistical analysis. The mean temperature in Hawaii is 71.0 degrees Fahrenheit with a high of 83 degrees and a low of 56 degrees. The 25 percentile rests at 69 degrees and the 75 percentile rests at 74 degrees.

![image](https://user-images.githubusercontent.com/68082808/94349309-3e9f3f80-0011-11eb-91c3-b8ac7d031046.png)
### Notable Differences
The interquartile range of the weather in January is only 4 degrees. This indicates that the temperature in Hawaii stays relatively stable compared to the weather in December. The interquartile range for the weather in December is six degrees, an insignificant difference but perhaps one for investors to note. This is further revealed by the difference in standard deviations in temperature between the two months. December has a low of 56 degrees, however it is important to note that the 25 percentile rests at 69 degrees, indicating that it is uncommon for the temperature to reach a low of 56 degrees. The low temperature in June stays comparatively constant, where the low temperature is 64 degrees whereas the 25 percentile rests at 69 degrees. The max temperature in both months is above 80 degrees, encouraging surfing and beach going at both ends of the year.

## Summary and Further Findings
In the SurfsUp.ipynb file we explore temperature fluctuations between the months of June and December. But there is so much more one may consider when it comes to weather analysis. In the climate analysis.ipynb file we explore precipitation patterns between August 2016 and August 2017.

![image](https://user-images.githubusercontent.com/68082808/94349340-83c37180-0011-11eb-954d-6b72e525b8fa.png)

Hawaii may experience a few heavy rainstorms over the course of a single year, stastical data reveals that these heavy rainstorms are anomalies and do not account for the general weather on the islands of Hawaii. Over the course of the specified interval, Hawaii experienced an average rainfall of 0.17 inches of rain, where the 50 percentile rests at 0.02 inches and the 75 percentile rests at 0.13 inches. This is an indication that precipitation patterns are skewed to the right.

![image](https://user-images.githubusercontent.com/68082808/94349352-99389b80-0011-11eb-90ba-594ab0a45d8d.png)

The temperature in Hawaii is stable throughout the year, with unfriendly rainfalls occurring few and far between. Through this statistical analysis, an investor can be confident that the weather will not conflict with a growing surf shop.
