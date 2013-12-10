


```r
plot(5, 5, "n", xlim = c(0, 100), ylim = c(0, 100), xaxt = "n", yaxt = "n", 
    xlab = "string", ylab = "string", asp = 1, byt = "n")
```

```
## Warning: "byt" is not a graphical parameter Warning: "byt" is not a
## graphical parameter Warning: "byt" is not a graphical parameter Warning:
## "byt" is not a graphical parameter Warning: "byt" is not a graphical
## parameter Warning: "byt" is not a graphical parameter
```

```r
polygon(c(20, 20, 40, 40), c(40, 60, 60, 40), density = 70, border = "blue", 
    col = "green")
polygon(c(30, 30, 40, 40), c(10, 20, 20, 10), density = 70, border = "black", 
    col = "red")
polygon(c(70, 65, 80, 95, 90), c(45, 60, 75, 60, 45), density = 100, border = "white", 
    col = "yellow")
symbols(50, 50, circle = 20, bg = "blue", add = TRUE)
polygon(c(10, 30, 50, 30), c(65, 90, 65, 40), density = 70, border = "white", 
    col = "pink")
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 

