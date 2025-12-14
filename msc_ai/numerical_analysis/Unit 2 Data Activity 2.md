```
> df <- read.csv("C:/Users/mahah/RStudio/Covid19 India (Jan 20 - Mar 20).csv", header=TRUE)
```

## Create a frequency table to count how many daily reports showed recoveries versus no recoveries during this period. Use the table() command.

```
> table(df$Cured)

  0   1   2   3   4   5   9 
215  14   4  27   2   5   3 
```

## Calculate percentages to understand what proportion of daily state reports included recovery cases.

```
> sum(1*14, 2*4, 3*27, 4*2, 5*5, 9*3)
[1] 163
>
> sum(df[df$Cured > 0,]$Cured)
[1] 163
```

## Create a binary variable called has_recovery that indicates whether any recoveries (cured cases) were reported.

```
> df$has_recovery <- df$Cured > 0
```
