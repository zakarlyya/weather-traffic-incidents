# Final Project: Traffic, Weather, and Incident Data
## Zakariyya Al-Quran, Rithik Reddy, & Mohamed Sufiyaan

#### Project Description

We analyzed and visualized incidents in the Greater Nashville Area using AWS Athena and Spark EMR to merge and query the data stored on S3.

#
#### Contents

This repository contains all the source codeused  and explanations on how to load, query and tranform the data and generate visuals.

#
#### Data

The data sets used in this project as described below:
 - **Traffic**: Gives traffic data such as speed and congestion across Davidson County.
 - **Incident**: Record of all of the incidents that occurred in Nashville from 2017-2021.
 - **Weather**: Weather in TN including precipitation, visibility, and temperature.
 - **Roads**: Data of all major roadways such as length of roadway, number of lanes, etc. 

#
#### Milestones Delivered 
**1. Merge all Relevant Datasets together**
> - Upload all Datasets onto an **S3 Bucket**
> - Set up an **EMR Cluster** for **pySpark** pre-processing
>   - Transform Traffic Data and Weather Data for 6hr Windows: [Jupyter Notebook #1](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Steps/pySpark_transform.ipynb)
> - Merge all the Datasets: [Merge Queries](Queries/Merge%20Queries.pdf)
> - Clean up Duplicated Columns after Merging: [Colab Notebook #1](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Steps/Table_Cleanup.ipynb)

**2. Loading Tables onto Database** 
> - Upload Tables onto **Athena** via S3
> - Directly Use Athena Console for **SQL** Querying

**3. Querying the Data for Filtered Information**
> - Generate Historical Trends of Incidents across 20 major Nashville Roads: [Query Group #1](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Queries/Query%20Group%20%231_%20Historical%20Trends%20Across%20Top%2020%20Roadways.pdf)
>   - Results stored in [Historical T20 Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Historical%20T20%20Query%20Results) folder
> - Generate Correlation of Incidents with Relevant Weather Patterns: [Query Group #2](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Queries/Query%20Group%20%232_%20Correlation%20of%20Traffic%20Incidents%20%26%20Weather%20Patterns.pdf)
>   - Results stored in [Weather Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Weather%20Query%20Results) folder
> - Generate Grid-Partitioned Incident Querying for Greater Nashville Area: [Query Group #3](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Queries/Query%20Group%20%233_%20Grid-Partitioned%20Incidents.pdf)
>   - Results stored in [Geo-Grid Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Geo-Grid%20Query%20Results) folder

**4. Processing the Data Plotting and Visualizations**

> - The results of the queries above (either on S3 or downloaded locally) were loaded into Pandas dataframes
> - Pandas was used for simple post processing if necessary
> - Plotly Go and Plotly Express were used to generate visualizations of the data such as maps and graphs 

A link to a pdf of all the plots can be found [here](plots.pdf)

**5. Processing the Data through Machine Learning Modeling**
> - Using the [Grid-Partitioned Data](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Geo-Grid%20Query%20Results), an EMR cluster was made and then this [Jupyter Notebook #2](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/ML_Regressions.ipynb) was used to run the machine learning model.
> - Results are stored [here](google.com)

#
#### Presentation

A link to the video presentation can be found [here](https://photos.google.com/share/AF1QipNQbDPu_xLAehm9o4nLx4sgq4_DCl6s69Vivo87aR02vg09DaV-Eakp2r_AqsNPVg/photo/AF1QipOICs7oRpicpem1vhTXG4D7RYDgQEqfGxG0dGT4?key=VGdaZ0xmSmxnQlc3TlZfUUpDX3Ewd1A5QllLVW9n)

If the link above does not work then the following link can be used: https://photos.app.goo.gl/dXpyeWkzEUSCinpD7

A link to the presentation slides can be found [here](slides.pdf)

