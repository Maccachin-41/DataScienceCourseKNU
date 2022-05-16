# Лабораторна робота №1

## 1. Створити змінні базових (atomic) типів. Базові типи: character, numeric, integer, complex, logical.

```{R}
x <- 49
class(x)
[1] "numeric"

y <- 6L
class(y)
[1] "integer"

z <- FALSE
class(z)
[1] "logical"

p <- "baba"
class(p)
[1] "character"

w <- 15-3i
class(w)
[1] "complex"
```
## 2. Створити вектори, які: містить послідовність з 5 до 75;

```{R}
z <- 5:75
z
 [1]  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29
[26] 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54
[51] 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75
```
## містить числа 3.14, 2.71, 0, 13; 
```{R}
q <- c(3.14, 2.71, 0, 13)
q
[1]  3.14  2.71  0.00 13.00
```
## 100 значень TRUE.
```{R}
y <- rep(TRUE, 100)
y
  [1] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [17] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [33] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [49] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [65] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [81] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [97] TRUE TRUE TRUE TRUE
```
## 3. Створити наступну матрицю за допомогою matrix, та за допомогою cbind або rbind.
```{R}
m <- matrix(c(0.5, 3.9, 0, 2, 1.3, 131, 2.2, 7, 3.5, 2.8, 4.6, 5.1), nrow = 4, ncol = 3)
m
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1


x <- c(0.5, 3.9, 0, 2)
y <- c(1.3, 131, 2.2, 7)
z <- c(3.5, 2.8, 4.6, 5.1)
cbind(x,y,z)
       x     y   z
[1,] 0.5   1.3 3.5
[2,] 3.9 131.0 2.8
[3,] 0.0   2.2 4.6
[4,] 2.0   7.0 5.1
```
## 4. Створити довільний список (list), в який включити всі базові типи.
```{R}
list(6, "boo", TRUE, 4 + 3i, 2L)
[[1]]
[1] 6

[[2]]
[1] "boo"

[[3]]
[1] TRUE

[[4]]
[1] 4+3i

[[5]]
[1] 2
```
## 5. Створити фактор з трьома рівнями «baby», «child», «adult».
```{R}
x <- factor(c("baby", "baby", "child", "adult"))
x
[1] baby  baby  child adult
Levels: adult baby child
```
## 6. Знайти індекс першого значення NA в векторі 1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11.
```{R}
o <- c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11)
match(NA, o)
[1] 5
```
## Знайти кількість значень NA.
```{R}
sum(is.na(o))
[1] 3
```

## 7. Створити довільний data frame та вивести в консоль.
```{R}
x <- data.frame (student = 1:6, name = c("Kate", "Nick", "Charlie", "Samantha", "Rocky", "Jin"), status = c(T, F, F, T, T, F))
x
  student     name status
1       1     Kate   TRUE
2       2     Nick  FALSE
3       3  Charlie  FALSE
4       4 Samantha   TRUE
5       5    Rocky   TRUE
6       6      Jin  FALSE
```

## 8. Змінити імена стовпців цього data frame.
```{R}
colnames(x) <- c("id", "who", "student")
x
  id      who student
1  1     Kate    TRUE
2  2     Nick   FALSE
3  3  Charlie   FALSE
4  4 Samantha    TRUE
5  5    Rocky    TRUE
6  6      Jin   FALSE
```




