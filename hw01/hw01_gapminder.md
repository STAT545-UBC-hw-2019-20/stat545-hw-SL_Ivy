Exercise 2: R Markdown for Gapminder exploration
================
Ivy Li

  - [About the “gapminder”](#about-the-gapminder)
  - [Useful Functions for Exploring Data
    Frames](#useful-functions-for-exploring-data-frames)

## About the “gapminder”

`gapminder` is a package created for the purpose of teaching and making
code examples. It excerpt from the [Gapminder
data](https://www.gapminder.org/data/). The main object in this package
is the `gapminder` data frame.

To explore the data, the `gapminder` package need to be loaded by runing
the code below:

``` {r}
library(gapminder)
```

## Useful Functions for Exploring Data Frames

  - Use `nrow()` and `ncol()` to get the number of rows and number of
    columns, respectively. This could give you a general picture of the
    size of the data frame.

<!-- end list -->

``` {r,collapse=true}
nrow(gapminder) # show the number of rows
ncol(gapminder) # show the number of columns
```

  - `str` is a diagnostic function that compactly display the internal
    structure of an R object. It returns many useful pieces of
    information, including the number of observations, varaiables, and
    the types of data for each column.

<!-- end list -->

``` {r}
str(gapminder)
```

  - `summary` is a generic function used to produce result summaries of
    the results of various model fitting functions. Sometimes, it is the
    alternative option to `str`. It is essentially applied to each
    column, and the results for all columns are shown together.

<!-- end list -->

``` {r}
summary(gapminder)
```
