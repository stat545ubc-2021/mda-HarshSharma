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

## Task 1.2: Introductory Dataset Exploration

In this section, we will individually perform introductory exploration
into the four chosen datasets using dyplr to find the associated data
attributes. This will enhance the understanding about the information
contained within each dataset and enable a more informed decision.

#### Building Permits

``` r
glimpse(building_permits)
```

    ## Rows: 20,680
    ## Columns: 14
    ## $ permit_number               <chr> "BP-2016-02248", "BU468090", "DB-2016-0445~
    ## $ issue_date                  <date> 2017-02-01, 2017-02-01, 2017-02-01, 2017-~
    ## $ project_value               <dbl> 0, 0, 35000, 15000, 181178, 0, 15000, 0, 6~
    ## $ type_of_work                <chr> "Salvage and Abatement", "New Building", "~
    ## $ address                     <chr> "4378 W 9TH AVENUE, Vancouver, BC V6R 2C7"~
    ## $ project_description         <chr> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA~
    ## $ building_contractor         <chr> NA, NA, NA, "Mercury Contracting Ltd", "08~
    ## $ building_contractor_address <chr> NA, NA, NA, "88 W PENDER ST  \r\nUnit 2069~
    ## $ applicant                   <chr> "Raffaele & Associates DBA: Raffaele and A~
    ## $ applicant_address           <chr> "2642 East Hastings\r\nVancouver, BC  V5K ~
    ## $ property_use                <chr> "Dwelling Uses", "Dwelling Uses", "Dwellin~
    ## $ specific_use_category       <chr> "One-Family Dwelling", "Multiple Dwelling"~
    ## $ year                        <dbl> 2017, 2017, 2017, 2017, 2017, 2017, 2017, ~
    ## $ bi_id                       <dbl> 524, 535, 539, 541, 543, 546, 547, 548, 54~

#### Cancer Sample

#### Parking Meters

#### Vancouver Trees

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
