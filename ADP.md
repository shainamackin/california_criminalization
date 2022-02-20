ADP
================
Shaina Mackin
2/20/2022

``` r
adp_df = read_excel("./data/juvenile_adp.xlsx", col_types = "text") 
```

``` r
adp_girls = adp_df %>%
  janitor::clean_names() %>%
  mutate(
    adp_pre_disposition_female = replace(adp_pre_disposition_female, adp_pre_disposition_female == "D", 0),
    adp_pre_disposition_female = replace(adp_pre_disposition_female, adp_pre_disposition_female == "d", 0),
     adp_pre_disposition_female = replace(adp_pre_disposition_female, adp_pre_disposition_female == "u", 0),
     adp_post_disposition_female = replace(adp_post_disposition_female, adp_post_disposition_female == "D", 0),
     adp_post_disposition_female = replace(adp_post_disposition_female, adp_post_disposition_female == "d", 0),
    adp_post_disposition_female = replace(adp_post_disposition_female, adp_post_disposition_female == "u", 0),
  ) %>%
  select(county, year, month, adp_pre_disposition_female, adp_post_disposition_female)
```
