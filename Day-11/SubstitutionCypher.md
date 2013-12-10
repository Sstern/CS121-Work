

```r
Alpha <- c(letters, LETTERS, "", "^", "$", "!")
Key2 <- function(word) {
    word <- unlist(strsplit(word, split = NULL))
    res <- character(length(word))
    for (k in 1:length(word)) {
        res[k] <- which(word[k] == letters)
    }
    res <- paste(res, collapse = "")
    return(as.numeric(res))
}
Key2("zoo")
```

```
## [1] 261515
```

```r
Cypher <- function(word) {
    set.seed(Key2(word))
    return(sample(Alpha))
}
Cypher("zoo")
```

```
##  [1] "n" "v" "h" "S" "y" "p" "g" "z" "u" "a" "V" "N" "D" "G" "e" "i" "c"
## [18] "q" "R" "M" "Q" "O" "H" "x" "$" "P" "t" "k" "Z" ""  "f" "C" "b" "I"
## [35] "E" "w" "^" "o" "W" "J" "d" "X" "A" "B" "s" "U" "Y" "m" "F" "L" "!"
## [52] "T" "r" "K" "j" "l"
```

```r

Encryption <- function(x, y, word) {
    chartr(x, y, word)
}
Encryption("z", "Z", "zoo")
```

```
## [1] "Zoo"
```

```r
encrypte <- function(word, message) {
    Shuffled <- Cypher(word)
    New <- paste(Shuffled, collapse = "")
    Old <- paste(Alpha, collapse = "")
    return(chartr(Old, New, message))
}
encrypte("zoo", "Sam")
```

```
## [1] "UnD"
```

```r
dycrypte <- function(word, message) {
    Shuffled <- Cypher(word)
    New <- paste(Shuffled, collapse = "")
    Old <- paste(Alpha, collapse = "")
    return(chartr(New, Old, message))
}
dycrypte("zoo", "UnD")
```

```
## [1] "Sam"
```

```r

```


