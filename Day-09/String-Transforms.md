
```r
a <- c("a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", 
    "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z")
b <- c(1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 
    21, 22, 23)
c <- c("sam", "nick")
Reverser <- function(x) {
    s <- strsplit(x, split = character(0))
    d <- s[[1]][nchar(x):1]
    return(paste(d, collapse = ""))
}
Reverser2 <- function(x) {
    sapply(x, Reverser)
}
Reverser("sam")
```

```
## [1] "mas"
```

```r
Reverser2(c)
```

```
##    sam   nick 
##  "mas" "kcin"
```

```r

Scrambler <- function(x) {
    s <- strsplit(x, split = character(0))
    d <- s[[1]]
    return(sample(d))
}
Scrambler2 <- function(x) {
    sapply(x, Scrambler)
}
Scrambler("abcde")
```

```
## [1] "e" "b" "a" "d" "c"
```

```r
Scrambler2(c)
```

```
## $sam
## [1] "a" "m" "s"
## 
## $nick
## [1] "k" "c" "i" "n"
```

```r



VowelBleeper <- function(x) {
    chartr("aeiou", "*****", x)
}
VowelBleeper2 <- function(x) {
    sapply(x, VowelBleeper)
}

VowelBleeper("same")
```

```
## [1] "s*m*"
```

```r
VowelBleeper(c)
```

```
## [1] "s*m"  "n*ck"
```

```r
L33t <- function(x) {
    chartr("IElOhSb", "1310456", x)
}
L33t2 <- function(x) {
    sapply(x, L33t)
}
L33t("hElp")
```

```
## [1] "431p"
```

```r
L33t2(c)
```

```
##    sam   nick 
##  "sam" "nick"
```

```r

```

