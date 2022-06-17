By Rodrigo Esteves de Lima Lopes *University of Campinas* [rll307\@unicamp.br](mailto:rll307@unicamp.br)

------------------------------------------------------------------------

# Comparação entre Tweets

## Introdução

Neste tutorial vamos discutir como fazer uma exploração inicial nos dados textuais do Twitter. Aqui pretendemos realizar uma análise exploratória do texto raspado da linha do tempo de cada candidato.

Vamos usar os seguintes pacotes:

-   **dplyr** para lidar com os dados
-   **tidytext** para lidar com o texto
-   **ggplot2** para plotar

``` r
library(dplyr)
library(tidytext)
library(ggplot2)
```

# Preparando os dados

Nosso primeiro passo é isolar o texto de cada político que estamos estudando:

``` r
LI <- subset(presidents, screen_name == "LulaOficial")
JB <- subset(presidents, screen_name == "jairbolsonaro")
CG <- subset(presidents, screen_name == "cirogomes")
```

Nosso próximo passo é criar uma lista de palavras irrelevantes. Aqui vamos usar um que já existe, fornecido pelo `Quanteda`. Nós a salvamos como uma tabela de dados para aplicá-la aos nossos tweets posteriormente.

``` r
my.stopwords <- data.frame(word = quanteda::stopwords("pt"))
```

Agora executamos o seguinte comando para cada candidato, então temos três listas de palavras:

**Lula**

``` r
LI.w <- LI %>%
  unnest_tokens(word, text) %>% # separates each word
  count(word, sort = TRUE) %>% # counts each word
  anti_join(my.stopwords, by= "word") %>% # delete stopwords
  mutate(freq = n / sum(n)) %>% # proportion (base 1)
  mutate_at(vars(-matches("word|n")),~ .x * 100)  # tanslates proportion to base 100
```

**Jair Bolsonaro**

``` r
JB.w <- JB %>%
  unnest_tokens(word, text) %>%
  count(word, sort = TRUE) %>%
  anti_join(my.stopwords, by= "word") %>%
  mutate(freq = n / sum(n)) %>%
  mutate_at(vars(-matches("word|n")),~ .x * 100)
```

**Ciro Gomes**

``` r
CG.w <- CG %>%
  unnest_tokens(word, text) %>%
  count(word, sort = TRUE) %>%
  anti_join(my.stopwords, by= "word") %>%
  mutate(freq = n / sum(n)) %>%
  mutate_at(vars(-matches("word|n")),~ .x * 100) 
```

O próximo conjunto de comandos plota as listas de palavras, para mais informações sobre isso, consulte [08_plotting](08_plotting.md).

*Ciro*

``` r
CG.w %>% 
  slice(1:25) %>% 
  ggplot(aes(x = reorder(word, n, function(n) -n), y = n)) + 
  geom_bar(stat = "identity") + 
  theme(axis.text.x = element_text(angle = 60, hjust = 1)) +
  labs(
    x = "Words", y = "Frequency",
    title = "Frequency of Twitter words posted by Ciro Gomes",
    subtitle = "Twitter status (tweet) counts aggregated by day from January 2022",
    caption = "\nSource: Data collected from Twitter's REST API via rtweet"
  )
```

![Ciro](images/ciro.png)

*Lula*

``` r
LI.w %>% 
  slice(1:25) %>% 
  ggplot(aes(x = reorder(word, n, function(n) -n), y = n)) + 
  geom_bar(stat = "identity") + 
  theme(axis.text.x = element_text(angle = 60, hjust = 1)) +
  labs(
    x = "Words", y = "Frequency",
    title = "Frequency of Twitter words posted by Lulla",
    subtitle = "Twitter status (tweet) counts aggregated by day from January 2022",
    caption = "\nSource: Data collected from Twitter's REST API via rtweet"
  )
```

![Lula](images/lula.png)

*Jair Bolsonaro*

``` r
JB.w %>% 
  slice(1:25) %>% 
  ggplot(aes(x = reorder(word, n, function(n) -n), y = n)) + 
  geom_bar(stat = "identity") + 
  theme(axis.text.x = element_text(angle = 60, hjust = 1)) +
  labs(
    x = "Words", y = "Frequency",
    title = "Frequency of Twitter words posted by Jair Bolsonaro",
    subtitle = "Twitter status (tweet) counts aggregated by day from January 2022",
    caption = "\nSource: Data collected from Twitter's REST API via rtweet"
  )
```

![Jair Bolsonaro](images/jb.png)
