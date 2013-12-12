
```r
require(mosaic)
```

```
## Loading required package: mosaic Loading required package: grid Loading
## required package: lattice
## 
## Attaching package: 'mosaic'
## 
## The following objects are masked from 'package:stats':
## 
## D, IQR, binom.test, cor, cov, fivenum, median, prop.test, sd, t.test, var
## 
## The following object is masked from 'package:base':
## 
## max, mean, min, print, prod, range, sample, sum
```

```r
fetchData("COMP121/word-hints.R")
```

```
## Retrieving from http://www.mosaic-web.org/go/datasets/COMP121/word-hints.R
```

```
## [1] TRUE
```

```r
res <- letterProportionHint(phraseOne)
languages <- list(English, German, Finnish, French, Italian, Spanish)
letterProportion <- function(string) {
    a <- tolower(string)
    b <- unlist(strsplit(a, split = ""))
    c <- table(b)
    d <- (c[1:sum(c)]/sum(c))
    return(c(unlist(d)))
}

res
```

```
## 9
##               .       b       c       d       e       h       i       k 
## 0.12903 0.03226 0.06452 0.03226 0.06452 0.25806 0.03226 0.06452 0.03226 
##       l       n       o       r       v 
## 0.03226 0.06452 0.03226 0.09677 0.06452
```

```r
letterProportion(phraseOne)
```

```
##               .       b       c       d       e       h       i       k 
## 0.12903 0.03226 0.06452 0.03226 0.06452 0.25806 0.03226 0.06452 0.03226 
##       l       n       o       r       v    <NA>    <NA>    <NA>    <NA> 
## 0.03226 0.06452 0.03226 0.09677 0.06452      NA      NA      NA      NA 
##    <NA>    <NA>    <NA>    <NA>    <NA>    <NA>    <NA>    <NA>    <NA> 
##      NA      NA      NA      NA      NA      NA      NA      NA      NA 
##    <NA>    <NA>    <NA>    <NA> 
##      NA      NA      NA      NA
```

```r
step1 <- letterProportion(phraseTwo)

freqCompare <- function(x, y) {
    t <- 0
    d <- 0
    a <- 0
    e <- 0
    b <- names(letterProportionHint(x))
    c <- names(y)
    repeat {
        if (b[e] == c[1]) {
            a <- (((x[e] - y[1])^2)/y[1])
            
            
        }
        if (b[e] == c[2]) {
            a <- (((x[e] - y[2])^2)/y[2])
            
        }
        if (b[e] == c[3]) {
            a <- (((x[e] - y[3])^2)/y[3])
            
        }
        if (b[e] == c[4]) {
            a <- (((x[e] - y[4])^2)/y[4])
            
        }
        if (b[e] == c[5]) {
            a <- (((x[e] - y[5])^2)/y[5])
            
        }
        if (b[e] == c[6]) {
            a <- (((x[e] - y[6])^2)/y[6])
            
        }
        if (b[e] == c[7]) {
            a <- (((x[e] - y[7])^2)/y[7])
            
        }
        if (b[e] == c[8]) {
            a <- (((x[e] - y[8])^2)/y[8])
            
        }
        if (b[e] == c[9]) {
            a <- (((x[e] - y[9])^2)/y[9])
            
        }
        
        e <- a + e
        
        t <- t + 1
        if (t == 10000) 
            break
    }
    return(e)
}

freqCompareHint(res, English)
```

```
##      e 
## 0.2067
```

```r
freqCompare(res, English)
```

```
## Error: argument is of length zero
```

```r

whichLanguage <- function(x) {
    a <- freqCompareHint(letterProportionHint(x), English)
    b <- freqCompareHint(letterProportionHint(x), German)
    c <- freqCompareHint(letterProportionHint(x), Finnish)
    d <- freqCompareHint(letterProportionHint(x), French)
    e <- freqCompareHint(letterProportionHint(x), Italian)
    f <- freqCompareHint(letterProportionHint(x), Spanish)
    g <- c(a, b, c, d, e, f)
    h <- which.min(g)
    h
    
}
# A response of e2 means German, e1 means English,a3 is Finish, e4 is
# French, e5 is Italian, e6 is Spanish
whichLanguageHint(phraseOne)
```

```
## [1] "German"
```

```r
whichLanguageHint(phraseTwo)
```

```
## [1] "English"
```

```r
whichLanguage(phraseOne)
```

```
## e 
## 2
```

```r
whichLanguage(phraseTwo)
```

```
## e 
## 1
```

```r
whichLanguage(phraseThree)
```

```
## a 
## 3
```

```r
whichLanguage(phraseFour)
```

```
## e 
## 1
```

```r
whichLanguage(phraseFive)
```

```
## e 
## 6
```
