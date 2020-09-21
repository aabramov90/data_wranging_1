Data Wrangling Part1
================

# Setup

``` setup
library(tidyverse)
```

# Importing Dataset

Here we are importing the dataset from a relative path.

``` {"importing_dataset"}
"./data/FAS_litters.csv"
litters_data = read_csv(
  file = "./FAS_litters.csv"
  )
```

Cleaning up the dataset

``` {"cleaning_up"}
names(litters_data)

litters_data = janitor::clean_names(litters_data)

names(litters_data)
```

Now trying absolute versus relative paths.

``` {"absolute_vs_relative"}
pups_data = read_csv(file = "./FAS_pups.csv")

names(pups_data)

pups_data = janitor::clean_names(pups_data)

names(pups_data)
```
