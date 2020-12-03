-   [Introduction](#introduction)
-   [Data Organization](#data-organization)
-   [Exploratory Data Analysis](#exploratory-data-analysis)
-   [Run Notebook in Google Colab](#run-notebook-in-google-colab)
-   [Inquiries](#inquiries)
-   [Data Sources](#licensing)
-   [Acknowledgments](#references)

## Introduction
Motor vehicle accidents is a leading cause of death and injury in the United States. The use of motor vehicles is steadily increasing in the United States, with the number of vehicle miles traveled increasing each year. As more and more Americans place their lives and wellbeing in the hands of traffic and motor vehicles, ensuring their safety becomes an issue of the utmost importance. In 2015 over 2.5 million individuals were treated in emergency departments for injuries resulting from motor vehicle crashes (CDC, 2020). In 2019 alone, the National Highway Traffic Safety Administration reported over 36,096 fatalities in motor vehicle accidents (NHTSA, 2020). In addition to posing a danger to the safety of the people, motor vehicle accidents are currently a financial drain on the United States government and economy. The CDC estimates that for crashes that occurred in 2017, the cost of medical care and productivity losses associated with occupant injuries and deaths from motor vehicle traffic crashes exceeded $75 billion (CDC, 2020). Furthermore, traffic safety has been the target of a significant amount of spending by the government and other organizations.

With this in mind, we have decided to analyze data related to accidents in the United States with the goal of uncovering potential patterns in the occurrences of accidents. The specific questions we are looking to investigate are: **What conditions may make the risk of accidents higher?** and **What conditions impact the severity of accidents that occur?**

This analysis has the potential to provide valuable insight for people and organizations who are working to decrease the risk of accidents in the United States. An understanding of factors that increase the risk and severity of motor vehicle accidents would allow these organizations to carry out targeted efforts to ameliorate those conditions. Such efforts not only have the potential to save lives, but also save money and allow for optimal use of funds.

## Data Organization
In order to obtain insight on our question of causes of motor vehicle accidents in the United States, we used two main datasets. The first dataset, [US-Accidents](https://www.kaggle.com/sobhanmoosavi/us-accidents), provides about 3.5 million instances of traffic accidents that have taken place across the contiguous United States between February 2016 and June 2020. The second dataset, [US Census Demographic Data](https://www.kaggle.com/muonneutrino/us-census-demographic-data), contains information regarding the population of each state and county in the United States in 2015 and 2017. For the purposes of this analysis, we use the county data collected in 2017 as it is the more recent of the two. Although the accidents we are looking at happened over the span of five years (2016-2020), we do think that the 2017 population data is a decent representation for all of our analysis since we think that the population would not have changed by a significant amount. The latter dataset will be used to standardize the analysis of the occurrence of accidents across different sized states.

After filtering the data by removing the irrelevant attributes to our analysis, we ended up with the following attributes:

### US-Accidents Data:
<div class="datatable-begin"></div>
| Attribute | Data Type | Description | Nullable |
| --- | --- | --- | --- |
| Severity | Ordinal | Shows severity of the accident on a scale of 1-4 (1 indicates the least impact on traffic and 4 indicates a significant impact on traffic | No |
| Start_Lat | Categorical | Shows latitude in GPS coordinate of the start point | No |
| Start_Lng | Categorical | Shows longitude in GPS coordinate of the start point | No |
| Distance(mi) | Ratio | The length of the road extent affected by the accident | No |
| County | Categorical | Shows the county in address field | Yes |
| State | Categorical | Shows the state in address field | Yes |
| Temperature(F) | Categorical | Shows the time-stamp of weather observation record in local time | Yes |
| Humidity(%) | Categorical | Shows the humidity in percentage | Yes |
| Pressure(in) | Categorical | Shows air pressure in inches | Yes |
| Visibility(mi) | Categorical | Shows visibility in miles  | Yes |
| Wind_Speed| Categorical | Shows wind speed in miles per hour | Yes |
| Precipitation(in) | Categorical | Shows precipitation amount in inches | Yes |
| Amenity | Categorical | A POI annotation which indicates presence of amenity in a nearby location | No |
| Bump | Categorical | A POI annotation which indicates presence of speed bump or hump in a nearby location | No |
| Crossing | Categorical | A POI annotation which indicates presence of crossing  in a nearby location | No |
| Give_Way | Categorical | A POI annotation which indicates presence of giveway sign in a nearby location | No |
| Categorical | A POI annotation which indicates presence of junction in a nearby location | No |
| No_Exit | Categorical | A POI annotation which indicates presence of no exit sign in a nearby location | No |
| Railway | Categorical | A POI annotation which indicates presence of railway in a nearby location | No |
| Roundabout | Categorical | A POI annotation which indicates presence of roundabout in a nearby location | No |
| Station | Categorical | A POI annotation which indicates presence of station (bus, train, etc.) in a nearby location | No |
| Stop | Categorical | A POI annotation which indicates presence of stop sign in a nearby location | No |
| Traffic_Calming | Categorical | A POI annotation which indicates presence of traffic calming means in a nearby location | No |
| Traffic_Signal | Categorical | A POI annotation which indicates presence of traffic signal in a nearby location | No |
| Turning_Loop | Categorical | A POI annotation which indicates presence of turning loop in a nearby location | No |
| Sunrise_Sunset | Categorical | Shows the period of day (i.e. day or night) based on sunrise/sunset | Yes |
<div class="datatable-end"></div>

### US Census Demographic Data:
<div class="datatable-begin"></div>
| Attribute | Data Type | Description | Nullable
| --- | --- | --- | ---
| State | Categorical | Name of one of the 52 states of America, or DC or Puerto Rico | No |
| County | Categorical | Name of the county or county equivalent | No |
| TotalPopulation | Ratio | Total population of the county | No |
| Drive | Ratio | Percentage of the county’s population commuting alone in a car, van, or truck | No |
| Transit | Ratio | Percentage of the county’s population commuting on public transport | No |
| MeanCommute | Ratio | Mean commute time in minutes | No |
| Poverty | Ratio | Percentage of the county’s population under the level of poverty | No |
<div class="datatable-end"></div>

Furthermore, we added the following attributes that we are using later in our analysis:
| Attribute | Data Type | Description | Nullable
| --- | --- | --- | ---
| Duration | Ratio | The time duration of the accident in minutes which is calculated as the difference between the start time and end time | No |
| Start_Hour | Ratio | The hour when the accident started | No |
| Day | Categorical | The day of the week on which the accident took place | No |

## Exploratory Data Analysis

## Run Notebook in Google Colab
Click the link below to run [our notebook](https://github.com/pard187/pard187.github.io/blob/master/Final_Project_Gormley_Giffin_Johnston_Saleh.ipynb) directly in Google Collab. No coding is needed to run this notebook. However, since the datasets we are using are too big, it was not convienient to download and import them to github directly. All you need to do is use your own API key by downloading your Kaggle JSON file (only a few kilobytes) and uploading it when prompted (in the 3rd code cell).

<table align="left">
  <td>
    <a target="_blank" href="https://colab.research.google.com/github/pard187/pard187.github.io/blob/master/Final_Project_Gormley_Giffin_Johnston_Saleh.ipynb"><img src="https://www.tensorflow.org/images/colab_logo_32px.png" />Run in Google Colab</a>
  </td>
</table>
<br> <br> <br>

## Inquiries
For inquiries about this project, please contact Kaelyn Gormey at gormleyk@lafayette.edu, James Giffin at giffinj@lafayette.edu, Kate Johnston at johnstkr@lafayette.edu, or Marwa Saleh at salehm@lafayette.edu.

## Data Sources
- [US-Accidents Dataset](https://www.kaggle.com/sobhanmoosavi/us-accidents)
- [US Census Demographic Data](https://www.kaggle.com/muonneutrino/us-census-demographic-data)

## Acknowledgments
- Centers for Disease Control and Prevention (CDC), [*Cost Data and Prevention Policies*](https://www.cdc.gov/transportationsafety/costs/index.html?CDC_AA_refVal=https%3A%2F%2Fwww.cdc.gov%2Fmotorvehiclesafety%2Fcosts%2Findex.html), November 2020

- Moosavi, S. [*US Accidents (3.5 million records)*](https://www.kaggle.com/sobhanmoosavi/us-accidents), Version 6. 2020 

- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. [*A Countrywide Traffic Accident Dataset.*](https://arxiv.org/abs/1906.05409), 2019.

- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. [*Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights.*](https://arxiv.org/abs/1909.09638), 2019.

- Muon, Neutrino. [*US Census Dempgraphic Data*](https://www.kaggle.com/muonneutrino/us-census-demographic-data), Version 3. 2018

- National Highway Traffic Safety Administration (NHTSA), [*2019 Fatality Data Show Continued Annual Decline in Traffic Deaths*](https://www.nhtsa.gov/press-releases/2019-fatality-data-traffic-deaths-2020-q2-projections), October 2020

```
- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pard187/pard187.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
