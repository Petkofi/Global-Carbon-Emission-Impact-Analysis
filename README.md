# Global-Carbon-Emission-Impact-Analysis
![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

![Carbon Emission Impact Analysis](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/carbon-emission-hero.png)

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Introduction  
This project leverages Python's data science stack to analyze the critical relationship between global CO₂ emissions and temperature anomalies. By applying statistical modeling and climate science methodologies, I quantify emission impacts, forecast warming scenarios, and deliver actionable insights for climate mitigation strategies, turning atmospheric data into actionable climate intelligence.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Background
Atmospheric CO₂ concentrations have surged 50% since pre-industrial levels, creating unprecedented demand for emission intelligence systems. This project builds the analytical infrastructure that converts NOAA and IPCC datasets sourced from Statso into precision decarbonization insights-the same tools powering carbon markets, ESG reporting, and the $7.5B climate analytics industry.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Dataset
The dataset used in this analysis is sourced from Statso and represents data compiled by NOAA and the IPCC. It includes two main components: one with annual temperature anomalies across multiple countries and decades, and another with monthly global CO₂ concentration levels. The temperature dataset records changes relative to a historical baseline, while the CO₂ dataset captures atmospheric carbon levels in parts per million. By combining these datasets, we can explore historical trends, identify anomalies, and model future climate scenarios, offering data-driven insights into the relationship between carbon emissions and global temperature changes.
![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Problem Statement
Climate change, fueled by increasing CO₂ concentrations, has become a pressing global concern, highlighting the urgent need for data-driven insights to inform effective policy-making.
This analysis seeks to understand the impact of carbon emissions on global temperatures by examining the relationship between key climate variables-including CO₂ concentrations, temperature anomalies, and their temporal dynamics-and how they collectively inform climate response strategies.

### Core Objectives:
#### Historical Trend Analysis
- Identify long-term correlations between CO₂ levels and temperature anomalies
- Understand the influence of industrialization and human activities on global warming

#### Anomaly Detection
- Detect significant deviations from climate trends
- Attribute anomalies to natural or anthropogenic events (e.g., volcanic eruptions, emission surges)

#### Scenario Simulation
- Model “what-if” scenarios to forecast temperature responses to varying CO₂ levels
- Quantify the potential impact of emission increases or reductions

### Policy Impact:
The findings will equip policymakers to:
- Design evidence-based emission reduction strategies
- Set realistic climate targets grounded in historical and predictive data
- Prioritize climate actions based on high-impact intervention points

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Importing and Exploring the Dataset
To conduct this analysis, we will utilize two main datasets:
- Temperature Data – Yearly records of temperature anomalies (°C) spanning multiple decades.- 
- CO₂ Data – Monthly measurements of global atmospheric carbon dioxide levels, reported in parts per million (ppm).
I loaded this dataset into the Google Colab environment. Below is the preview:

![Data preview](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/data%20preview.png)

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Basic Statistics for Temperature Changes and Carbon Emission Concentration
Next, I computed essential statistical measures—such as the mean, median, variance, etc, for both temperature anomalies and CO₂ concentrations.

![Basic Stats](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Basic%20Stats.png)

The temperature data ranges from -2.06°C to 3.69°C, covering a span of 5.75°C, with a modest skewness of 0.48 indicating a slight right-tailed distribution. Its interquartile range (0.88°C) and relatively low variability suggest moderate fluctuations over time. In contrast, CO₂ concentrations vary significantly more, ranging from -0.10 ppm to 424.00 ppm, with a spread of 424.10 ppm and a standard deviation of 180.55 ppm. The kurtosis value of -1.94 indicates lighter tails, pointing to fewer extreme outliers. Overall, CO₂ data shows much greater fluctuation compared to temperature anomalies, highlighting the more volatile nature of atmospheric carbon levels across the dataset. Both datasets are complete, with no missing values.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Time-Series Analysis
Next, I explored the trends in temperature anomalies and CO₂ concentrations over time, and analyze the relationship between these two variables.

![Time Series Analysis](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Time%20Series%20Analysis.png)

The time-series analysis reveals a clear upward trend in both CO₂ concentrations and global temperature anomalies over time. CO₂ levels are rising at an average rate of 8.3 ppm per decade, while temperatures are increasing by approximately 0.26°C per decade. This parallel growth highlights a strong visual correlation between the two variables, reinforcing the connection between rising carbon emissions and global warming. The alignment of these trends over time provides compelling evidence of CO₂’s role in driving temperature increases.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

