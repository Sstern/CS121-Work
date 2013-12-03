
```r

countOdds <- function(x) {
    sum(x%%2)
    
}

countOdds(1:9)
```

```
## [1] 5
```



```r
countEvens <- function(x) sum((x + 1)%%2)

countEvens(1:9)
```

```
## [1] 4
```



```r

hypotenusLength <- function(x, y) {
    
    return((x^2) + (y^2))
    
}

hypotenusLength(3, 4)
```

```
## [1] 25
```



```r
lawofCosines <- function(a, b, t) {
    return(((a^2) + (b^2) - (2 * a * b * cos(t)))^0.5)
}
lawofCosines(13, 84, pi/2)
```

```
## [1] 85
```

```r
lawofCosines(13, 84, 0)
```

```
## [1] 71
```

```r
lawofCosines(5, 5, pi/3)
```

```
## [1] 5
```



```r
thetafromLengths <- function(i, o, p) {
    return(acos(((p^2) - (i^2) - (o^2))/(-2 * i * o)))
}
thetafromLengths(3, 4, 5)
```

```
## [1] 1.571
```



```r
canvas <- function(x, y) {
    return(plot(x:y))
}

canvas(1, 10)

drawCircle <- function(x, y, z, a) {
    border = NULL
    
    symbols(x, y, circle = z, add = TRUE, bg = a)
}
drawCircle(5, 5, 3, "yellow")
drawCircle(3, 3, 3, "red")
drawCircle(2, 3, 3, "blue")
```

![plot of chunk unnamed-chunk-6](figure/unnamed-chunk-6.png) 

```r
drawCircle2 <- function(x, y, z, b, a, ...) {
    border = NULL
    
    symbols(x, y, circles = z, add = TRUE, fg = b, bg = a, ...)
}

```



```r
h <- c(12)
canvas(1, 10)
drawCircle2(2, 5, h, "blue", NULL)
drawCircle2(3, 5, 0.5, "black", NULL)
drawCircle2(4, 5, 0.5, "red", NULL)
drawCircle2(2.5, 4, 0.5, "yellow", NULL)
drawCircle2(3.5, 4, 10, "green", NULL)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7.png) 

```r

```

