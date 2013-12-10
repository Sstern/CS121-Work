
```r

outlier <- function(x) {
    
    ifelse(x < (quantile(x, 0.25) - ((quantile(x, 0.75) - quantile(x, 0.25)) * 
        1.5)), x, ifelse(x > (quantile(x, 0.75) + ((quantile(x, 0.75) - quantile(x, 
        0.25)) * 1.5)), x, "Not an Outlier"))
    
    
}


w <- c(5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 
    5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 
    5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 5, 
    5, 5, 5, -1000, 1000)

outlier(w)
```

```
##  [1] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
##  [5] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
##  [9] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [13] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [17] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [21] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [25] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [29] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [33] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [37] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [41] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [45] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [49] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [53] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [57] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [61] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [65] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [69] "Not an Outlier" "Not an Outlier" "Not an Outlier" "Not an Outlier"
## [73] "Not an Outlier" "Not an Outlier" "-1000"          "1000"
```







```r
digitToWord <- function(x) {
    ifelse(x == "1", "one", ifelse(x == "2", "two", ifelse(x == "3", "three", 
        ifelse(x == "4", "four", ifelse(x == "5", "five", ifelse(x == "6", "six", 
            ifelse(x == "7", "seven", ifelse(x == "8", "eight", ifelse(x == 
                "9", "nine", "Needs to be between 0 and 10")))))))))
}

digitToWord(1)
```

```
## [1] "one"
```

```r
digitToWord(2)
```

```
## [1] "two"
```

```r

digitToWord(9)
```

```
## [1] "nine"
```

```r
digitToWord(11)
```

```
## [1] "Needs to be between 0 and 10"
```



```r
digitToWord2 <- function(language, number) {
    if (language == "english") {
        if (number == "0") {
            print("zero")
        }
        if (number == "1") {
            print("one")
        }
        if (number == "2") {
            print("two")
        }
        if (number == "3") {
            print("three")
        }
        if (number == "4") {
            print("four")
        }
        if (number == "5") {
            print("five")
        }
        if (number == "6") {
            print("six")
        }
        if (number == "7") {
            print("seven")
        }
        if (number == "8") {
            print("eight")
        }
        if (number == "9") {
            print("nine")
        }
    }
    if (language == "spanish") {
        if (number == "0") {
            print("cero")
        }
        if (number == "1") {
            print("uno")
        }
        if (number == "2") {
            print("dos")
        }
        if (number == "3") {
            print("tres")
        }
        if (number == "4") {
            print("cuatro")
        }
        if (number == "5") {
            print("cinco")
        }
        if (number == "6") {
            print("seis")
        }
        if (number == "7") {
            print("siete")
        }
        if (number == "8") {
            print("ocho")
        }
        if (number == "9") {
            print("nueve")
        }
    }
    if (language == "french") {
        if (number == "0") {
            print("zero")
        }
        if (number == "1") {
            print("un")
        }
        if (number == "2") {
            print("deux")
        }
        if (number == "3") {
            print("trois")
        }
        if (number == "4") {
            print("quartre")
        }
        if (number == "5") {
            print("cinq")
        }
        if (number == "6") {
            print("six")
        }
        if (number == "7") {
            print("sept")
        }
        if (number == "8") {
            print("huit")
        }
        if (number == "9") {
            print("neuf")
        }
    }
}

digitToWord2("english", "2")
```

```
## [1] "two"
```

```r
digitToWord2("spanish", "5")
```

```
## [1] "cinco"
```

```r
digitToWord2("french", "7")
```

```
## [1] "sept"
```



```r
lettersMatch <- function(x, y) {
    grepl(x, y)
}
q <- c("word", "names", "twelve", "wonder", "hungry", "slow", "am", "find", 
    "eighteen", "search")
lettersMatch("^...$", q)
```

```
##  [1] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
```

```r
grepl("^....$", q)
```

```
##  [1]  TRUE FALSE FALSE FALSE FALSE  TRUE FALSE  TRUE FALSE FALSE
```



```r
lettersMatch2 <- function(words, pattern) {
    list <- grepl(pattern, words)
    return(list)
}
q <- c("word", "names", "twelve", "wonder", "hungry", "slow", "am", "find", 
    "eighteen", "search")
lettersMatch2(q, "^....$")
```

```
##  [1]  TRUE FALSE FALSE FALSE FALSE  TRUE FALSE  TRUE FALSE FALSE
```




```r
piSeries <- function(n) {
    return(4 * (sum(((1/(((((1:n) - 1) * 2) + 1))) * (-1)^((1:n) - 1)))))
}
piSeries(5)
```

```
## [1] 3.34
```

```r
piSeries(10)
```

```
## [1] 3.042
```

```r
piSeries(1e+05)
```

```
## [1] 3.142
```

```r
howCloseToPi <- function(n) {
    plot((4 * (cumsum(((1/(((((1:n) - 1) * 2) + 1))) * (-1)^((1:n) - 1))))))
}
howCloseToPi(1000)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-71.png) 

```r



randomApproxToPi <- function(n) {
    x <- runif(100)
    y <- runif(100)
    q <- (x^2) + (y^2)
    plot(sapply(q, howCloseToPi))
}

randomApproxToPi(10)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-72.png) 

```
## Error: 'x' is a list, but does not have components 'x' and 'y'
```




```r
randomApproxToPi2 <- function(n) {
    sapply(10^runif(100, min = 2, max = 6), howCloseToPi)
}
sapply(10^runif(1, min = 2, max = 6), howCloseToPi)
```

![plot of chunk unnamed-chunk-8](figure/unnamed-chunk-8.png) 

```
## [[1]]
## NULL
```

 plot(((x^2)+(y^2)))
