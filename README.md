# Final Project: US Car Accidents

## Data Organization
Attribute | Data Type | Description | Nullable
--- | --- | --- | ---
Traffic Attributes (12) 
ID | Categorical | A unique identifier of the accident record | No
Source | Categorical | Indicates source of the accident report (i.e. the API which reported the accident) | No
TMC | Numeric | A traffic accident may have a Traffic Message Channel (TMC) code which provides more detailed description of the event | Yes
Severity | Ordinal | Shows severity of the accident on a scale of 1-4 (1 indicates the least impact on traffic and 4 indicates a significant impact on traffic | No
Start_Time | Categorical | Shows start time of the accident in the local time zone | No
End_Time | Categorical | Shows end time of the accident in the local time zone | No
Start_Lat | Categorical | Shows latitude in GPS coordinate of the start point | No
Start_Lng | Categorical | Shows longitude in GPS coordinate of the start point | No
End_Lat | Categorical | Shows latitude in GPS coordinate of the end point | Yes
End_Lng | Categorical | Shows longitude in GPS coordinate of the end point | Yes
Distance(mi) | Ratio | The length of the road extent affected by the accident | No
Description | Categorical | Shows natural language description of the accident | No
Address Attributes (9)
Number | Categorical | Shows the street number in address field | Yes
Street | Categorical | Shows the street name in address field | Yes
Side | Categorical | Shows the relative side of the street (Right/Left) in address field | Yes
City | Categorical | Shows the city in address field | Yes
County | Categorical | Shows the county in address field | Yes
State | Categorical | Shows the state in address field | Yes
Zipcode | Categorical | Shows the zipcode in address field | Yes
Country | Categorical | Shows the country in address field | Yes
Timezone | Categorical | Shows timezone based on the location of the accident (eastern, central, etc.) | Yes
Weather Attributes (11)
Airport_Code | Categorical | Denotes an airport-based weather station which is the closest one to location of the accident | Yes
Weather_Timestamp | Categorical |  | Yes
Temperature(F) | Categorical | Shows the time-stamp of weather observation record in local time | Yes
Wind_Chill(F) | Categorical | Shows the wind chill in Fahrenheit | Yes
Humidity(%) | Categorical | Shows the humidity in percentage | Yes
Pressure(in) | Categorical | Shows air pressure in inches | Yes
Visibility(mi) | Categorical | Shows visibility in miles  | Yes
Wind_Direction | Categorical | Shows wind direction | Yes
Wind_Speed| Categorical | Shows wind speed in miles per hour | Yes
Precipitation(in) | Categorical | Shows precipitation amount in inches | Yes
Weather_Condition | Categorical | Shows the weather condition (rain, snow, thunderstorm, fog, etc.) | Yes
Point of Interest (POI) Attributes (13):
Amenity | Categorical | A POI annotation which indicates presence of amenity in a nearby location | No
Bump | Categorical | A POI annotation which indicates presence of speed bump or hump in a nearby location | No
Crossing | Categorical | A POI annotation which indicates presence of crossing  in a nearby location | No
Give_Way | Categorical | A POI annotation which indicates presence of giveway sign in a nearby location | No
Junction | Categorical | A POI annotation which indicates presence of junction in a nearby location | No
No_Exit | Categorical | A POI annotation which indicates presence of no exit sign in a nearby location | No
Railway | Categorical | A POI annotation which indicates presence of railway in a nearby location | No
Roundabout | Categorical | A POI annotation which indicates presence of roundabout in a nearby location | No
Station | Categorical | A POI annotation which indicates presence of station (bus, train, etc.) in a nearby location | No
Stop | Categorical | A POI annotation which indicates presence of stop sign in a nearby location | No
Traffic_Calming | Categorical | A POI annotation which indicates presence of traffic calming means in a nearby location | No
Traffic_Signal | Categorical | A POI annotation which indicates presence of traffic signal in a nearby location | No
Turning_Loop | Categorical | A POI annotation which indicates presence of turning loop in a nearby location | No
Period-of-day Attributes(4):
Sunrise_Sunset | Categorical | Shows the period of day (i.e. day or night) based on sunrise/sunset | Yes
Civil_Twilight | Categorical | Shows the period of day (i.e. day or night) based on civil twilight | Yes
Nautical_Twilight | Categorical | Shows the period of day (i.e. day or night) based on nautical twilight | Yes
Astronomical_Twilight | Categorical | Shows the period of day (i.e. day or night) based on astronomical twilight | Yes

## Data Statistics
## Inquiries
## References
Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. [*“A Countrywide Traffic Accident Dataset.”*](https://arxiv.org/abs/1906.05409), arXiv preprint       arXiv:1906.05409 (2019).

Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. [*“Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights.”*](https://arxiv.org/abs/1909.09638) In proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, ACM, 2019.


- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pard187/pard187.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
