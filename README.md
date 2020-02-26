# Client Project: Utilizing Yelp Cost Estimates for Estimating Neighborhood Affluency
#### Author: Brian Jankowitz
[Medium](https://medium.com/@JankowitzB) | [LinkedIn](https://www.linkedin.com/in/brian-jankowitz/)

#### [Project Presentation](presentation.pptx)
#### [Jupyter Notebook](/code/project_notebook.ipynb)

## Problem Statement

In 2018, the number of people without health insurance increased to 28 million people, from 27.3 million the year before. 72.2% of people 100% or more below the poverty line are uninsured according to the US Census. New Light Technologies, a company that helps provide healthcare to Americans, taksed us with finding areas that are not affluent this way they can go to those areas and help people who do not have health insurance to obtain health insurance. Unlike traditional methods where you can look at demographic data such as income and unemployment rate, New Light Technologies asked us to estiamte the affluency of a neighborhood using Yelp dollar signs (\$, \$\$, \$\$\$, \$\$\$\$). The novelty of this approach is in its use of big data related to commercial activity and cost of product and services as an indicator for affluency.

## Executive Summary

We first started with gathering yelp and irs data. This gave us the basic of our data. We colleceted over 30,000 businesses from Yelp. From there, we cleaned the data and looked at IRS data to see what qualifies as an area being affluent. From there, we looked and put the IRS data together with the yelp data.  This allowed us to look at each restaurant to see if that business is in an affluent area.

We used our data and put it into a few models looking at sensitivity as we wanted to maximize the number of true positives. This is because we want to market to the maximum number of people. One of our models performed extremely well which shows us that we can predict affluent areas.

## Model Selection

All the models scored relatively the same. The model we chose is Random Forest. It has 99% for train and test but the sensititvity is the same as the other models. However, this model has means it's going to predict the true positive the most of all the models. This is good as we can market to more areas that are not in affluent areas. Other models had 100% for test which is fishy. With more time, we would need to go back and look at the data to see why the scores are relatively the same.


## Conclusions

Using Yelp price data to predict the affluency of an area may seem good on paper but according to our research, it is not a good predictor for predicting affluency of an area. When we made our model, we used the yelp dollar but it was not as important as review count and the location.
Review count and location are better predictors for seeing if an area is affluent or not. Higher review counts played more into account because the affluent aras seemed to be in densely populated areas that have more restaurants. Also, location is important as affluent people tend to live in the same areas. Our model can predict an area to be affluent confidently.

## Recommendations

The model that we created was designed for New York City. Although it is a basic model, this model should be tested in other areas to see how it compares.
We would recommend to look at specific areas that are known to be more expensive such as Times Square and the World Trade Center. A plain pizza slice costs about \$2 but in those areas, it can be \$4+ in those areas.
There are many other ways to use big data to predict the affluency of the neighborhood. We would recommend to look at apartment prices
When doing outside research, an inexpensive restaurant can be in an affluent area as well as an expensive restaurant being in a non-affluent area. In the Tribecca (10007), Don Bella pizza is rated at \$ but it is the richest zip code in New York City, according to Business Insider.
I would recommend having this project be done in a bigger group next time. In addition, I would recommend that big data be used in another way to look at affluency such as location. The next step would be to apply this to another area outside of New York City to see how our model does.

## Sources

- https://www.irs.gov/statistics/soi-tax-stats-individual-income-tax-statistics-zip-code-data-soi
- https://www.citylab.com/equity/2013/01/class-divided-cities-new-york-edition/3819/
- https://www.census.gov/library/stories/2018/09/who-are-the-uninsured.html
- Correlation Matrix and convert_string_dict_to_string provided by Varun, Adrianna, and Greg
- Ideas from James Hampton, GA Seattle for df_affluency dataframe,
