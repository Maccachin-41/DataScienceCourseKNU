# Лабораторна робота №3
## 1. Функція add2(x, y), яка повертає суму двох чисел.
```{R}
add2 <- function(x,y)
      {
        x+y
      }
add2(62, 456.2)
[1] 518.2
```
## 2. Функція above(x, n), яка приймає вектор та число n, та повертає всі елементі вектору, які більше n. По замовчуванню n = 10.
```{R}
above <- function(x, n=10)
       {
         x1=x[x>n]
         return(x1)
       }
above(vect <- c(1,3,15,63,10,45,7.5, 21.3))
[1] 15.0 63.0 45.0 21.3
```
## 3. Функція my_ifelse(x, exp, n), яка приймає вектор x, порівнює всі його елементи за допомогою exp з n, та повертає елементи вектору, які відповідають умові expression. Наприклад, my_ifelse(x, “>”, 0) повертає всі елементи x, які більші 0. Exp може дорівнювати “<”, “>”, “<=”, “>=”, “==”. Якщо exp не співпадає ні з одним з цих виразів, повертається вектор x.
```{R}
my_ifelse <- function(x,exp,n)
           {
             if(exp == "<"){
                x1=x[x<n]
             } else if(exp == ">"){
                x1=x[x>n]
             } else if(exp == "<="){
                x1=x[x<=n]
             } else if(exp == ">="){
                x1=x[x>=n]
             } else if(exp == "=="){
                x1=x[x==n]
             } else {
                      x1=x
                    }
             return(x1)
            }
my_ifelse(vect, ">", 10)
[1] 15.0 63.0 45.0 21.3
my_ifelse(vect, "<=", 25)
[1]  1.0  3.0 15.0 10.0  7.5 21.3
my_ifelse(vect, "==", 45)
[1] 45
my_ifelse(vect, ">=", 7)
[1] 15.0 63.0 10.0 45.0  7.5 21.3
my_ifelse(vect, "<", 36)
[1]  1.0  3.0 15.0 10.0  7.5 21.3
```
## 4. Функція columnmean(x, removeNA), яка розраховує середнє значення (mean) по кожному стовпцю матриці, або data frame. Логічний параметр removeNA вказує, чи видаляти NA значення. По замовчуванню він дорівнює TRUE.
```{R}
columnmean <- function(x, removeNA=TRUE)
            {
               apply(x, 2, mean, na.rm = removeNA)
            }
m <- matrix(c(NA,5,69,4.1,3,NA,6,4,85,41,NA,NA,36,5,6.3,1), nrow = 4, ncol = 4)
m
     [,1] [,2] [,3] [,4]
[1,]   NA    3   85 36.0
[2,]  5.0   NA   41  5.0
[3,] 69.0    6   NA  6.3
[4,]  4.1    4   NA  1.0
columnmean(m)
[1] 26.033333  4.333333 63.000000 12.075000
columnmean(m, removeNA=FALSE)
[1]     NA     NA     NA 12.075
```


