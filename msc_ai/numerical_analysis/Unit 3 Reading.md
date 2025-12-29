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

### ggplot2

`ggplot(data = <DATA>, mapping = aes(<MAPPINGS>)) +  <GEOM_FUNCTION>()`

`ggplot(data = dataframe, aes(x = POS, y = DP))` - Plots with `POS` column as x-axis and `DP` column as y-axis

`geom_point()` for scatter plots, dot plots, etc.
`geom_boxplot()` for, well, boxplots!
`geom_line()` for trend lines, time series, etc.

The + sign used to add new layers must be placed at the end of the line containing the *previous* layer. This is because R assumes that the end of a line is the end of a command, unless you tell it otherwise. So, if the + sign is added at the beginning of the next line containing the new layer, `ggplot2` will not add that new layer and will return an error message.

`labs(x = "Base Pair Position", y = "Read Depth (DP)")` - Adds descriptions

`scale_y_log10()` - Uses log10 scale for y-axis

`facet_grid(. ~ sample_id)` - Enables *faceting* - split one plot into multiple plots based on a factor included in the dataset; uses format `rows ~ columns` and a `.` can be used as placeholder for either `rows` or `columns` value.

`theme_bw()` - Sets theme, in this case setting background to white. The complete list of themes is available at https://ggplot2.tidyverse.org/reference/ggtheme.html. `theme_minimal()` and `theme_light()` are popular, and `theme_void()` can be useful as a starting point to create a new hand-crafted theme.

The different stages can be combined like:
```
ggplot(data = variants, aes(x = POS, y = MQ, color = sample_id)) +
  geom_point() +
  labs(x = "Base Pair Position",
       y = "Mapping Quality (MQ)") +
  facet_grid(sample_id ~ .) +
  theme_bw() +
  theme(panel.grid = element_blank())
```

### knitr

`knitr` allows creating a document that is a mixture of text and some chunks of code. When the document is processed by `knitr`, chunks of R code will be executed, and graphs or other results inserted.
