
<!-- README.md is generated from README.Rmd. Please edit that file -->

# tidyheatmap

<!-- badges: start -->

<!-- badges: end -->

The goal of `tidyheatmap` is to provide a tidyverse-style interface to
the powerful heatmap package
[pheatmap](https://github.com/raivokolde/pheatmap) by
[@raivokolde](https://github.com/raivokolde). This enables the
convenient generation of complex heatmaps from tidy data.

## Installation

You can install the released version of `tidyheatmap` from GitHub with:

``` r
# install.packages("devtools")

devtools::install_github("jbengler/tidyheatmap")
```

## Example

Given a tidy data frame of gene expression data like `data_exprs`, you
can easily generate a basic heatmap.

``` r
library(tidyheatmap)

data_exprs
#> # A tibble: 800 x 3
#>    external_gene_name sample expression
#>    <chr>              <chr>       <dbl>
#>  1 Bsn                Hin_1        9.59
#>  2 Bsn                Hin_2        9.48
#>  3 Bsn                Hin_3        9.66
# ...

tidy_heatmap(data_exprs,
             rows = external_gene_name,
             columns = sample,
             values = expression
)
```

## Documentation

<https://jbengler.github.io/tidyheatmap/>
