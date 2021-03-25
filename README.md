# Tropical Storm Classification Modeling Project

**Author**: [Christie Sarver](mailto:christie.sarver@gmail.com)

## Overview

The goal of this project is to build a model that takes in tropical cyclone tracking data and classifies accurately whether readings indicate that a storm is a severe Tropical Storm or a less disruptive disturbance.

### The Data

The data for this project is from the National Oceanic and Atmospheric Administration's International Best Track Archive for Climate Stewardship (IBTrACS) project. The goal of this project is make available tropical cyclone best track data to aid understanding of the distribution, frequency, and intensity of tropical cyclones worldwide.

Because the idea is to have a global data source, this data is pulled from many separate agenices worldwide, and therefore has many columns that are duplicative, inconsistent, or difficult to interpret. When doing this analysis, reference was made to the data documentation saved in this repository. 

[Source](https://www.ncdc.noaa.gov/ibtracs/index.php)

### Business Problem

The resulting model will be used by meterologists to understand whether an incoming storm is a major threat to a certain area, and therefore inform news agenices, local governments, and the public to prepare accordingly.

## Methodology

Due to the complexity of this data, a large part of this project was cleaning and exploring the data with reference to its documentation, located in this repository. Before modeling, relevant features were selected including:
* Location-based indicators: latitude, longitude, basin, distance to land
* Weather conditions: wind speed, storm speed, storm direction
* Times of occurence: year, week of year

The modeling section of this project runs and evaluates four different classification modeling types, with attention paid to how they parform against the class imbalance and the nonlinear features. 

![y_dist.png](./Images/y_dist.png)



## Results

Based on the model evaluations which are detailed in the notebook, thie final model chosen to move forward with is 

### Business Results and Recommendation

The final model analysis describes the following. 

Features that drive value in homes for our target buyer are:
* Size of the home interior
* Number of bathrooms (more so than bedrooms)
* High construction quality and materials

The value is significantly decreased where:
 * Construction quality is average or low
* House is further away from the city center

Based on this, recommendations for the housing developers are

* Focus on maximizing the living area of the house over the yard size, or adding a basement
* Use high quality construction methods 
* Build multi-floor homes and include ample bathrooms to reflect what buyers are looking for

### Technical Recommendation/Future Work

If there is further work on this project, I would recommend continuing to engineer features of the model in order to improve the R2 score and decrease error. Although I didn't detect any interactions, I would recommend looking more into how the features interact and relate to each other.
To make the model more generalizable, it would also be interesting to include data from multiple markets to see what trends are local vs specific to this market and potentially build multiple models to show the differences.

## Conclusions

While the data cleaning and transformations I made to this data followed best practices to fit it to a linear regression model, it didn't end up as accurate as I would have hoped. However, I was able to inform my business question by defining features of a home that would be important to a certain segment of buyers and eliminating many that do not prove to affect price.

## For More Information

See the full analysis in the [Jupyter Notebook](./Housing%20Data%20Model%20&%20Analysis.ipynb) or review this [presentation](./Housing%20Data%20Analysis%20Presentation.pdf).

## Repository Structure

```
├── Archive
├── Images
├── data
├── Housing Data Model & Analysis.ipynb
├── Housing Data Analysis Presentation.pdf
├── README.md

```
Thank you!
