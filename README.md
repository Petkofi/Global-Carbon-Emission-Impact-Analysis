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

### Correlation Heatmap
![Correlation Heatmap](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Correlation%20Heatmap.png)

The correlation heatmap highlights a strong positive relationship (r = 0.96) between CO₂ concentrations and temperature anomalies, confirming that increases in atmospheric CO₂ are closely associated with rising global temperatures. The diagonal line reflects perfect self-correlation, validating the structure of the matrix, while the deep blue hues emphasize the strength of the correlation between key variables. This reinforces the need to focus on reducing carbon emissions as a critical strategy in addressing climate change.

### Scatter Plot with Marginal Distributions
![Scatter Plot ](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Scatter%20Plot.png)

The scatter plot with marginal distributions illustrates a strong linear relationship between CO₂ concentrations and temperature anomalies, with a Pearson correlation of 0.96. The fitted regression line indicates that a 100 ppm rise in CO₂ could lead to an estimated 3.18°C increase in global temperature, emphasizing climate sensitivity. The marginal histograms show that both variables follow approximately normal distributions, with temperature values ranging from -0.25°C to 1.55°C and CO₂ concentrations from 158.9 to 209.5 ppm. With 62 overlapping data points, the plot provides robust visual and statistical evidence of the strong connection between carbon emissions and global warming, reinforcing the urgency for emission-reduction policies.

### Decadal Analysis with Line Plot
![Decadal Analysis](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Decadal%20Analysis.png)

The decadal analysis reveals an apparent acceleration in both CO₂ concentrations and global temperature anomalies over time. Compared to the 1960s average, CO₂ levels in the most recent decade have risen by approximately 29.9%, reflecting the growing intensity of carbon emissions in recent years. Similarly, global temperatures have increased by 1.45°C since the 1960s, signaling a significant warming trend. This steady rise across decades underscores the long-term impact of sustained greenhouse gas emissions. The analysis not only highlights the pace at which climate change is progressing but also reinforces the need for urgent, data-informed interventions to slow the trajectory of global warming.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Trends and Seasonal Variation Analysis
Next, I used linear regression to uncover long-term trends and detect any seasonal patterns present in the data.
### Trend Analysis
![Trends Analysis](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Trends%20%20Analysis.png)

The linear trend analysis illustrates steady upward trajectories in both temperature anomalies and CO₂ concentrations over time. Temperature is increasing at a rate of 0.26°C per decade with a strong fit (R² = 0.88), indicating a consistent and significant warming trend. CO₂ concentrations are also rising—by 3.2 ppm per decade—though with a weaker fit (R² = 0.04), reflecting more short-term variability in emissions data. Despite the difference in R² values, both trends are statistically significant (p < 0.001), reinforcing the long-term link between rising carbon emissions and global temperature increases.

### Seasonal Variation Analysis
![Seasonal Variation Analysis](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Seasonal%20Variation%20Analysis.png)

The graph illustrates clear seasonal fluctuations in CO₂ concentrations, with levels peaking in May (182.3 ppm) and reaching their lowest in January (178.2 ppm), showing an annual variation of approximately 4.2 ppm. This pattern reflects the natural carbon cycle, where plant growth during spring and summer absorbs more CO₂, while decay and reduced photosynthesis in the winter months lead to higher atmospheric levels. These recurring seasonal shifts highlight the critical role of terrestrial ecosystems in regulating atmospheric carbon dioxide.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Correlation and Causality Analysis
To better understand the relationship between CO₂ concentrations and temperature anomalies, we will estimate both Pearson and Spearman correlation coefficients to measure the strength and direction of their association. Additionally, we will conduct Granger Causality tests to explore whether changes in CO₂ levels can be used to predict or potentially drive changes in global temperature.

![Correlation Coefficient]( )
![granger Causality]( )

The Pearson correlation coefficient (0.955) indicates a very strong linear relationship between CO₂ concentrations and temperature anomalies, while the Spearman correlation (0.938) also confirms a very strong monotonic relationship, meaning that as CO₂ levels increase, temperature anomalies tend to increase consistently. However, the Granger causality test results show p-values of 0.0617 (lag 1), 0.6754 (lag 2), and 0.2994 (lag 3). The p-value for lag 1 is slightly above the common significance threshold of 0.05, suggesting weak evidence of causality, while lags 2 and 3 are not statistically significant, indicating no evidence of causality. Therefore, although CO₂ concentrations and temperature anomalies are strongly correlated, the Granger causality test does not provide strong evidence that CO₂ changes directly cause temperature anomalies within the lags tested.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)
