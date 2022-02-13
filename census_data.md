Census\_data
================
Shaina Mackin
12/17/2021

Import US Census American Community Survey data:

``` r
education_df = read_excel(path = "./data/ACS_Education_2019.xlsx", sheet = 2) 
poverty_df = read_excel(path = "./data/ACS_Poverty_2019.xlsx", sheet = 2)
disability_df = read_excel(path = "./data/ACS_Disability_2019.xlsx", sheet = 2) 
insurance_df = read_excel(path = "./data/ACS_Insurance_2019.xlsx", sheet = 2)
birth_df = read_excel(path = "./data/ACS_Birth_2019.xlsx", sheet = 2)
```

\#\#split , California from county column values \#\#merge on fips codes
for all 5 dfs, write to new csvs
