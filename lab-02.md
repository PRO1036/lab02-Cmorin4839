Lab 02 - Plastic waste
================
Coralie Morin
15 septembre 2025

## Chargement des packages et des données

``` r
library(tidyverse)
```

``` r
plastic_waste <- read_csv("data/plastic-waste.csv")
```

Commençons par filtrer les données pour retirer le point représenté par
Trinité et Tobago (TTO) qui est un outlier.

``` r
plastic_waste <- plastic_waste %>%
  filter(plastic_waste_per_cap < 3.5)
```

## Exercices

### Exercise 1

``` r
ggplot(plastic_waste,aes(x = plastic_waste_per_cap)) + geom_histogram(binwidth = 0.2) + facet_wrap( ~ continent )
```

![](lab-02_files/figure-gfm/plastic-waste-continent-1.png)<!-- -->

### Exercise 2

``` r
 ggplot(plastic_waste,aes(x = plastic_waste_per_cap, colour=continent, fill=continent))+ geom_density (alpha=0.4)
```

![](lab-02_files/figure-gfm/plastic-waste-density-1.png)<!-- -->

Le réglage de la couleur (color et fill) se retrouve dans aes\_
puisqu’il est relié avec une variable qui est dans ce cas, les
continents. Cependant, la transparence (alpha) est dans geom_density,
puisqu’elle n’est pas reliée aux variables et s’applique pour toute le
graphique.

### Exercise 3

Boxplot:

``` r
ggplot(plastic_waste, aes(x = continent, y=plastic_waste_per_cap)) +
  geom_boxplot()
```

![](lab-02_files/figure-gfm/plastic-waste-boxplot-1.png)<!-- -->

Violin plot:

``` r
ggplot(plastic_waste, aes(x = continent, y=plastic_waste_per_cap)) +
  geom_violin()
```

![](lab-02_files/figure-gfm/plastic-waste-violin-1.png)<!-- -->

Les violin plots permettent de mieux voir la distribution des données et
sont plus précis qu’un simple boxplot.

### Exercise 4

``` r
# insert code here
```

Réponse à la question…

### Exercise 5

``` r
# insert code here
```

``` r
# insert code here
```

Réponse à la question…

## Conclusion

Recréez la visualisation:

``` r
# insert code here
```
