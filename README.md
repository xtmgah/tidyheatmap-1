
<!-- README.md is generated from README.Rmd. Please edit that file -->

# tidyheatmap

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/jbengler/tidyheatmap.svg?branch=master)](https://travis-ci.org/jbengler/tidyheatmap)
[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![Codecov test
coverage](https://codecov.io/gh/jbengler/tidyheatmap/branch/master/graph/badge.svg)](https://codecov.io/gh/jbengler/tidyheatmap?branch=master)
<!-- badges: end -->

The goal of `tidyheatmap` is to provide a tidyverse-style interface to
the powerful heatmap package
[pheatmap](https://github.com/raivokolde/pheatmap) by
[@raivokolde](https://github.com/raivokolde). This enables the
convenient generation of complex heatmaps from tidy data.

## Installation

You can install `tidyheatmap` from GitHub with:

``` r
# install.packages("devtools")

devtools::install_github("jbengler/tidyheatmap")
```

## Example

Given a tidy data frame of gene expression data like `data_exprs`, you
can easily generate a customized heatmap.

``` r
library(tidyheatmap)
devtools::load_all()
#> Loading tidyheatmap
#> Warning: package 'testthat' was built under R version 3.5.2
tidy_heatmap(data_exprs,
             rows = external_gene_name,
             columns = sample,
             values = expression,
             scale = "row",
             annotation_col = c(sample_type, condition, group),
             annotation_row = c(is_immune_gene, direction),
             gaps_row = direction,
             gaps_col = group
)
```

<img src="man/figures/README-unnamed-chunk-3-1.png" width="100%" />

## Documentation

<https://jbengler.github.io/tidyheatmap/>
