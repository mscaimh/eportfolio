## Task 1.1: Basic Dataset Information

How many total variables (columns) are in this dataset?
```
> ncol(df)
[1] 7
```

How many total observations (rows) are in this dataset?
```
> nrow(df)
[1] 270
```

What are the names of all variables in the dataset?
```
> names(df)
[1] "Sno"                      "Date"                     "State.UnionTerritory"    
[4] "ConfirmedIndianNational"  "ConfirmedForeignNational" "Cured"                   
[7] "Deaths"
```

How many variables are in numeric format?

```
5 (including Sno)
````

How many variables are in character/text format?

```
1 (excluding Date)
```

How many variables are in date format?
```
1
```

```
> class(df$Sno)
[1] "integer"
> 
> class(df$Date)
[1] "character"
> 
> class(df$State.UnionTerritory)
[1] "character"
> 
> class(df$ConfirmedIndianNational)
[1] "integer"
> 
> class(df$ConfirmedForeignNational)
[1] "integer"
> 
> class(df$Cured)
[1] "integer"
> 
> class(df$Deaths)
[1] "integer"
```

## Task 1.2 Data Related information

How many unique states/union territories are represented in the dataset?
```
> length(unique(df$State.UnionTerritory))
[1] 27
```

What is the date range covered by this dataset?
```
> cd <- as.ts(df$Date)
> 
> range(cd)
[1] "01-02-2020" "31-01-2020"
```

Which state appears most frequently in the dataset?
```
> names(which.max(table(df$State.UnionTerritory)))
[1] "Kerala"
> 
> which.max(table(df$State.UnionTerritory))
Kerala 
    11 
```
