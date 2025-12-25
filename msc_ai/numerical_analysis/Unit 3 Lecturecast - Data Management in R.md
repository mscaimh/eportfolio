R can be used to open CSV (.csv), text files (.txt), table files (.tbl), excel files (.xlsx), STATA (.dta), SPSS (.sav), SAS (.sas)

R's internal data format is .Rdata

`read.<filetype>("filename")` - Read file

`view(dataset)` - View data details

`names(dataset)` - Variable names within the dataset

`str(dataset)` - Structure of variables within the dataset

`class(dataset$column)` - Type of specific column

`head(dataset)` - First few rows

`summary(dataset)` - Statistical summary (min, max, mean, median, 1st quartile and 3rd quartile)

`dataset$column <- as.integer(dataset$column)` - Changing datatype of a column
