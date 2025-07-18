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
As global temperatures continue to rise, the role of carbon dioxide (CO₂) emissions in driving climate change remains a critical concern. This project leverages historical climate data to explore the relationship between atmospheric CO₂ concentrations and global temperature anomalies. By applying regression modeling, clustering, and scenario simulation, the analysis aims to uncover actionable insights into how emission trends impact global warming and how future scenarios could influence climate outcomes.

### Core Objectives
#### 1. Historical Pattern Exploration
- Analyze long-term trends linking CO₂ concentrations with global temperature anomalies
- Evaluate the impact of industrial activities on rising emissions and temperature changes

#### 2. Climate Clustering & Pattern Recognition
- Group years with similar climate conditions based on CO₂ and temperature data
- Reveal hidden patterns and transitional phases in climate behavior over time

#### 3. Predictive Scenario Modeling
- Simulate hypothetical changes in CO₂ levels and their projected effect on global temperatures
- Assess the sensitivity of climate response under different emission scenarios

#### 4. Policy Relevance and Strategic Guidance
- Translate findings into practical insights for climate policy formulation
- Support data-informed decision-making to shape realistic emission targets and adaptation strategies

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

![Correlation Coefficient](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Correlation%20Coefficients.png)

![granger Causality](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Granger%20Causality.png)

The Pearson correlation coefficient (0.955) indicates a very strong linear relationship between CO₂ concentrations and temperature anomalies, while the Spearman correlation (0.938) also confirms a very strong monotonic relationship, meaning that as CO₂ levels increase, temperature anomalies tend to increase consistently. However, the Granger causality test results show p-values of 0.0617 (lag 1), 0.6754 (lag 2), and 0.2994 (lag 3). The p-value for lag 1 is slightly above the common significance threshold of 0.05, suggesting weak evidence of causality, while lags 2 and 3 are not statistically significant, indicating no evidence of causality. Therefore, although CO₂ concentrations and temperature anomalies are strongly correlated, the Granger causality test does not provide strong evidence that CO₂ changes directly cause temperature anomalies within the lags tested.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Lagged Effects Analysis
We will now investigate whether past CO₂ concentrations influence current temperature anomalies by introducing lagged variables—shifting CO₂ data by 1, 2, and 3 years. This approach helps assess any lagged effects that historical CO₂ levels may have on present-day temperature changes. Using these lagged values, we will construct an Ordinary Least Squares (OLS) regression model, with both current and lagged CO₂ concentrations as predictors. The goal is to evaluate the extent to which present and past CO₂ levels contribute to temperature anomalies and to identify whether there is a statistically significant lagged impact over time.

![Lagged Effects Analysis Results](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Lagged%20Effects%20Analysis.png) 

The lagged effects analysis reveals that current CO₂ levels have a significant and positive impact on temperature anomalies, with a coefficient of 0.3245°C per ppm (p < 0.001). Additionally, CO₂ levels from one year prior also show a significant but negative effect (-0.2962), suggesting a short-term compensatory or delayed adjustment in the climate system. However, lagged CO₂ values from two and three years ago are not statistically significant, indicating minimal delayed influence beyond one year. The model is highly explanatory, with an R-squared of 0.949, meaning it accounts for nearly 95% of the variation in temperature anomalies. Overall, the results highlight the dominant role of current CO₂ emissions and a notable one-year lag effect in driving temperature changes.


![OLS regression results](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/OLS%20Regression.png)

The OLS regression results demonstrate a strong relationship between CO₂ levels and temperature, with an R-squared value of 0.949, indicating that approximately 94.9% of the variation in temperature is explained by the model. The coefficient for current CO₂ concentration (0.3245) is statistically significant (p < 0.001), suggesting a positive and substantial association between CO₂ levels and temperature. Additionally, the one-period lag of CO₂ (CO2_Lag_1) is also statistically significant (coefficient = -0.2962, p < 0.001) but shows a negative effect, indicating possible short-term dynamics or adjustments in the system. In contrast, the two- and three-period lags (CO2_Lag_2 and CO2_Lag_3) are not statistically significant (p > 0.8), implying limited influence of CO₂ beyond one lag period. Overall, the model provides strong evidence of an immediate and significant impact of CO₂ on temperature variations.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Clustering Climate Patterns
We then use K-Means clustering to categorize years according to patterns in temperature anomalies and CO₂ concentrations.

![Climate Pattern Clusters](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Clustering%20Climate%20Patterns.png)

The K-Means clustering results divide the data into four distinct groups based on similarities in CO₂ concentrations and temperature anomalies: Low Temp & Low CO₂, Low Temp & High CO₂, High Temp & Low CO₂, and High Temp & High CO₂. This segmentation reveals a clear progression: early years (1960s to 1980s) mostly fall under the Low Temp & Low CO₂ cluster, while recent years (1990s to 2020s) increasingly shift into the High Temp & High CO₂ category. Notably, the High Temp & High CO₂ cluster spans from 1994 to 2022 and dominates the recent decades, suggesting a sustained rise in both carbon emissions and temperature anomalies.

This clustering pattern highlights the growing impact of rising CO₂ concentrations on global temperatures over time. It demonstrates how climate behavior has shifted significantly, with a marked increase in high-temperature years closely associated with elevated CO₂ levels-underscoring the urgency for effective climate mitigation strategies.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Temperature Changes Prediction Under What-If Analysis
Next, we apply a simple linear regression model to explore how variations in CO₂ concentrations could potentially affect global temperature anomalies. By modeling the historical link between CO₂ levels and temperature changes, we can project future outcomes under different emission scenarios.

To begin, we train a linear regression model using historical CO₂ concentrations as the predictor and corresponding temperature anomalies as the response variable. After training, we use this model to simulate various hypothetical futures by adjusting the average CO₂ concentration by a given percentage.

For each scenario, we modify the current CO₂ average accordingly, input the new value into the model, and generate the predicted temperature anomaly. The scenarios analyzed include:

![Climate Scenario Prediction](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Climate%20Scenario%20Projections.png)

![Temperature Change Prediction](https://github.com/Petkofi/Global-Carbon-Emission-Impact-Analysis/blob/main/Temperature%20Change%20Prediction.png)

Based on the simulation results, a 20% increase in CO₂ levels could lead to a temperature rise of approximately 1.15°C, highlighting a strong warming effect under high-emission scenarios. Similarly, a 10% increase projects a moderate warming of around 0.57°C. On the other hand, reducing CO₂ by 10% or 20% results in cooling of 0.57°C and 1.15°C respectively, indicating that substantial emission cuts could significantly reverse current warming trends. With an R² score of 0.913 and a standard error of ±0.15°C, the model demonstrates strong predictive performance and suggests that global temperatures are highly sensitive-about 3.18°C per 100 ppm-to changes in atmospheric CO₂ levels.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Implications and Recommendations
### 1. CO₂ Emissions Significantly Drive Temperature Increases
The strong linear relationship (R² = 0.913) between CO₂ levels and temperature anomalies confirms that rising atmospheric CO₂ is a primary contributor to global warming. Continued emissions will likely lead to amplified temperature extremes.

### 2. Emission Reductions Offer Measurable Cooling Effects
Scenario simulations show that reducing CO₂ concentrations by 10–20% could lower global temperatures by up to 1.15°C. This reinforces the critical importance of emission mitigation strategies for climate stabilization.

### 3. Climate Sensitivity Calls for Rapid Policy Action
With a climate sensitivity of 3.18°C per 100 ppm CO₂, even small increases in atmospheric carbon levels can have substantial warming impacts. Immediate and sustained policy efforts are required to curb emissions and avoid irreversible tipping points.

### 4. Leverage Predictive Models for Climate Planning
Accurate modeling enables policymakers and scientists to test hypothetical scenarios and guide future climate strategies. Continued development and integration of such models into climate planning can enhance decision-making.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)

## Conclusion
Our analysis reveals a strong positive correlation between rising atmospheric CO₂ concentrations and global temperature anomalies, with carbon levels increasing at a notably faster pace than temperature changes. Clustering techniques underscore distinct patterns across different periods, showing how elevated emissions align with warmer temperature phases. Time-series observations further illustrate a steady upward trend in both CO₂ and temperature, signaling persistent climate pressure. Scenario simulations emphasize the high sensitivity of global temperatures to CO₂ fluctuations-demonstrating that even moderate reductions in emissions could lead to measurable cooling effects. These insights collectively highlight the urgent need for aggressive climate action and policy interventions to stabilize emissions and limit future warming.

![--](https://github.com/Petkofi/Netflix-Content-Analysis-A-Comprehensive-Intelligence-Framework-for-Data-Driven-Decisions/blob/main/divider.png)
