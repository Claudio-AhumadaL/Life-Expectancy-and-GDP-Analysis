# Life Expectancy and GDP Analysis

Data analysis and visualization project for Codecademy's Data Science Career Path. I worked on this project during the first week of March, 2023. It's one of my first approaches to working with data in a professional matter. Any questions, commentaries or suggestions can be addressed to clahumadal@gmail.com

Thank you in advance for reading it!


## Summary

The data used for this project had GDP and life expectancy information about six different countries (Chile, China, the U.S., Zimbabwe, Germany and Mexico), taken from the World Health Organization and the World Bank. This information included data taken from years 2000 to 2015. 

The provided dataframe had 4 columns ("Country", "Year", "Life expectancy at birth (years)" and "GDP"), and had a total of 96 entries.

### Data Sorting

To facilitate working with the columns, "Life Expectancy at birth (years)" column was renamed as "LEB_years".

To have a better access to visualization tools, data was sorted by the following criteria:

* Filtered by **country**
* Filtered by **year**
* Filtered by **state of development** (Developed = The U.S., China, Germany. Underdeveloped = Chile, Mexico, Zimbabwe).

### Data Visualization

To visualize the data the following figures were produced:

* GDP mean for each country:
    + All countries displayed on the **same barplot** including each country's standard deviation.
    
* GDP Change over time:
    +  Separate **side-by-side lineplots** for each country.
    +  All countries displayed on the **same lineplot**.
    
* Life expectancy mean for each country:
    + All countries displayed on the **same barplot** including each country's standard deviation.
    
* Life expectancy over time:
    +  Separate **side-by-side lineplots** for each country.
    +  All countries displayed on the **same lineplot**.
    
* Life expectancy at birth and GDP:
    +  **Bubble chart** displaying Life Expectancy vs Years, with GDP as the size of each point. Separate bubble chart for developed and underdeveloped countries.
    
### Statistical Analysis

Mean and median values were extracted for each country during the whole period to showcase the differences they had both in GDP as in Life Expectancy.

Based on the relations showcased by the different figures, an statistical analysis was performed on the general GDP - Life Expectancy relationship using NumPy's Covariance and SciPy Correlation (Pearson's r test). This same test was performed to the data filtered by developed and underdeveloped countries.

## Conclusions

* GDP Change over time in separate lineplots showed that **all the countries studied, except China, had a decrease on their GDP between the years 2008 and 2009**. This may be related to the US' Economic Crisis that happened around that year.

* GDP Change over time in the same lineplot showed that there is a great difference in the orders of magnitude of each country's GDP. An y-axis adjustment to use a logarhitmic scale has to be used to be able to effectively display the different countries on the same figure. This figure showed that the countries tend to follow a similar trend of slow grow regarding their GDP. China is an exception of this, showing a rapid increase of their GDP. **China's GDP surpassed Germany's GDP around 2007**.

* The highest average GDP difference happens between the US and Zimbabwe, with about 1 x 10<sup>4</sup> dollars of difference. The highest average Life Expectancy happens between Germany and Zimbabwe, with 29.56 years of difference between them.

* Chile has the **second highest average Life Expectancy among the studied countries**, only behind Germany.

* Life Expectancy over time in separate lineplots showed that Chile had a decrease on their Life Expectancy between 2008 and 2010, which happened to Mexico between 2007 and 2008. China, Germany and the U.S. showed a positive trend on their Life Expectancy during the whole period. Zimbabwe showed a decrease on their Life Expectancy between 2000 and 2004, and after that it increased consistently.

* The bubble charts prepared for developed and underdeveloped countries suggest that **the size of a GDP does not necessarily imply a higher Life Expectancy**. In the developed countries bubble chart it can be seen that Germany has a smaller GDP compared to the US, yet it had a higher life expectancy during the overall period. This figure also shows the growth of China's GDP, specially since 2007 to 2015. The underdeveloped countries bubble chart shows that Chile has a higher life expectancy compared to Mexico, even though the latter has a higher GDP. In the case of Zimbabwe, their GDP didn't grow significantly enough to be showed in this figure in the whole period, yet their life expectancy grew from 2004 and onwards. **This suggests that Zimbabwe's higher life expectancy values are not caused by a variation on their GDP.**

* Pearson's r test showed that even if there may be some positive relation between GDP and Life Expectancy values for these countries in the reported period, **it isn't strong enough to be confidently called a correlation**. Nonetheless, **for underdeveloped countries the result of the test was of approximately 0.52, which is a higher than the values obtained both for the general dataframe as well for the developed countries dataframe**. This suggests that it may be that the impact of the GDP - Life Expectancy relation is better showcased in underdeveloped countries due to their economic situation. This ideas should be explored further to determine whether there is a correlation between GDP and Life Expectancy for these kind of countries or not.