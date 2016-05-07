# R
R is a language and environment for statistical computing and graphics. R provides a wide variety of statistical (linear and nonlinear modelling, classical statistical tests, time-series analysis, classification, clustering, …) and graphical techniques, and is highly extensible. The S language is often the vehicle of choice for research in statistical methodology, and R provides an Open Source route to participation in that activity. [Source](https://www.r-project.org/about.html)

### Expressions
```
> 1+1
[1] 2

> "Hello"
[1] "Hello"

> 6*7
[1] 42

> 3 < 3
[1] TRUE
```

### Variables
```
> x <- 42
> x / 2
[1] 21

> x
[1] 21
```

### Functions
```
> sum (1, 3, 5)
[1] 9

> rep ("Hi", times = 3)
[1] "Hi" "Hi" "Hi"

> sqrt(16)
[1] 4
```

### Help
```
> help (sum)
...

> example(sum)
...
```

### Listing Files
```
> list.files()
[1] "a.csv" "b.csv"
```

### Executing Source Files
```
> source("file.R")
```

### Vectors
Use c for combine.
```
> c(1, 4, 7)
[1] 1 4 7

> c(1, TRUE, "three")
[1] "1" "TRUE" "three"

All items converted to single mode (characters) so that the vector can hold them all.
```

### Sequences
```
> 5:9
[1] 5 6 7 8 9

> seq(9, 5)
[1] 9 8 7 6 5

> seq(0, 6, 2)
[1] 0, 2, 4, 6
```

### Vector Access
```
> sentence <- c("This", "old", "house")
> sentence[1]
[1] "This"
> sentence[1:2]
[1] "This" "old"
> sentence[4] <- "smells"              # adds entry onto end
> sentence[2:3] <- c("new", "garage")
```

### Vector Names
```
> ranks <- 1:3
> names(ranks) <- c("first", "second", "third")
> ranks["third"]
[1] 3
> ranks["second"] <- 5
```

### Plotting
```
> barplot(vector)

If names are used for items, will include these.

> barplot(1:100)
```

### Vector Maths
```
> a <- c(1, 2, 3)
> a + 1
[1] 2 3 4

> b <- c(4, 5, 6)
> a + b
[1] 5 7 9

> a - b
[1] -3 -3 -3

> a == c(1, 99, 3)
[1]  TRUE FALSE  TRUE

> a < b
[1] TRUE TRUE TRUE

> sqrt(a)
[1] 1.000000 1.414214 1.732051
```

### Scatter Plots
```
> x <- seq(1, 20, 0.1)
> y <- sin(x)
> plot(x,y)
```

### NA Values
```
> a <- c(1, 3, NA, 7, 9)
> sum(a)
[1] NA

> sum(a, na.rm = TRUE)
[1] 20
```

