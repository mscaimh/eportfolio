## Scalar

Only has a magnitude - Distance, speed

## Vector

Has a magnitude (size) and a direction - Displacement, velocity

An object containing elements of the **same datatype**

`vec1 <- c(5,2,3,7,8,9,1,4,10,15)`

Extracting subset from a vector:
```
>subset(vec1, vec1 > 5)
[1] 5 7 8 9 10 15
```
Random sampling from a vectos
```
>sample(vec1, 5)
[1] 9 2 4 8 7
```

[Operators](img/operators.png)

## Matrix

Collection of elements belonging to the **same datatype**

To create a matrix, first create a vector and then convert using the command `table <- matrix(data, nrow = 4, ncol = 8)`

`table [4,5]` - retrieve value at row 4 and column 5

`cell<- which( table == 10, arr.ind = TRUE)` - find location of the cell that contains the value `10`

## List
