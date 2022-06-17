By Rodrigo Esteves de Lima Lopes *University of Campinas* [rll307\@unicamp.br](mailto:rll307@unicamp.br)

------------------------------------------------------------------------

# R Básico

## Introdução

Neste tutorial, tentaremos estabelecer um terreno comum sobre a linguagem R e algumas convenções básicas. Por favor, execute o [script](03_basics.R) neste notebook.

# Algumas coisas bem básicas

R é uma boa ferramenta aritmética. Se digitarmos as seguintes linhas em nosso script e executarmos uma de cada vez:

``` r
1+5
```

    ## [1] 6

``` r
5-4
```

    ## [1] 1

``` r
100/33
```

    ## [1] 3.030303

``` r
5^2
```

    ## [1] 25

``` r
5**2
```

    ## [1] 25

``` r
9/4
```

    ## [1] 2.25

``` r
9*4
```

    ## [1] 36

``` r
(300 * 9) + (500 / 2)
```

    ## [1] 2950

``` r
x <- 2L
x
```

    ## [1] 2

``` r
typeof(x)
```

    ## [1] "integer"

``` r
y <- 2.5
y
```

    ## [1] 2.5

``` r
typeof(y)
```

    ## [1] "double"

``` r
z <- 3+2i
z
```

    ## [1] 3+2i

``` r
typeof(z)
```

    ## [1] "complex"

``` r
h <- "h"
typeof(h)
```

    ## [1] "character"

``` r
h
```

    ## [1] "h"

``` r
q1 <- TRUE
typeof(q1)
```

    ## [1] "logical"

``` r
q1
```

    ## [1] TRUE

``` r
q2 <- FALSE
q2
```

    ## [1] FALSE

``` r
typeof(q2)
```

    ## [1] "logical"

``` r
a <- seq(0,100, 2)
a
```

    ##  [1]   0   2   4   6   8  10  12  14  16  18  20  22  24  26  28  30  32  34  36
    ## [20]  38  40  42  44  46  48  50  52  54  56  58  60  62  64  66  68  70  72  74
    ## [39]  76  78  80  82  84  86  88  90  92  94  96  98 100

``` r
typeof(a)
```

    ## [1] "double"

``` r
repetition <- rep("repetition",100)
repetition
```

    ##   [1] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##   [6] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [11] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [16] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [21] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [26] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [31] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [36] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [41] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [46] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [51] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [56] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [61] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [66] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [71] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [76] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [81] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [86] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [91] "repetition" "repetition" "repetition" "repetition" "repetition"
    ##  [96] "repetition" "repetition" "repetition" "repetition" "repetition"

``` r
typeof(repetition)
```

    ## [1] "character"

# Resumindo

Esses comandos nos ensinaram algumas coisas:

1.  R pode fazer cálculos básicos
2.  R pode guardar valores em sua memória

-   Mas tenha em mente que o R não salva nada a não ser que você solicite

1.  Usamos "\<-" para atribuir variáveis

-   "=" também é possível, mas "\<-" is é melhor porque
    1.  "=" já aparece em alguns comandos, então "\<-" é exclusivo para atribuir variáveis
    2.  "\<-" explicita a direção da atribuição

1.  Existem alguns tipos de dados no R, sendo os básicos os seguintes:

-   **Integer**: números inteiros
-   **Double**: números com decimais
-   **Complex**: números em notação científica
-   **Character**: palavras ou letras
-   **Logical** ou Boolean): variável logica *TRUE* ou *FALSE*
-   **Dates**: números que representam datas
-   **Vector**: sequência ordenada de números ou letras

1. Os comandos em R são sempre sequências de letras seguidas de  "()" como `seq()`
2. A maneira de dizer ao R que um valor deve ser entendido como um caractere é escrever entre aspas
3. Cada comando pode receber um conjunto de argumentos
