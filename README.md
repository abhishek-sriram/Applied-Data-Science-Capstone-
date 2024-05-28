
# SpaceX Falcon9 Landing Prediction

## Introduction

SpaceX has revolutionized the space industry with its cost-effective Falcon 9 rocket launches. The primary reason for their cost efficiency is the reusability of the rocket's first stage. This project aimed to create a machine learning pipeline to predict the success of the first stage landing, which is crucial for reducing launch costs. By determining the factors influencing the landing success, we can help other companies compete with SpaceX.

## Methodology

### Data collection

#### Using SpaceX API: 
* Retrieved data from the SpaceX API using get requests.
* The response was decoded into JSON format and converted to a pandas DataFrame for analysis.

###### Data Collection with API

![Data Collection with API](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_1.png)

#### Web Scraping from Wikipedia: 

- BeautifulSoup was used to scrape Falcon 9 launch records from Wikipedia.
- The HTML table containing the launch records was parsed and converted into a pandas DataFrame.

###### Data Collection with Web Scraping

![Data Collection with Web Scraping](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_2.png)

#### Data Wrangling:

- Cleaned the data by checking for and filling in missing values.

- Applied one-hot encoding to categorical features.

##  Exploratory Data Analysis (EDA)

### Visualization: 

- Used various plots to visualize the relationship between different features like flight number, launch site, payload mass, and success rate.

- Plotted success rate trends over the years and success rates of different orbit types.

###### Payload vs Launch Site

![Payload vs. Launch Site](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_4.png)

###### Flight Number vs Launch Site                                                      

![Flight Number vs. Launch Site](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_3.png)

###### Flight Number vs Orbit Type

![Flight Number vs. Orbit Type](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_5.png)

###### Payload vs Orbit Type 

![Payload vs. Orbit Type](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_6.png)

### SQL Queries: 

- Loaded the dataset into a database.

- Executed SQL queries to extract insights, such as unique launch sites, total payload mass by NASA missions, and average payload mass by booster versions.

###### All Launch Site Names

![All Launch Site Names](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_7.png)

###### Total Payload Mass 

![Total Payload Mass](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_8.png)

###### Rank Landing Outcomes Between 2010-06-04 and 2017-03-20

![Rank Landing Outcomes Between 2010-06-04 and 2017-03-20](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_9.png)

###### Successful Drone Ship Landing with Payload between 4000 and 6000

![Successful Drone Ship Landing with Payload between 4000 and 6000](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_10.png)

### Interactive Visual Analytics

- Created interactive maps with Folium to visualize the success and failure of launches at different sites.

- Built a dashboard with Plotly Dash to provide interactive visual analytics, including pie charts and scatter plots.

###### Ground Stations

![Ground stations](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_11.png)

###### Color-labeled launch records

![Color-labeled launch records](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_12.png)

###### Distance from the launch site to its proximities

![Distance from the launch site to its proximities](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_13.png)

###### Highest Launch site success ratio(Plotly)

![Highest Launch site success ratio(Plotly)](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_14.png)

### Predictive Analysis

- Split the data into training and testing sets.

- Built and tuned various classification models using GridSearchCV.

- Evaluated the models using accuracy as the metric.

- Improved the model with feature engineering and hyperparameter tuning to find the best performing classifier.

###### Confusion Matrix

![Confusion Matrix](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_15.png)

###### Scores and Accuracy of the Test Set

![Scores and Accuracy of the Test Set](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_16.png)

###### Scores and Accuracy of the Entire Data Set

![Scores and Accuracy of the Entire Data Set](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Project%20Screenshots/spacex_17.png)

### Results

#### Exploratory Data Analysis: 

- Found that higher flight numbers at a launch site correlate with higher success rates.

- Certain orbits like ES-L1, GEO, HEO, SSO, and VLEO have higher success rates.

- Success rate has been increasing since 2013.

#### Interactive Analytics: 

- Mapped all launch sites and their proximity to landmarks such as railways and highways.

- Visualized success rates of different launch sites with color-coded markers on a map.

#### Predictive Analysis: 

- Decision Tree Classifier emerged as the best model for predicting landing outcomes.

- Confusion matrix analysis showed high accuracy, though there were some false positives.

### Conclusion:

The project demonstrated that various factors like flight number, payload mass, and orbit type significantly influence the success of Falcon 9's first stage landing. The success rate of launches has been improving over the years, and certain orbits have higher success rates. The Decision Tree Classifier was the most effective model for predicting landing success. These insights can help other companies to strategize and compete with SpaceX.


## 🔗Links to Notebooks

1. ![Data Collection using SpaceX API](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Data%20Collection%20using%20SpaceX%20API/Data_Collection_using_SpaceX_API.ipynb)

2. ![Data Collection with Web Scraping](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Data%20Collection%20with%20Web%20Scraping/Webscraping.ipynb)

3. ![EDA with Data Visualization](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/EDA%20with%20Data%20Visualization/EDA_with_Data_Visualization.ipynb)

4. ![EDA with SQL](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/EDA%20with%20SQL/EDA_with_SQL.ipynb)

5. ![Interactive Map with Folium](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Interactive%20Map%20with%20Folium/Interactive%20Maps_using_folium.ipynb)

6. ![Machine Learning Prediction](https://github.com/abhishek-sriram/SpaceX-Falcon-9-Landing-Prediction/blob/main/Machine%20Learning%20Prediction/SpaceX_Machine_Learning_Prediction.ipynb)










