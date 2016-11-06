# Exercise 9: Comparing data to predictions
In this week's exercise we XXX.

This exercise is due by the start of class on **14.11.2016**.
Late submissions will lose 25% of the total points per day late unless discussed with Dave or Jorina in advance of the due date.

## Problem 1: Calculating a goodness-of-fit
For this problem, you are given a [broken Python script](read-and-plot-data.py) for reading and plotting thermochronometer age data.
Your job is to fix the **6 issues** with the script so that it does what says it should in the comments.
The issues are in comments that start with the text `# FIX`.
Data for this exercise comes from a [recent paper published on the exhumation of the Himalaya in Bhutan](http://dx.doi.org/10.1002/2013JB010891), in case you're curious.
Your modified script should

1. Read the data file and split the data into separate arrays for each variable.
2. Calculate the goodness of fit between the measured and predicted ages in the data file. The goodness of fit equation you should use is

    ![Reduced chi-squared](Images/reduced-chi-squared.png)<br/>
where *n* is the number of ages, *O* is the measured age, *E* is the predicted age and *σ* is the standard deviation.
3. Produce a plot of the measured ages with their error bars and the predicted ages, both as a function of latitude. Be sure to include axis labels and a title.

### Questions for Problem 1
1. Looking at your plot and without looking at the goodness of fit value, how well would you say the predicted ages fit the measured ages in this example? Is this difficult to do? Why or why not?
2. How well would you say the predicted ages fit the measurements using the calculated goodness of fit? Is your calculated goodness of fit intuitive to use? Why or why not?

**For this problem, save a modified copy of the code in your Github repository and edit the `README.md` document to display a copy of your plot and answers to the questions above.**

## Problem 2: Linear data regression

### Tasks/Questions for Problem 2

## Hints
If you get stuck, have a look at the [hints for this week's exercise](https://github.com/Intro-Quantitative-Geology/Lesson-8-Basic-geostatistics/blob/master/Lesson/hints.md).

### Footnote(s)
[1]: [Coutand, I., Whipp, D.M., Grujic, D., Bernet, M., Fellin, M.G., Bookhagen, B., Landry, K.R., Ghalley, S.K. and Duncan, C., 2014. Geometry and kinematics of the Main Himalayan Thrust and Neogene crustal exhumation in the Bhutanese Himalaya derived from inversion of multithermochronologic data. *Journal of Geophysical Research: Solid Earth*, *119*(2), pp.1446-1481](https://dx.doi.org/10.1002/2013JB010891)

# Answers
This is some text.
You can make it **bold** or use *italics*.
You can also display images, as shown below.

![A sine curve](Images/sine-curve.png)<br/>
*Figure 1. A sine curve*.
