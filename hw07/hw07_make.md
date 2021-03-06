hw07 word length report using make
================
Lisa Wei
2017-11-12

``` r
library(readr)
library(ggplot2)
library(readr)
library(tidyverse)
args <- commandArgs(TRUE)
```

Step 1: Downloading and writing to data frame the orginal data showing all the english words.
---------------------------------------------------------------------------------------------

Source: <http://www-01.sil.org/linguistics/wordlists/english/wordlist/wordsEn.txt>

``` r
knitr::opts_chunk$set(echo=TRUE)
en_words <- read_tsv(args[1], col_names="Words")
```

### The table below shows the first 100 words.

``` r
knitr::kable(head(en_words, n=100))
```

| Words         |
|:--------------|
| a             |
| aah           |
| aahed         |
| aahing        |
| aahs          |
| aardvark      |
| aardvarks     |
| aardwolf      |
| ab            |
| abaci         |
| aback         |
| abacus        |
| abacuses      |
| abaft         |
| abalone       |
| abalones      |
| abandon       |
| abandoned     |
| abandonedly   |
| abandonee     |
| abandoner     |
| abandoners    |
| abandoning    |
| abandonment   |
| abandonments  |
| abandons      |
| abase         |
| abased        |
| abasedly      |
| abasement     |
| abaser        |
| abasers       |
| abases        |
| abash         |
| abashed       |
| abashedly     |
| abashes       |
| abashing      |
| abashment     |
| abashments    |
| abasing       |
| abatable      |
| abate         |
| abated        |
| abatement     |
| abatements    |
| abater        |
| abaters       |
| abates        |
| abating       |
| abatis        |
| abatises      |
| abator        |
| abattoir      |
| abattoirs     |
| abbacies      |
| abbacy        |
| abbatial      |
| abbe          |
| abbes         |
| abbess        |
| abbesses      |
| abbey         |
| abbeys        |
| abbot         |
| abbotcies     |
| abbotcy       |
| abbots        |
| abbotship     |
| abbotships    |
| abbott        |
| abbr          |
| abbrev        |
| abbreviate    |
| abbreviated   |
| abbreviates   |
| abbreviating  |
| abbreviation  |
| abbreviations |
| abbreviator   |
| abbreviators  |
| abc           |
| abdicable     |
| abdicate      |
| abdicated     |
| abdicates     |
| abdicating    |
| abdication    |
| abdications   |
| abdicator     |
| abdomen       |
| abdomens      |
| abdominal     |
| abdominally   |
| abduct        |
| abducted      |
| abducting     |
| abduction     |
| abductions    |
| abductor      |

Step 2: Length of each word was calculated. Then, the number of words that started with each letter in the alphabet was counted.
--------------------------------------------------------------------------------------------------------------------------------

``` r
word_length <- data.frame(apply(en_words, 1, nchar)); colnames(word_length) <- c("Length"); rownames(word_length) <- NULL

en_words$start <- data.frame(do.call('rbind', strsplit(en_words$Words,'',fixed=TRUE)))[,1]
word_starts <- en_words %>% group_by(start) %>% count()
```

### Below are the word lengths of the first 100 words.

``` r
knitr::kable(head(word_length, n=100))
```

|  Length|
|-------:|
|       1|
|       3|
|       5|
|       6|
|       4|
|       8|
|       9|
|       8|
|       2|
|       5|
|       5|
|       6|
|       8|
|       5|
|       7|
|       8|
|       7|
|       9|
|      11|
|       9|
|       9|
|      10|
|      10|
|      11|
|      12|
|       8|
|       5|
|       6|
|       8|
|       9|
|       6|
|       7|
|       6|
|       5|
|       7|
|       9|
|       7|
|       8|
|       9|
|      10|
|       7|
|       8|
|       5|
|       6|
|       9|
|      10|
|       6|
|       7|
|       6|
|       7|
|       6|
|       8|
|       6|
|       8|
|       9|
|       8|
|       6|
|       8|
|       4|
|       5|
|       6|
|       8|
|       5|
|       6|
|       5|
|       9|
|       7|
|       6|
|       9|
|      10|
|       6|
|       4|
|       6|
|      10|
|      11|
|      11|
|      12|
|      12|
|      13|
|      11|
|      12|
|       3|
|       9|
|       8|
|       9|
|       9|
|      10|
|      10|
|      11|
|       9|
|       7|
|       8|
|       9|
|      11|
|       6|
|       8|
|       9|
|       9|
|      10|
|       8|

### Below is the number of words that starts with each letter of the alphabet.

``` r
knitr::kable(word_starts)
```

| start |      n|
|:------|------:|
| a     |   6541|
| b     |   6280|
| c     |  10324|
| d     |   6694|
| e     |   4494|
| f     |   4701|
| g     |   3594|
| h     |   3920|
| i     |   4382|
| j     |   1046|
| k     |    964|
| l     |   3363|
| m     |   5806|
| n     |   2475|
| o     |   2966|
| p     |   8448|
| q     |    577|
| r     |   6804|
| s     |  12108|
| t     |   5530|
| u     |   3312|
| v     |   1825|
| w     |   2714|
| x     |     79|
| y     |    370|
| z     |    265|

Step 3: Drawing graphs - a histogram of the distribution of the lengths of the English words and a bar graph showing the number of words that started with each letter in the alphabet.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![plot](length_distribution.png)

### What we notice in the graph below is that words that start with "d" and "s" are the greatest in number.

![plot](n_starts.png)
