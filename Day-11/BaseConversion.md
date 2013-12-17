State: the integer and a output array of character strings, initially empty.
Loop state update:
Let r be the remainder when dividing Z by b. (%%)
Tack a character string representing r onto the end of the output array.
Subtract r from Z, then divide by b to create a new value for Z
Loop termination: If the integer Z is 0, you're done.
Output: the array of character strings.


```r
toBase <- function(z, b) {
    d <- c()
    repeat {
        list <- c()
        r <- z%%b
        d <- c(d, r)
        z <- (z - r)/b
        if (z == 0) 
            break
    }
    rev(d)
}
toBase(z = 10, b = 2)
```

```
## [1] 1 0 1 0
```

```r
toBase(z = 100, b = 3)
```

```
## [1] 1 0 2 0 1
```

```r
toBase(z = 1000, b = 16)
```

```
## [1]  3 14  8
```

```r

base2Numeric <- function(n, b) {
    # To use this function you need to have the number as a vector with each
    # digit seperated by a comma
    a <- 1
    c <- 0
    e <- 0
    f <- 0
    q <- rev(n)
    h <- length(n)
    repeat {
        d <- q[a] * b^(c)
        e <- e + d
        c <- c + 1
        a <- a + 1
        f <- f + 1
        if (f == h) 
            break
        
    }
    e
}
q <- c(2, 1, 2)
p <- c(3, 2, 1)
base2Numeric(q, 3)
```

```
## [1] 23
```

```r
base2Numeric(p, 4)
```

```
## [1] 57
```

