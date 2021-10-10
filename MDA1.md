Mini Data Analysis: Report 1
================
Harsh Sharma
09/10/2021

## Overview

This report includes the exploratory data analysis performed on a
dataset chosen from the `datateacher` package. Incremental effort will
be placed in familiarizing with different data sets to finally choose
one, and four research questions will formulated around it.

## Set-up

First we need to load the following two packages:

``` r
library(datateachr)
library(tidyverse)
```

The `datateachr` is comprised of the 7 semi-tidy datasets:

> 1.  apt\_buildings: Acquired courtesy of The City of Toronto’s Open
>     Data Portal. It currently has 3455 rows and 37 columns.

> 2.  building\_permits: Acquired courtesy of The City of Vancouver’s
>     Open Data Portal. It currently has 20680 rows and 14 columns.

> 3.  cancer\_sample: Acquired courtesy of UCI Machine Learning
>     Repository. It currently has 569 rows and 32 columns.

> 4.  flow\_sample: Acquired courtesy of The Government of Canada’s
>     Historical Hydrometric Database. It currently has 218 rows and 7
>     columns.

> 5.  parking\_meters: Acquired courtesy of The City of Vancouver’s Open
>     Data Portal. It currently has 10032 rows and 22 columns.

> 6.  steam\_games: Acquire d courtesy of Kaggle. It currently has 40833
>     rows and 21 columns.

> 7.  vancouver\_trees: Acquired courtesy of The City of Vancouver’s
>     Open Data Portal. It currently has 146611 rows and 20 columns.

## Task 1.1: Priliminary Dataset Selection

Based on the descriptions, I narrow down my intial choices to the
following:

1.  *building\_permits:* working for a regulatory agency, I have prior
    experience working in compliance of permits and licenses.

2.  *cancer\_sample:* I am interested to pursue my research in a field
    related to algorithms employed in healthcare digital images so this
    seems very meaningful and applicable

3.  *parking\_meters:* having worked for Translink, this may be an
    interesting dataset to probe into parking trends and by extension
    into travel behavior

4.  *vancouver\_trees:* interesting dataset that may be leverage-able to
    assess the effects of climate change and/or rate of planting by the
    city

## Task 1.3: Intermediate Dataset Selection

Based on the above I further limit my choices to the following top
contenders:

1.  cancer\_sample

2.  

## Task 1.4: Final Dataset Selection

In order to make the concluding dataset choice, it is important to
consider the end result i.e. the associated research question. This will
help gauge the project that is most appealing. Following are my research
questions:

1.  cancer\_sample
