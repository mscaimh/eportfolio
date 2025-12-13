## Scalar

Only has a magnitude - Distance, speed

## Vector

Has a magnitude (size) and a direction - Displacement, velocity

An object containing elements of the **same datatype**

`vec1 <- c(5,2,3,7,8,9,1,4,10,15)`

Extracting subset from a vector:
```
> subset(vec1, vec1 > 5)
[1] 5 7 8 9 10 15
```
Random sampling from a vectos
```
> sample(vec1, 5)
[1] 9 2 4 8 7
```

[Operators](img/operators.png)

## Matrix

Collection of elements belonging to the **same datatype**

To create a matrix, first create a vector and then convert using the command `table <- matrix(data, nrow = 4, ncol = 8)`

`table [4,5]` - retrieve value at row 4 and column 5

`cell<- which( table == 10, arr.ind = TRUE)` - find location of the cell that contains the value `10`

## List

Allows for a combination of **different datatypes** in one object

```
> a1 <- c(1, 2, 3, 4)
> a2 <- c("a", "b", "c", "d")
> a3 <- c(TRUE, FALSE, TRUE, FALSE)
>
> lst1 = list(a1, a2, a3)
```

## Data frame

Data frames are a special case of list.

```
> rollno <- c(1, 2, 3, 4)
> mathsmarks <- c(80, 65, 50, 73)
> englishmarks <- c(90, 70, 54, 61)
>
> students <- data.frame(rollno, mathsmarks, englishmarks)
>
> print(students)

    rollno  mathsmarks  englishmarks
1        1          80            90
2        2          65            70
3        3          50            54
4        4          73            61
```

## Factor

To create a factor, need to first create a vector and then transform

```
> vec1 <- c(1, 2, 2, 1, 1, 2, 1, 2, 1, 2)
> fac1 <- factor(vec1)
```

## Arrays

Arrays are same as matrices, but can store data in **more than two dimensions**

```
> vec1 <- c(2, 3, 4, 1, 2, 3, 7, 8, 9, 5, 6, 7, 1, 4, 5)

> arr1 <- array(vec1, dim = c(2,3,2))
```
