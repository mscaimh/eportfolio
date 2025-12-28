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
