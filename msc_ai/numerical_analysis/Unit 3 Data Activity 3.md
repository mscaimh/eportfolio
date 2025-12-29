## Create a binary variable called has_deaths that indicates whether any deaths were reported:  
* Value = 1 (or TRUE) if Deaths > 0 
* Value = 0 (or FALSE) if Deaths = 0

```
> install.packages("readr")
> library(readr)
>
> df <- readr::read_csv("Covid19 India (Jan 20 - Mar 20).csv")
>
> library(dplyr)
>
> df <- dplyr::mutate(df, has_deaths = Deaths > 0)
```

## Create a frequency table using the table() command to analyze death reporting patterns.

```
> table(df$Deaths)
  0   1 
245  25 
```

## Convert to a factor variable with appropriate labels ("No Deaths", "Deaths Reported").

```
> fdeaths <- factor(df$has_deaths, labels = c("No Deaths", "Deaths Reported"))
```

## Create a categorical variable called case_level based on total confirmed cases (Indian + Foreign nationals):  
* No Cases = 0 cases 
* Low Cases = 1-5 cases 
* Medium Cases = 6-15 cases 
* High Cases = 16+ cases

```
> df <- dplyr::mutate(df, TotalConfirmed = ConfirmedIndianNational + ConfirmedForeignNational)
>
> df <- dplyr::mutate(df,
            case_level = as.factor(
                ifelse(TotalConfirmed >= 16, "High Cases",
                ifelse(TotalConfirmed >= 6, "Medium Cases",
                ifelse(TotalConfirmed >= 1, "Low Cases", "No Cases")))))
```

## Create a frequency table for the State/Union Territory variable to see which states had the most frequent reporting.

```
> table(df$`State/UnionTerritory`)
```
  
## Identify the top 10 states with the highest number of daily reports in the dataset. 

```
> df %>% group_by(`State/UnionTerritory`) %>% summarize(max_daily = max(TotalConfirmed)) %>% arrange(desc(max_daily))
# A tibble: 27 × 2
   `State/UnionTerritory` max_daily
   <chr>                      <dbl>
 1 Maharashtra                   63
 2 Kerala                        40
 3 Delhi                         26
 4 Uttar Pradesh                 24
 5 Telengana                     21
 6 Haryana                       17
 7 Rajasthan                     17
 8 Karnataka                     15
 9 Ladakh                        13
10 Punjab                        13
# ℹ 17 more rows
# ℹ Use `print(n = ...)` to see more rows
```
