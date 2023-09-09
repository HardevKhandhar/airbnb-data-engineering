# Airbnb Data Engineering

> _This project was completed as part of my graduate coursework at Simon Fraser University (SFU) during the Fall 2022 term. It does not represent the official views or endorsements of Airbnb or any other organization. The project's primary goal is to demonstrate data engineering concepts and practices. It may not reflect real-world practices and any data used is for illustrative purposes only._

## Overview: Airbnb

Airbnb is an online marketplace that helps people in finding a short-term homestay. The host or a person renting out their home for a short duration put up various details of the homestay such as pictures, different amenities, location and the nightly charge. The visitors can use these details to select the ideal homestay. The choice of selection is also helped by the ratings and reviews each listing receives. Airbnb is currently active in 191 countries and over 100,000 cities.


## Problem Definition

One of the main issues that international students face on their arrival in Canada is finding a temporary stay for the initial few days. After a long journey, students desire comfort and they are most motivated to book Airbnb accommodations because of their low cost, convenient location and household amenities. However, selecting an Airbnb can be a challenge if you don’t have prior knowledge of the place. Through this project, we intend to work on comprehensive data engineering pipeline with students as a target group and analyse the listings in Toronto and Vancouver to help the students select the area and the type of Airbnb they need to choose.


## Prerequisites

- Python3
- Apache Spark
- AWS S3


## Project Structure

```bash
.
├── executeProject.sh
├── __init__.py
├── README.md
├── requirements.txt
├── RUNNING.md
└── src
    ├── analysis
    │   ├── amenitiesUtility.py
    │   ├── analyzeAmenities.py
    │   ├── calculateDistance.py
    │   ├── distanceUtility.py
    │   ├── __init__.py
    │   └── __pycache__
    │       ├── amenitiesUtility.cpython-310.pyc
    │       └── distanceUtility.cpython-310.pyc
    ├── cleaning
    │   ├── cleaningUtility.py
    │   ├── dataCleaning.py
    │   ├── extractS3Data.py
    │   ├── __init__.py
    │   └── __pycache__
    │       └── cleaningUtility.cpython-310.pyc
    ├── __init__.py
    ├── notebooks
    │   ├── __init__.py
    │   ├── toronto_exploratory_data_analysis.ipynb
    │   └── vancouver_exploratory_data_analysis.ipynb
    ├── preprocessing
    │   ├── extractData.py
    │   ├── __init__.py
    │   └── loadData.py
    └── utils
        ├── config.ini
        ├── constants.py
        ├── __init__.py
        ├── __pycache__
        │   ├── constants.cpython-310.pyc
        │   └── __init__.cpython-310.pyc
        └── restructure.py
```

- `/analysis`: Source code for different analysis performed in the project
- `/cleaning`: Source code for data cleaning applied to Raw Data
- `/notebooks`: Jupyter notebooks containing the preliminary exploratory data analysis
- `/preprocessing`: Source code for the preprocessing of the datasets
- `/utils`: Different utility files and helper functions used in the project


## Data Source

[Inside Airbnb](http://insideairbnb.com/get-the-data)


## Approach to the solution

We chose two major student hubs in Canada for the project: Vancouver and Toronto. The data was then downloaded from the Internet using Python scripts and the raw, unfiltered data was uploaded to Amazon S3 for further processing and analysis. The dataset was examined (exploratory data analysis) to determine its potential and the amount of cleaning required. The data was cleaned with the help of these observations. During cleaning, unnecessary rows were removed, null values were removed and minor issues were addressed. The cleaned dataset was then used for analysis. The analysis was based on two factors: the distance from the city's major universities and the amenities available in each listing. Pricing is critical, especially in large cities where there is a lot of competition and even small price differences can make the difference between optimum occupancy and high earnings or being priced out of the market. The datasets obtained after the analysis were then visualized on Tableau.


## Results

- In terms of outcomes, the project helped us understand the preferences of students based on budget and locations near their educational institute. 

- By working on this project, we learnt that the scraped raw data is almost always dirty and required a lot of cleaning. 

- A look at the raw data and some preliminary exploratory data analysis helped us understand the potential of raw data in terms of feature selection as well as which data needs cleaning and null value handling.

- The analysis helped us understand the demographics of a region and how the prices of every listing are affected based on the location.

- Amenity analysis helped us figure out some of the essential amenities which are always preferred over other generally available amenities. 

- The location-based analysis portrayed a picture of how dense the listings were near some of the educational institutes. 

- In terms of software development, we had a great opportunity to learn about Agile methodologies and the software development lifecycle in general. We learnt about initial architecture design and code structures to be followed. 

- As opposed to the waterfall model, we could easily adjust change requirements in this project. Overall, it was a good learning opportunity.


## Visualizations

- One of the many reasons we chose Tableau to visualize our data was that Tableau dashboards can be viewed and operated on several devices such as your laptop, mobile, or even a tablet! You aren’t required to perform any additional steps in order to make your dashboards mobile-friendly. Tableau automatically understands the device that you’re viewing the report on and makes adjustments accordingly.

- Compared to other BI tools, Tableau lets you create rich visualizations in just a few seconds! It lets you perform complex tasks with simple drag-and-drop functionalities, hence answering your questions in no time!

**Dashboard Links**

- [Vancouver Data Analysis Dashboard](https://public.tableau.com/app/profile/priyanka.jain4165/viz/vancouveranalysis/vancouver_main)

- [Toronto Data Analysis Dashboard](https://public.tableau.com/app/profile/priyanka.jain4165/viz/torontoanalysis/toronto_main)


## Project Execution

Please refer to the instructions given in this [FILE](RUNNING.md)


## Summary

This project allowed us to explore the vastness of big data and solve a real-world problem while learning and applying big data applications.

Large data sets uncover hidden patterns, unknown correlations, market trends, customer preferences and other useful business information. These analytical findings are helping organizations in more effective marketing, new revenue opportunities and better customer service.

The team was also able to learn a lot about the software development life cycle and gain valuable experience dealing with interesting challenges as a result of this.

---

Thank you!
