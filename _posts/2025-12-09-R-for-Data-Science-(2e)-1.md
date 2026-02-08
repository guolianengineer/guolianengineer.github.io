---
layout: post
title:  "《R for Data Science (2e)》"
date:   2025-12-09 23:24:00 +0800
categories: 数据分析 R
---

# Introduction
The process of data science is as the following pciture showed.<br>
![model of the data science process](/assets/images/blog/2025/12/model-of-the-data-science-process.png "process flow")
Import,take data stored in R<br>
Tidy,Tidying your data means storing it in a consistent form that matches the semantics of the dataset with how it is stored. In brief, when your data is tidy, each column is a variable and each row is an observation.<br>
Transform,<br>
Visualization is a fundamentally human activity.<br>
Models<br>


# Whole game
This book focus on importing, tidying, transforming, and visualizing data, as shown in following figure<br>
![Whole game](/assets/images/blog/2025/12/whole-game.png "Whole game")


# 1.Data visualization
## 1.1 Introduction
ggplot2<br>
### 1.1.1 Prerequisites
library(tidyverse)<br>
library(palmerpenguins)<br>
library(ggthemes)<br>

## 1.2 First step
Hypothesis<br>

Do penguins with longer flippers weigh more or less than penguins with shorter flippers? <br>
What does the relationship between flipper length and body mass look like? Is it positive? Negative? Linear? Nonlinear? <br>
Does the relationship vary by the species of the penguin? How about by the island where the penguin lives?<br>
Let’s create visualizations that we can use to answer these questions.<br>

### 1.2.1 The penguins data frame
1. A data frame is a rectangular collection of variables (in the columns) and observations (in the rows). penguins contains 344 observations collected and made available by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER2.<br>
2. A variable is a quantity, quality, or property that you can measure.<br>
3. A value is the state of a variable when you measure it. The value of a variable may change from measurement to measurement.<br>
4. An observation is a set of measurements made under similar conditions (you usually make all of the measurements in an observation at the same time and on the same object). An observation will contain several values, each associated with a different variable. We’ll sometimes refer to an observation as a data point.<br>
5. Tabular data is a set of values, each associated with a variable and an observation. Tabular data is tidy if each value is placed in its own “cell”, each variable in its own column, and each observation in its own row.<br>
In the tidyverse, we use special data frames called tibbles<br>

### 1.2.2 Ultimate goal
Our ultimate goal of this chapter to plot a graphic, asa shown in the picture.
![Ultimate goal](/assets/images/blog/2025/12/unnamed-chunk-6-1.png "Ultimate goal")

### 1.2.3 Creating a ggplot