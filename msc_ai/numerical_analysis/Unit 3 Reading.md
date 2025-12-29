## Promoting Open Science Through Research Data Management

Borghi, J. and Gulick, A. van (2022) “Promoting Open Science Through Research Data Management,” *Harvard Data Science Review*, 4(3). Available at: https://doi.org/10.1162/99608F92.9497F68E.

FAIR principle - Findable, Accessible, Interoperable, Reusable

## Intro to R and RStudio for Genomics

*Intro to R and RStudio for Genomics* (no date). Available at: https://edcarp.github.io/genomics-r-intro/01-introduction/index.html (Accessed: December 26, 2025).

`setwd("working-dir")` - Set working directory

`help.search("text")` - Wider search for help regarding text

`rm(objectname)` - Removes the object from memory

In R, every object has two properties:
* Length: How many distinct values are held in that object
* Mode: What is the classification (type) of that object

### Vector operations

`vector <- vector[-6]` - Removes 6th value from the vector

`vector[vector > 10]` - Returns all values greater than 10. Supports <, <=, >, >=, ==, !=, !x, a | b, a & b

`which(vector > 10)` - Index of the value > 10

`is.na(vector)` - Search if any columns contain NA, returns `[FALS, FALSE, TRUE, FALSE]`

`c("value1","value2") %in% vector` - Find if specified values match content of the vector, returns `[FALSE, TRUE]`

### Factors and data frames

`summary(dataframe)` and `str(dataframe)`

**Factors** can be thought of as vectors specialised for categorically data.

Items in a factor are called **levels**, represents different categories containes in the factor. Levels are assigned in **alphabetical order**.

`as.numeric(...)` - coerce values to numeric. Where not compatible, `NA` is introduced.

Implicit and explicit coercion

When using `read.table()` function from base R, make sure to set `StringAsFactors = FALSE`. Readr packages `read_csv()` doesn't do this

`colnames(dataframe)[colunames(dataframe) == "oldcolname"] <- "newcolname"` - Renames column

### dplyr and tidyr

The `tidyverse` package is an "umbrella-package" that installs `tidyr`, `dplyr`, and several other packages useful for data analysis, such as `ggplot2`, `tibble`, etc.
* `dplyr` is a package for making tabular data manipulation easier
* `tidyr` enables converting between different data formats for plotting and analysis

#### dplyr

`select()` - Subset columns (`select(dataframe, SAMPLEID, DP)` selects SAMPLEID and DP columns and `select(dataframe, -CHROM)` selects all columns minus the CHROM column)

`filter()` - Subset rows on conditions (`filter(dataframe, SAMPLEID == "SRR2584863")` filters all rows where `SAMPLEID` is `"SRR2584863"`)

`mutate()` - Create new columns by using information from other columns (`mutate(DEC = QUAL/10)` creates anew column `DEC` based on existing `QUAL` column)

`group_by()` and `summarize()` - Create summary statistics on grouped data (`dataframe %>% group_by(sample_id) %>% summarize(n_observations = n())` groups rows based on `sample_id` value and derives count using the `n()` function under a new `n_observations` column)

`count()` - Count discrete values

`dataframe <- as_tibble(dataframe)` - Converts into a friendlier `tibble` format

**Pipes** in R look like `%>%` and are made available via the `magrittr` package, which is installed as part of `dplyr`
```
dataframe %>%
  filter(SAMPLEID == "SRR2584863") %>%
  select(SAMPLEID, DP)
```

**split-apply-combine** paradigm - split the data into groups, apply some analysis to each group, and then combine the results
