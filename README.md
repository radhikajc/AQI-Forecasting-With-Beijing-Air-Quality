#AQI-Forecasting-With-Beijing-Air-Quality

###I. Introduction:
Development in industrialization and advancement of technology has led to an increase in pollutant levels in the air. In China, this has led to an increase in extreme weather conditions such as a higher recorded increase in temperature, haze, smog and adverse effects on health conditions to the residents of these areas.
The research on the concentration of these pollutants will provide the information required for the improvement of significant health, environmental conditions, and benefits to the economy while reducing costs on solutions to reduce air pollution.

<img width="591" alt="image" src="https://user-images.githubusercontent.com/103969912/192121759-caa546d9-fdaa-455e-92fb-31cf5cb4f2b2.png">

The Air Quality Index is a metric that quantitatively describes the number of pollutants suspended in the air to briefly describe the air quality in an area. The air's concentration of pollutants such as PM2.5, PM10, CO, O3, SO2 and NO2 indicates the overall air quality. However, other meteorological conditions also play a pivotal role in the quality of air.

####I.I. Problem Definition:
Through this project, we aim to research and incorporate complex nonlinear relationships between the concentration of air pollutants and meteorological variables across a given period. Implement and build a prediction system based on individual pollutant concentration levels that can predict air quality. Doing so will make the information on the air quality index more flexible and useful. Systems that can generate warnings based on air quality are required and important for a change as they may play an important role in health alerts when air pollution levels may exceed specified levels. By the end of this classroom project, we aim to establish a relationship between the concentration of pollutants and its correlation with AQI (Air Quality Index).

<img width="703" alt="image" src="https://user-images.githubusercontent.com/103969912/192121823-6d9dc0d1-78d8-4c92-a049-ba44c0cd5b50.png">


###II. Data Description:
The dataset was procured from the very versatile website for the Data Science dataset, UCI ML. The dataset records hourly pollutant concentrations from twelve different controlled air quality monitoring centres across China.

####II.I. Data Features:
The data set selected by us comprises of eighteen dimensions and four lakh instances across the timeline of March 1st, 2013, to February 28th, 2017. Below we listed the types of features to gauge a better understanding of our data:

<img width="481" alt="image" src="https://user-images.githubusercontent.com/103969912/192121938-baa3ba9f-85e9-49c7-82e7-0ea56f28c713.png">

####II.II. Data Cleaning and Preprocessing:
To prepare the data for exploration and model fitting, we first combined the data files that were separated by record for each unique station. After combining these files we performed various exploratory data analyses to study and understand the recorded data and the following were the changes made to attain our target:
● Columns ‘year’, ‘month’, ‘day’ and ‘hour’ were combined to create a Date – Time column such that we can distinguish the records per each day per time.
● There were no duplicate records of Date – Time in the dataset, hence no rows were dropped.

####II.III. Feature Engineering
The recorded data for these pollutants were converted to their standard unit from the recorded unit. The above calculations were achieved by the formulae:

<img width="489" alt="image" src="https://user-images.githubusercontent.com/103969912/192121952-f7d5c228-77a0-4f8c-8de9-a7f9cec079a0.png">

● All Null values within the data were replaced by their median for each day recorded by each station. While checking the data we noted that there exist days with a whole 24-hour period where no data was recorded. We replaced these null values with 0.
● Further to obtain the AQI Index of individual pollutants, a rolling window average for each pollutant must be obtained. This data is then segregated into various classifications of AQI and the max value is recorded as the quality index for the given day. The category of AQI is defined as per the standardized government information.
● AQI is calculated using the formula given below:

<img width="409" alt="image" src="https://user-images.githubusercontent.com/103969912/192121968-f5ab2dde-e17d-4afb-a2c4-8b2dbd090736.png">


<img width="645" alt="image" src="https://user-images.githubusercontent.com/103969912/192121970-451d116f-fbeb-46c0-bcba-83a739fb567c.png">

####II.IV. Data Exploration:
*Pie Chart - Percentage of Days Within Each Air Quality Classification:*

<img width="433" alt="image" src="https://user-images.githubusercontent.com/103969912/192122014-c907e775-d3d2-4a49-ae8d-06744b8780d2.png">

To prepare the data for exploration and model fitting, we first combined the data files that were separated by record for each unique station. After combining these files we performed various exploratory data analyses to study and understand the recorded data and the following were the changes made to attain our target:
