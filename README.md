# Ironhhack Project 1 - Pandas
## Global Shark Attacks - Project overview
This project has been the first one I have done as part of my course on Data Analytics, focusing mainly on Python and dataframes cleaning & wrangling via Pandas.

The data source used for this project is coming from the Kaggle API, but there was some data cleaning needed in order to get more of an useful input for the upcoming data analysis. 

### Data Cleaning
The first step after importing the libraries needed - mainly Regex, Pandas & Numpy -, has been cleaning the actual database given the large amount of empty cells it contained. In order to do that, I have applied some filters so I could have visibility of the actual number of empty cells I could get rid off - pretty much 20,000 rows of empty data have been removed, which means there are around 6,300 rows of actual data relevant for the project.

Similar approach for columns, where those columns that are either empty or not relevant enough for the purpose of this project have been deleted to make the upcoming analysis easier and more straightforward.

There were also a few repeated values from the column "Case Number", which should be unique given it is referring to actual people attacked by sharks.

Once the cleaning above has been executed, I have been able to establish some hypothesis to work on to further explore the data.

### Hypothesis
Before sharing the hypothesis I did set up for this project, I think it is worth mentioning what the data for this project looks like: essentially, it is a register of all those people that have been attacked by sharks all over the world throughout the years, regardless of this attack being fatal (i.e. people being killed) or not (i.e. people surviving).

Given the nature of the data, I have established the following three hypotheses:

1) Over the time, Australia is the country where men had more attacks whilst surfing.
2) 2015 was the year with less accidents across all activities in the last 10 years. From the top 3 countries for that year, 30% of the accidents where fatal and mainly with men involved (60% of the total cases within this scope where men).
3) People aged 30-50 have been the most injured people during summer (June-September) for the last 20 years, regardless of the hemisphere they live at.


In order to assess/validate these hypotheses, I have done more cleaning, applied ad-hoc filters - such as conditions, using Regex and concatenating different filtered databases - as well as doing a cross-check of different variables to see how they relate to each other.

With regards to the first hypotheses, the first thing I have done is getting the actual number of cases by gender as well as cleaning the variable "Year" so it is an actual integer number, as opposed to a float.

figure_one.jpg
Once this has been done, I have filtered the "Activity" variable so I could see how the data relates to "Surfing". I have also applied a conditional filter so I could get the final numbers I was after given the scope of the hypothesis. With all of that, I could see Australian men got attacked more times than Australian women.
figure_two.jpg

Having said that, when I compared the results vs. the other countries, especially vs. the top 5 more attacked countries, Australia WAS NOT the main one, that was the US, so this hypothesis has been rejected.
figure_three.jpg

With regards to the second hypothesis, I have firstly cleaned some more variables so I could get the most refined version, especially for the variables "Fatal Y/N" and "Year" (being the last one filtered for the last few years as 2015 is the year I was after).
With that, I could see 2015 IS NOT the year where the shortest number of attacks happened in the last 10 years, it's the one with the largest one actually.
figure_five.jpg
Regardless of the result, I still had a look at the top 3 countries to see how much percentage they represent, which is actually 80%. These countries are the US, Australia & South Africa.
figure_seven.jpg
When it comes to the fatality, there were only 3 cases registered in 2015.
figure_eight.jpg

With regards to the last hypothesis, I have used Regex in order to filter some data as well as have created new conditional columns so I could gather the information needed (e.g. age ranges and quarter of the year, given I'm interested in the summer/the third one).
figure_eleven.jpg
This chart is summarising the number of attacks that happened by age range and quarter for the last 20 years.
Surprisingly, people aged between 10-20 years old were the ones with the largest number of shark attacks, followed by people between 20-30 years old.

###Key challenges & learnings
- Getting familiarised with different techniques/approaches we can follow to get the same output.
- The more data you clean  at the beginning, the more time you save afterwards.
- The quality of the data source is very important - the better quality, the better for analysis.
- Importance of how to visually show the output of your analysis. As much information as possible but as easy as possible for the audience!


###Links & Resources
    https://www.kaggle.com/teajay/global-shark-attacks
    https://numpy.org/doc/1.18/
    https://pandas.pydata.org/
    https://docs.python.org/3/library/functions.html
    https://plotly.com/python/
    https://matplotlib.org/
    https://seaborn.pydata.org/
    https://pandas.pydata.org/docs/




[def]: images/figure_one.jpg