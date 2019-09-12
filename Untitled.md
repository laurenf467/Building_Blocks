new\_repository
================

I’m an R Markdown document\!

# Section 1

Here’s a **code chunk** that samples from a *normal
    distribution*:

``` r
library(tidyverse)
```

    ## ── Attaching packages ──────────────────────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 3.2.1     ✔ purrr   0.3.2
    ## ✔ tibble  2.1.3     ✔ dplyr   0.8.3
    ## ✔ tidyr   0.8.3     ✔ stringr 1.4.0
    ## ✔ readr   1.3.1     ✔ forcats 0.4.0

    ## ── Conflicts ─────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
samp = rnorm(100)
length(samp)
```

    ## [1] 100

``` r
plot_df = tibble(
  x = rnorm(100),
  y = 1 + 2 ^ x + rnorm(100)
)

z = 1
```

# Section 2

I can take the mean of the sample, too\! The mean is 0.039569. - this
allows you to execute small pieces of R in the comments section The
number of rows in `plot_df` is 100

  - See class notes for all additions to ’’’{r …} you can add to change
    up the code chunks
  - You can name the code chunks, helpful way to determine where issues
    are coming from
  - Hot key for adding rmd chunk command-option-i

<!-- end list -->

``` r
mean(samp)
```

Learning Assessment 1

``` r
df = tibble(
  a = rnorm(500, mean = 1),
  b = a > 0,
  c = abs(a)
)

ggplot(df, aes(c)) + geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](Untitled_files/figure-gfm/learning_assessment-1.png)<!-- -->

The median of the sample from the dataframe `df` is 0.98.

Formatting Text

## Text formatting

*italic* or *italic* **bold** or **bold** `code` superscript<sup>2</sup>
and subscript<sub>2</sub>

## Headings

# 1st Level Header

## 2nd Level Header

### 3rd Level Header

## Lists

  - Bulleted list item 1

  - Item 2
    
      - Item 2a
    
      - Item 2b

<!-- end list -->

1.  Numbered list item 1

2.  Item 2. The numbers are incremented automatically in the output.

## Tables

| First Header | Second Header |
| ------------ | ------------- |
| Content Cell | Content Cell  |
| Content Cell | Content Cell  |

YAML and Output Formats
