
<!-- README.md is generated from README.Rmd. Please edit that file -->

# sass

[![Travis build
status](https://travis-ci.org/rstudio/sass.svg?branch=master)](https://travis-ci.org/rstudio/sass)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/rstudio/sass?branch=master&svg=true)](https://ci.appveyor.com/project/rstudio/sass)

The `sass` R package is a CSS preprocessor, letting R developers use
variables, inheritance, and functions to generate dynamic style sheets.

`sass` uses the [Sass](https://sass-lang.com/) CSS extension language.
Sass is stable, powerful, and CSS compatiable. `sass` is an R wrapper
for [LibSass](https://github.com/sass/libsass), a fast Sass compiler
written in C++.

## Installation

Install the released version of `sass` from CRAN:

``` r
install.packages("sass")
```

Install the latest development build from Github:

``` r
# install.packages("devtools")
devtools::install_github("rstudio/sass")
```

## Getting Started

The Sass language syntax is similar to CSS, but allows functions and
variables, and can do arbitrary computations.

``` r
library(sass)
#>  [1] "sass"      "testthat"  "stats"     "graphics"  "grDevices"
#>  [6] "utils"     "datasets"  "colorout"  "methods"   "base"
sass("
  $size: 100%;
  foo { margin: $size * .33; }
")
#> foo {
#>   margin: 33%;
#> }
#> 
```

For an overview of the major features of Sass such as variables,
nesting, and imports check out the official [Sass
Basics](https://sass-lang.com/guide).

## Examples

Checkout the `sass` Example [Shiny
App](https://gallery.shinyapps.io/140-sass-size/) and the `sass`
[website](https://rstudio.github.io/sass/articles/sass.html).
![](man/figures/shiny-app.gif)
