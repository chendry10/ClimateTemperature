---
layout: default
---

<a href="Resume.pdf" download>
  <button style="background-color: #4CAF50; color: white; border: none; padding: 10px 20px; text-align: center; text-decoration: none; display: inline-block; font-size: 16px; margin: 4px 2px; cursor: pointer;">
    Download My Resume
  </button>
</a>

<a href="FinalProject.ipynb" download>
  <button style="background-color: #4CAF50; color: white; border: none; padding: 10px 20px; text-align: center; text-decoration: none; display: inline-block; font-size: 16px; margin: 4px 2px; cursor: pointer;">
    Download My Colab Worksheet
  </button>
</a>

# **Cameron Hendry and Eli Buffington**  
📍 **Location**: Washington

# Climate and Temperature Relationship   

# Correlation between carbon dioxide  emissions and Temperature in the United States  


# Introduction

## The data that we used was temperature data from the United States and also carbon dioxide data from the United States from 1991 to 2019\. These were two separate datasets. We did not have too many issues with the data. Downloading the data was made simple by the website that we were downloading from allowing us to choose different time periods and sample frequencies. The most difficult part was lining up the data and merging the two dataframes together which we eventually got working. 

The question we wanted to answer was: Is there a correlation between CO2 emissions and Temperature?

To answer this question we created graphs and used the highly scientific “eyeball test” (hahaha) and actual statistics to find the correlation between these two datasets by obtaining a p-value. 

# Methods & Results. 

The way that we were able to compare these two dataset was by using a time series and merging the two separate data frames together on the time column. We also only used yearly data averaged on January 1st of every year. One of the bigger issues that came up was how to plot data with two different units on the same graph. The way we solved this is by having two different y-axes, one on the left and one on the right side of the graph, so that we could see both graphs together on the same chart. 

{% include_relative fig1.html %}

The above is change in degrees celsius and change in tons of carbon dioxide emissions plotted on the same graph. We observed that a change in carbon dioxide emissions is followed by a change in temperature after two to five years. This is reasonable because climate change is a slow process that happens over years not months or days. Carbon dioxide  emitted from someone’s tailpipe probably does not instantly affect the temperature which explains the lag in the data. 

We used this data to run a linear regression on change in degrees celsius and change in tons of carbon dioxide emissions, with change in tons of carbon dioxide emissions as our independent variable and change in degrees celsius as the dependent variable. The regression had an R2 of 0.024, which means that only 2.4% of the change in temperature was explained by a change in carbon dioxide emissions. The regression equation is displayed on the following graph. The p-value on the coefficient on change in tons of carbon dioxide emissions was 0.421, which is far above the statistically significant value of 0.05. This means that we cannot reject the null and we cannot conclude that the effects were anything but chance. 

{% include_relative fig2 %}

This is a graph with difference in yearly carbon dioxide emissions as the independent variable and difference in yearly temperature as the dependent variable, with the line of best fit plotted over the data points. This graph explains our low p-value, as our data does not follow the line. Additionally, the slope of the line is negative, which implies that increasing carbon dioxide dioxide correlates with a decrease in temperature, which is illogical.

We then shifted the data for temperature by ten years in either direction and calculated the correlation coefficient for each. We then took the highest one and shifted our data by that amount. In our case, we concluded the offset was \-5, meaning that the change in carbon dioxide emissions was most correlated to temperature changes in 5 years.

{% include_relative fig3.html %}

In this graph we shifted the temperature graph by 5 years to showcase how the delay lines up and dropped 5 years off the end of both graphs. This graph shows how the CO2 emissions would affect the temperature if the effects were instantaneous. A bunch of the peaks and valleys line up pretty perfectly near the beginning and for some reason near the end there is less correlation which we are still unable to explain. 

We used this shifted data to run a linear regression on change in degrees celsius after the shift and change in tons of carbon dioxide emissions, with change in tons of carbon dioxide emissions as our independent variable and shifted change in degrees celsius as the dependent variable. The regression had an R2 of 0.069, which means that only 6.9% of the change in temperature was explained by a change in carbon dioxide emissions. The regression equation is displayed on the following graph. The p-value on the coefficient on change in tons of carbon dioxide emissions was 0.216, which is far above the statistically significant value of 0.05. This means that we cannot reject the null and we cannot conclude that the effects were anything but chance. 

{% include_relative fig4.html %}

This is a graph with the difference in yearly carbon dioxide emissions as the independent variable and the shifted difference in yearly temperature as the dependent variable, with the line of best fit plotted over the data points. This graph explains our medium p-value, as our data does not follow the line well but there appears to be some sort of collocation which explains our lower p-value, although not enough to be statistically significant. Additionally, the slope of the line is positive, which implies that increasing carbon dioxide dioxide correlates with an increase in temperature, which shows that this is likely closer to the truth than the previous analysis.

# Conclusions

Unfortunately, we were unable to find a statistically significant p-value, even after shifting the data to account for any lags between when the carbon dioxide  was produced and when the temperature changed. We were unable to reject the null hypothesis, which was that a change in carbon dioxide release has no effect on change in temperature. A major limitation to our data is that it only accounted for United States temperature and carbon dioxide  emissions and was blind to less local effects. Another limitation was that the tracking of carbon dioxide  emissions in our publicly available data set only went back until 1990, so we were unable to observe longer term changes that might have yielded more significant results. We believe that the magnitude of climate change was low enough across the relatively short chunk of time we measured that our analysis was blind to its effects, and was masked by the local unpredictability of climate. We would not recommend making long term conclusions based on our failure to reject the null hypothesis. 

An area for future study would be looking at atmospheric carbon dioxide emissions instead of carbon dioxide release. This would yield greater insight into the effects of carbon dioxide emissions as it would bypass the country specific reporting requirements that are prone to corruption and the falsification of results. 

 

# References 

Food and Agriculture Organization of the United Nations (FAO). *FAOSTAT: Emissions Totals.* FAO, [https://www.fao.org/faostat/en/\#data/ET](https://www.fao.org/faostat/en/#data/ET). Accessed 19th November. 2024\.

Singh, Ravindra. "Carbon CO2 Emissions." *Kaggle*, [https://www.kaggle.com/datasets/ravindrasinghrana/carbon-co2-emissions](https://www.kaggle.com/datasets/ravindrasinghrana/carbon-co2-emissions). Accessed 14th November. 2024\.



[Main Page](https://chendry10.github.io/WhereSchueller/)
