HW1
================
Shourav Makkapati
9/22/2021

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.3     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.6     ✓ dplyr   1.0.3
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.4.0     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
bridges<- read_csv("~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv")
```

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
    ## cols(
    ##   .default = col_double(),
    ##   STATE_CODE_001 = col_character(),
    ##   STRUCTURE_NUMBER_008 = col_character(),
    ##   ROUTE_NUMBER_005D = col_character(),
    ##   FEATURES_DESC_006A = col_character(),
    ##   CRITICAL_FACILITY_006B = col_logical(),
    ##   FACILITY_CARRIED_007 = col_character(),
    ##   LOCATION_009 = col_character(),
    ##   LRS_INV_ROUTE_013A = col_character(),
    ##   RAILINGS_036A = col_character(),
    ##   TRANSITIONS_036B = col_character(),
    ##   APPR_RAIL_036C = col_character(),
    ##   APPR_RAIL_END_036D = col_character(),
    ##   NAVIGATION_038 = col_character(),
    ##   OPEN_CLOSED_POSTED_041 = col_character(),
    ##   VERT_CLR_UND_REF_054A = col_character(),
    ##   LAT_UND_REF_055A = col_character(),
    ##   DECK_COND_058 = col_character(),
    ##   SUPERSTRUCTURE_COND_059 = col_character(),
    ##   SUBSTRUCTURE_COND_060 = col_character(),
    ##   CHANNEL_COND_061 = col_character()
    ##   # ... with 20 more columns
    ## )
    ## ℹ Use `spec()` for the full column specifications.

    ## Warning: 98508 parsing failures.
    ##  row                   col           expected actual                                                    file
    ## 4071 OTHER_STATE_CODE_098A 1/0/T/F/TRUE/FALSE    134 '~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv'
    ## 4731 OTHER_STATE_CODE_098A 1/0/T/F/TRUE/FALSE    124 '~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv'
    ## 4849 OTHER_STATE_CODE_098A 1/0/T/F/TRUE/FALSE    134 '~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv'
    ## 7518 DESIGN_LOAD_031       a double              C   '~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv'
    ## 7685 OTHER_STATE_CODE_098A 1/0/T/F/TRUE/FALSE    134 '~/Desktop/Wisconsin/Math433/HW/HW1/2020BridgeData.csv'
    ## .... ..................... .................. ...... .......................................................
    ## See problems(...) for more details.

``` r
bridges_15<- bridges%>%
  filter(STATE_CODE_001==15)
```

``` r
bridges_15%>%
  ggplot(aes(STRUCTURE_KIND_043A, ADT_029, col=YEAR_BUILT_027))+
  geom_point()
```

    ## Warning: Removed 12 rows containing missing values (geom_point).

![](HW1_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->
