---
title       : Data Products Project
subtitle    : Mile Per Gallon Predictor
author      : Eric LAMY - November 2015
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

This presentation describes my contribution to the Data Products project assignment.

A Miles Per Gallon predictor:

1. based on a linear regression model

2. using the Motor Trend cars data (1974)

3. build using Shiny app 

You can compare your actual gaz consumption with what it would have been in 1974.

--- .class #id 

## The Model - Linear Regression


A linear model is fitted in order to predict **Mile Per Gallon** with features:

* number of cylinders
* car weight
* car horsepower
* number of gears
* transmission type (manual or automatic)


$mpg = \beta_0 + \beta_1 * cylinders + \beta_2 * horsepower + \beta_3 * weight$
    $+ \beta_4 * transmission + \beta_5 * gears$

with:

$\beta_0$ = ``37.1873``; $\beta_1$ = ``-0.8060183``; $\beta_2$ = ``-0.023392``; $\beta_3$ = ``-2.6313041``; $\beta_4$ = ``-2.6313041``; $\beta_5$ = ``1.6657414``

---

## The Model - Evaluation (cont'd)

This multivariate model has:

* R-squared value of ``84.93``%.

    (indication of how good the model fits the data)

* p-value of ``6.6866851 &times; 10<sup>-10</sup>`` (F-statistic)

* residual standard error of ``2.555``


---

## The MPG Predictor

<img src="DP-MPG SidePanel.jpg" style="width: 15%; height: 15%"/img>

To use the predictor you simply enter the different values in the side bar panel.

The predictor computes the estimated gaz consumption and displays the result in the main panel.
(quantities are converted to the metric system: weight, MPG)

On the histogram graph, you can see how the car compares with those of the magazine (in MPG term).




---

## One example

This example uses values of my own car:
* 4 cylinders, car weight = 4.7 (1000 pounds), 150 hp, 5 gears and manual transmission.
* Actual consumption = 6 liters / 100 km.

<img src="DP-MPG Predictor.jpg" style="width: 75%; height: 75%"/img>

---

## Conclusion

Using a simple linear regression model and shiny app it is possible to build a web application that predicts a  given car gaz consumption.

As the data used date from the 1970s, it is possible to compare what would have been the consumption of a current vehicle.
