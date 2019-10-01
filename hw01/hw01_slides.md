---
title: 'Exercise 2: R Markdown for Gapminder exploration'
author: "Ivy Li"
output: 
  ioslides_presentation: 
    highlight: espresso
    keep_md: yes
    smaller: yes
---

## About the "gapminder"
`gapminder` is a package created for the purpose of teaching and making code examples. It excerpt from the [Gapminder data](https://www.gapminder.org/data/).
The main object in this package is the `gapminder` data frame.

To explore the data, the `gapminder` package need to be loaded by runing the code below:


```r
library(gapminder)
```

## Useful Functions for Exploring Data Frames

* Use `nrow()` and `ncol()` to get the number of rows and number of columns, respectively. This could give you a general picture of the size of the data frame.


```r
nrow(gapminder) # show the number of rows
## [1] 1704
ncol(gapminder) # show the number of columns
## [1] 6
```


* `str` is a diagnostic function that compactly display the internal structure of an R object. It returns many useful pieces of information, including the number of observations, varaiables, and the types of data for each column. 

```r
str(gapminder)
```

```
## Classes 'tbl_df', 'tbl' and 'data.frame':	1704 obs. of  6 variables:
##  $ country  : Factor w/ 142 levels "Afghanistan",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ continent: Factor w/ 5 levels "Africa","Americas",..: 3 3 3 3 3 3 3 3 3 3 ...
##  $ year     : int  1952 1957 1962 1967 1972 1977 1982 1987 1992 1997 ...
##  $ lifeExp  : num  28.8 30.3 32 34 36.1 ...
##  $ pop      : int  8425333 9240934 10267083 11537966 13079460 14880372 12881816 13867957 16317921 22227415 ...
##  $ gdpPercap: num  779 821 853 836 740 ...
```

* `summary` is a generic function used to produce result summaries of the results of various model fitting functions. Sometimes, it is the alternative option to `str`. It is essentially applied to each column, and the results for all columns are shown together. 


```r
summary(gapminder)
```

```
##         country        continent        year         lifeExp     
##  Afghanistan:  12   Africa  :624   Min.   :1952   Min.   :23.60  
##  Albania    :  12   Americas:300   1st Qu.:1966   1st Qu.:48.20  
##  Algeria    :  12   Asia    :396   Median :1980   Median :60.71  
##  Angola     :  12   Europe  :360   Mean   :1980   Mean   :59.47  
##  Argentina  :  12   Oceania : 24   3rd Qu.:1993   3rd Qu.:70.85  
##  Australia  :  12                  Max.   :2007   Max.   :82.60  
##  (Other)    :1632                                                
##       pop              gdpPercap       
##  Min.   :6.001e+04   Min.   :   241.2  
##  1st Qu.:2.794e+06   1st Qu.:  1202.1  
##  Median :7.024e+06   Median :  3531.8  
##  Mean   :2.960e+07   Mean   :  7215.3  
##  3rd Qu.:1.959e+07   3rd Qu.:  9325.5  
##  Max.   :1.319e+09   Max.   :113523.1  
## 
```
