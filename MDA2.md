Mini Data Analysis: Report 2
================
Harsh Sharma
21/10/2021

## Overview

This report continues the exploratory data analysis performed in Report1
on the ‘cancer\_dataset’ chosen from the `datateacher` package.
Incremental effort will be placed in exploring in more detail the
dataset in a fashion that will lead to geenrating insights to answer the
research questions.

## Set-up

First we need to load the following two packages:

``` r
# Installing packages if missing, required only once
# install.packages("devtools")
# devtools::install_github("UBC-MDS/datateachr")

library(datateachr)
library(tidyverse)
```

## Task1: Processing and Summarizing Data

From earlier analysis we know the cancer\_dataset has the following high
level characteristics:

-   Shape is: 569, 32

-   Data class is: spec\_tbl\_df, tbl\_df, tbl, data.frame

### Task 1.1: Research Questions

Following are the research questions formulated in Report1:

1.  **Can a binary (malignant or benign) classification model be
    generated the given variables and dataset?**

2.  **Is data distribution/characteristics comparable between the benign
    and malignant classes?**

3.  **What variable(s) have the strongest correlations to the response
    variable?** Which next leads us to finding the optimized set of
    variables having the highest model performance. This inherently
    involves analyzing the three associated columns for the same
    parameter (example: radius\_mean, radius\_se, radius\_worst) in
    order to minimize redundancy.

4.  **Identifying what variable(s) contributes to the highest model
    sensitivity**. In this problem setting it is better to have a false
    positive than a false negative.

*PS: Research question 4 has been replaced in the follwong section due
to better alignment with this report’s instruction and also the course
scope.*

### Task 1.2: In-depth EDA

In this section atleast one summarizing and one graphing task is
attempted per research question.

#### Question1 - Generating binary classification model

Computing the summary statistic of numeric variable ‘radius\_mean’
across the categorical variable ‘diagnosis’:

``` r
# First grouping by diagnosis
# Using dyplr::unite() to output range as asked in question
cancer_sample %>%
  group_by(diagnosis) %>%
  summarize(min_value=min(radius_mean), max_value=max(radius_mean), mean=mean(radius_mean,na.rm=TRUE),median=median(radius_mean), sd=sd(radius_mean)) %>%
  unite(range, min_value, max_value, sep="-")
```

    ## # A tibble: 2 x 5
    ##   diagnosis range        mean median    sd
    ##   <chr>     <chr>       <dbl>  <dbl> <dbl>
    ## 1 B         6.981-17.85  12.1   12.2  1.78
    ## 2 M         10.95-28.11  17.5   17.3  3.20

Graphing mean\_radius with at least two geom layers:

``` r
# Using classic theme to maximize pixed-info ratio per best practices 
cancer_sample %>%
  ggplot(aes(diagnosis, radius_mean))+
  geom_boxplot(width=0.2)+
  geom_jitter(alpha=0.1, width=0.2)+
  theme_classic()
```

![](MDA2_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

The above results clearly indicate discernible difference in variable
‘radius\_mean’ across begnin and malignant diagnosis. This is strong
indicator that binary classification is possible.

#### Question2 - Comparing begnin and malignant data distribution

Computing the number of observations for categorical variable
‘diagnosis’:

``` r
# Without using table() as the output is not data frame
cancer_sample %>%
  group_by(diagnosis) %>%
  tally()
```

    ## # A tibble: 2 x 2
    ##   diagnosis     n
    ##   <chr>     <int>
    ## 1 B           357
    ## 2 M           212

Plotting graph of choice:

``` r
cancer_sample %>%
  ggplot(aes(x=factor(1), fill=diagnosis))+
  geom_bar()+
  coord_polar(theta="y")+
  scale_fill_grey()+
  theme_minimal()+
  theme(axis.title.y = element_blank())
```

![](MDA2_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

The above graph is appropriate for the research question2. However,
additional graph is plotted since the instructions require logarithmic
axis scale:

``` r
cancer_sample %>%
  ggplot()+
  geom_point()
```

### Task1.3: Learning
