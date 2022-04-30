# Final Project: Traffic, Weather, and Incident Data
## Zakariyya Al-Quran, Rithik Reddy, & Mohamed Sufiyaan

#### Project Description

We analyzed and visualized incidents in the Greater Nashville Area using AWS Athena to merge the data stored on S3.

#
#### Contents

This repository contains all the source code used to query the data and generate visuals.

#
#### Data

The data sets used in this project as described below:
 - Traffic
 - Incident
 - Weather
 - Roads

#
#### Milestones Delivered 
**1. Merge all Relevant Datasets together**
> - Upload all Datasets onto an **S3 Bucket**: [S3 Steps](google.com)
> - Set up an **EMR Cluster** for **pySpark** pre-processing: [EMR Steps](google.com)
>   - Transform Traffic Data and Weather Data for 6hr Windows: [Jupyter Notebook #1](google.com)
> - Merge Datasets: [Merge Queries](google.com)
>   - Merge Incidents with Traffic (on Incident ID, Window) -> name: *Traf_Inc*
>   - Merge Weather with Traf_Inc (on Incident ID, Window) -> name: *Intermediate*
>   - Merge Roads with Intermediate (on XDSegID) -> name: *Merge_Showdown*
> - Clean up Duplicated Columns after Merging: [Colab Notebook #1](google.com)

**2. Loading Tables onto Database** 
> - Upload Tables onto **Athena** via S3: [Athena Steps](google.com)
> - Directly Use Athena Console for **SQL** Querying

**3. Querying the Data for Filtered Information**
> - Generate Historical Trends of Incidents across 20 major Nashville Roads: [Query Group #1](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Query%20Group%20%231_%20Historical%20Trends%20Across%20Top%2020%20Roadways.pdf)
>   - Results stored in [Historical T20 Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Historical%20T20%20Query%20Results) folder
> - Generate Correlation of Incidents with Relevant Weather Patterns: [Query Group #2](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Query%20Group%20%232_%20Correlation%20of%20Traffic%20Incidents%20%26%20Weather%20Patterns.pdf)
>   - Results stored in [Weather Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Weather%20Query%20Results) folder
> - Generate Grid-Partitioned Incident Querying for Greater Nashville Area: [Query Group #3](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/blob/master/Query%20Group%20%233_%20Grid-Partitioned%20Incidents.pdf)
>   - Results stored in [Geo-Grid Query Results](https://github.com/vu-topics-in-big-data-2022/Project-Incident-Team2/tree/master/Geo-Grid%20Query%20Results) folder

**4. Processing the Data Plotting and Visualizations**

**5. Processing the Data through Machine Learning Modeling**

#
#### Presentation

A link to the video presentation can be found [here](google.com)
