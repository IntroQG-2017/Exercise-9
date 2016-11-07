# Exercise 9: Comparing data to predictions
In this week's exercise we will work on comparing observations (data) to predictions.
In particular, we will explore two different ways in which we can compare data to a prediction:

- Comparing individual measured values to their equivalent predicted values using a *goodness-of-fit* equation
- Fitting a line to *xy* data using the *least squares regression*

Both of these cases are frequently used, and can even be conducted in commonly used software such as **Microsoft Excel**, but our goal is to understand what the numbers from these "fits" mean, and how they are calculated.

This exercise is due by the start of class on **14.11.2016**.
Late submissions will lose 25% of the total points per day late unless discussed with Dave or Jorina in advance of the due date.

## Problem 1: Calculating a goodness-of-fit
For this problem, you are given a [broken Python script](read-and-plot-data.py) for reading and plotting [thermochronometer age data](Data/Coutand2014-AFT-ages.txt).
Your job is to fix the **6 issues** with the script so that it does what says it should in the comments.
The issues are in comments that start with the text `# FIX`.
Data for this exercise comes from a [recent paper published on the exhumation of the Himalaya in Bhutan](http://dx.doi.org/10.1002/2013JB010891), in case you're curious.
Your modified script should

1. Read the data file [`Coutand2014-AFT-ages.txt`](Data/Coutand2014-AFT-ages.txt) and split the data into separate arrays for each variable.
2. Calculate the goodness of fit between the measured and predicted ages in the data file.
The goodness of fit equation you should use is

    ![Reduced chi-squared](Images/reduced-chi-squared.png)<br/>
where *N* is the number of ages, *O<sub>i</sub>* is the *i*th measured age, *E<sub>i</sub>* is the *i*th predicted age, and *σ<sub>i</sub>* is the *i*th standard deviation.
3. Produce a plot of the measured ages with their error bars and the predicted ages, both as a function of latitude.
Be sure to display the calculated goodness-of-fit value from point 2 as text on the plot, and include axis labels and a title.

**For this problem, save a modified copy of the code in your GitHub repository, and edit the `README.md` document to display a copy of your plot and answers to the questions below.
For the plot, also include a figure caption presenting the figure as if it were in a scientific journal article.**

### Questions for Problem 1
1. Looking at your plot and without looking at the goodness of fit value, how well would you say the predicted ages fit the measured ages in this example?
Is this difficult to do?
Why or why not?
2. How well would you say the predicted ages fit the measurements using the calculated goodness of fit?
Is your calculated goodness of fit intuitive to use?
Why or why not?

## Problem 2: Linear data regression - NOAA climate data revisited again (!?!)
For this problem we will again use the NOAA climate data from Exercises 5-7, with a slight twist.
As a reminder, you will be working with a climate data file from the [US National Oceanographic and Atmospheric Administration (NOAA) climate database](https://www.ncdc.noaa.gov/cdo-web/).
The data file [`816295.csv`](Data/816295.csv) comprises daily temperature measurements (in Fahrenheit) from several stations in the vicinity of the town of Ann Arbor, Michigan in the US from 1 January 1926 to 31 December 2015.

You job in this problem is to modify your code used for Exercises 6 and 7 to do the following:

1. Perform the calculations of the seasonal average temperatures for summer and winter from 1927-2015, writing out the seasonal average temperature and *standard deviation in seasonal temperature* for each year to files titled `winter-avg-temps-stddev.csv` and `summer-avg-temps-stddev.csv`.
2. Calculate the slopes `B` and *y*-intercepts `A` for [linear regression lines](https://github.com/Intro-Quantitative-Geology/Lesson-9-Fitting-data/blob/master/Lesson/least-squares.md) of the both seasonal average temperatures versus time for:
  - The entire time covered in the data
  - The last 20 years
3. Plot the results.
The seasonal average temperatures should be plotted including their error bars based on the standard deviation in seasonal temperature and the corresponding linear regressions on two plots:
  - One for the entire time covered in the data
  - One for the last 20 years
4. Each plot should include axis labels, a title and a legend, as well as text displaying the slope of the regression lines for both the summer and winter seasons.

**For this problem, save a modified copy of your code(s) in your GitHub repository, and edit the `README.md` document to display a copy of both of your plots and answers to the questions below.
For the plots, also include figure captions presenting the figures as if they were in a scientific journal article.
Your modified codes can be kept in separate files as used for Exercises 6 and 7, or combined into a single script file.**

### Questions for Problem 2
1. For the linear regressions for the entire age range of seasonal average temperature data, is a line a suitable representation of the changes in seasonal average temperature from 1927-2015?
In other words, does your linear "fit" fall entirely within the uncertainty of your seasonal average temperatures, or are there some years where the line is outside of the standard deviation in seasonal temperature?
Is a linear fit an appropriate choice?
2. Again for the linear regressions for the entire age range of seasonal average temperature data, do you see any difference in the slopes calculated using your code for this exercise and the `linregress()` function from the `scipy.stats` module?
If so, how do they differ?
Do you have any idea why they might be different?
Lastly, do you now have a better sense of what `linregress()` does?
3. For the linear regressions for the last 20 years, is a line a suitable representation of the changes in seasonal average temperature?
By how much do your linear regression lines suggest seasonal average temperatures have changed per year?
Do you find these results surprising?
Why or why not?

## Hints
If you get stuck, have a look at the [hints for this week's exercise](https://github.com/Intro-Quantitative-Geology/Lesson-9-Fitting-data/blob/master/Lesson/hints.md).

### Footnote(s)
[1]: [Coutand, I., Whipp, D.M., Grujic, D., Bernet, M., Fellin, M.G., Bookhagen, B., Landry, K.R., Ghalley, S.K. and Duncan, C., 2014. Geometry and kinematics of the Main Himalayan Thrust and Neogene crustal exhumation in the Bhutanese Himalaya derived from inversion of multithermochronologic data. *Journal of Geophysical Research: Solid Earth*, *119*(2), pp.1446-1481](https://dx.doi.org/10.1002/2013JB010891)

# Answers
This is some text.
You can make it **bold** or use *italics*.
You can also display images, as shown below.

![A sine curve](Images/sine-curve.png)<br/>
*Figure 1. A sine curve*.
