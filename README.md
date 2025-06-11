# Climate-Data-Analysis-CO2-Concentration-vs.-Global-Temperature-Anomalies

📌 **Project Title**: Investigating the Relationship Between Atmospheric CO₂ and Global Temperature Anomalies


🔍 **Project Motivation**

As concerns about climate change and global warming grow, I was curious about the direct connection between rising carbon dioxide (CO₂) levels in the atmosphere and changes in global temperatures. I’ve seen charts showing climate change effects, but I wanted to personally investigate real-world data from NASA and NOAA to see how much evidence there is in the data that CO₂ and global temperatures are related.


📂 **Data Sources Used**

1. NOAA CO₂ Concentration Data (co2_trend_gl.csv):

Daily CO₂ levels measured at Mauna Loa, using the "trend" column (a smoothed signal without short-term noise).

I filtered it to monthly readings to match the temperature data by selecting only rows from the 1st day of each month.


2. NASA GISTEMP Global Temperature Anomaly Data (GLB.Ts+dSST.csv):

Global monthly temperature anomalies (i.e., deviation from a long-term baseline average), given as degrees Celsius.


🔗 **Why the Datasets Were Merged**
To analyze the relationship between atmospheric CO₂ and global temperatures, I needed to combine both datasets based on time — so they could be compared on the same monthly timeline.

This is why:

The CO₂ data was filtered to one reading per month (e.g., 2020-01-01, 2020-02-01).

The temperature anomaly data already came in monthly format.

They were merged using the "Date" column as a common key to allow time-aligned comparisons.

The resulting dataset allowed for statistical analysis like correlation and regression, and for visualizing how each variable changes over time.


📈 **Key Visual Findings**

1. CO₂ Concentration over Time:

The plot of CO₂ levels (y-axis) against time (x-axis) shows a steady and rapid upward trend, especially from the mid-20th century to the present.

This clearly reflects how CO₂ has been increasing due to industrial activity, fossil fuels, and deforestation.


2. Temperature Anomaly over Time:

The plot of temperature anomalies (y-axis) against time (x-axis) shows an overall increasing trend, especially after 1970.

While there is some year-to-year variation (natural variability), the long-term trend is upward, supporting the idea of global warming.


3. Correlation Analysis:

A Pearson correlation value of around 0.73 indicates a strong positive relationship between CO₂ levels and global temperature anomalies.


4.Linear Regression Results:

Regression Model: Temperature Anomaly = 0.006 * CO₂ - 2.281

R² = 0.73: This means that about 73% of the variance in global temperature anomaly can be explained by CO₂ levels.

The scatterplot of regression shows:

A general trend that higher CO₂ corresponds with higher temperatures.

But also scatter/noise, meaning other factors (natural variability, other greenhouse gases, volcanic activity, etc.) also influence temperatures.


5. Smoothed Trends Plot (CO₂ vs Temperature Anomaly):

When plotting smoothed CO₂ values against temperature anomalies, the trend looks more consistent.

CO₂ slowly increases from ~320 ppm to 420 ppm.

Temperature anomalies, though more scattered, generally align with that CO₂ rise — confirming the positive association.


📚 **Interpretation and Implications**

This analysis provides real-world, data-driven evidence that:

Atmospheric CO₂ levels have risen dramatically over recent decades.

Global temperature anomalies have also increased.

There is a strong correlation and a statistically meaningful linear relationship between the two variables.

This supports the widespread scientific consensus that human-caused CO₂ emissions are a major driver of global warming.


✨ **What I Learned**

How to clean and align real-world climate datasets.

How to perform correlation and regression analysis in Python using minimal code.

How to interpret visual patterns and statistical outputs to draw meaningful conclusions from data.

