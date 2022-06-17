By Rodrigo Esteves de Lima Lopes *Campinas University* [rll307\@unicamp.br](mailto:rll307@unicamp.br)

------------------------------------------------------------------------

# Plotagem

# Introdução

Nosso objetivo aqui é traçar os resultados que coletamos no último script. A gramática da plotagem pode ser um pouco desafiadora, mas lembre-se de que esta é apenas uma pequena introdução.

Neste tutorial usamos [`ggplot2`](https://ggplot2.tidyverse.org/index.html), um pacote para plotagem em R. Outros pacotes devem resolver, mas `ggplot2` é o mais popular entre os usuários do `R`.

Plotagem:

``` r
textplot_network(Lula.top.fcm, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'red')
```

![As 30 palavras mais frequentes de Lula](images/LulaWords.png)

``` r
textplot_network(Lula.top.hash, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'red')
```

![As 30 hashtags mais frequentes de Lula](images/LulaHash.png)

``` r
textplot_network(Lula.top.handles, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'red')
                 
```

![Os nomes de usuário mais citados/retuitados de Lula](images/LulaHandles.png)

``` r
textplot_network(Ciro.top.fcm, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'darkgreen')
```

![As palavras mais frequentes de Ciro Gomes](images/CiroWords.png)

``` r
textplot_network(Ciro.top.hash, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'darkgreen')
```

![As hashtags mais frequentes de Ciro Gomes](images/CiroHash.png)

``` r
textplot_network(Ciro.top.handles, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'darkgreen')
```

![Os nomes de usuário mais citados/retuitados de Jair Bolsonaro Ciro Gomes](images/CiroHandles.png)

``` r
textplot_network(JB.top.fcm, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'blue')
```

![As palavras mais frequentes de Jair Bolsonaro](images/JBWords.png)

``` r
textplot_network(JB.top.hash, 
                min_freq = 0.1, 
                edge_alpha = 0.5, 
                edge_size = 5,
                edge_color = 'blue')
```

![As hashtags mais frequentes de Jair Bolsonaro](images/JBHash.png)

``` r
textplot_network(JB.top.handles, 
                 min_freq = 0.1, 
                 edge_alpha = 0.5, 
                 edge_size = 5,
                 edge_color = 'blue')
```

![Os nomes de usuário mais citados/retuitados de Jair Bolsonaro](images/JBHandles.png)
