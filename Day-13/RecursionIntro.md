
```r

addNSeq <- function(n) {
    
    # test if the answer is simple.  If so, return the simple answer.  YOUR TEST
    # GOES HERE
    repeat {
        a <- (n - 1)
        q <- n + a
        n <- a
        if (a == 0) 
            break
    }
    return(q)
    # Simplify the problem and assemble the answer from the parts.  Your answer
    # here return( something involving addNSeq(simpler) )
}
addNSeq(4)
```

```
## [1] 1
```

```r
addNSeq(2)
```

```
## [1] 1
```
