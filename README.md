
<!-- README.md is generated from README.Rmd. Please edit that file -->

# warwickplots <img src="man/figures/logo.png" align="right" height="138" alt="" />

<!-- badges: start -->
<!-- badges: end -->

An R package with colour palettes and themes that are consistent with
The University of Warwick’s
[branding](https://warwick.ac.uk/about/brand/brand-guidelines/),
especially its
[colours](https://warwick.ac.uk/about/brand/brand-guidelines/colours/)
and
[typography](https://warwick.ac.uk/about/brand/brand-guidelines/typography/).

The palettes are built using the
[**palettes**](https://mccarthy-m-g.github.io/palettes/index.html)
package.

## Installation

You can install the development version of warwickplots from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("Warwick-Stats-Resources/warwickplots")
```

## Example

Below is a plot that uses the `primary` palette and `theme_warwick()`.

``` r
library(warwickplots)
#> Loading required package: palettes
```

``` r
library(ggplot2)
library(palmerpenguins)
ggplot(penguins, aes(flipper_length_mm, body_mass_g, group = species)) +
  geom_point(aes(colour = species, shape = species), alpha = 0.8, size = 2) +
  scale_color_palette_d(warwick_palettes$primary) +
  labs(title = "Penguin Size, Palmer Station LTER",
       subtitle = "Flipper length and body mass for **<span style = 'color:#3C1053;'>Adelie</span>**, **<span style = 'color:#6DCDB8;'>Chinstrap</span>** and **<span style = 'color:#CB333B;'>Gentoo</span>** Penguins",
       caption = "Visualization: Ella Kaye, Data: Gorman, Williams & Fraser (2014) DOI: 10.1371/journal.pone.009008",
       x = "flipper length (mm)",
       y = "body mass (g)") +
  theme_warwick() +
  theme(legend.position = 'none')
```

![](man/figures/README-example-1.png)<!-- -->

For further docuementation, see `vignette("warwickplots")`.
