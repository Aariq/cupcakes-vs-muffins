# Cupcakes vs. Muffins
Are cupcakes empirically different than muffins?  Let's find out!

This repository contains the following R notebooks:

1. `1-web-scraping.Rmd`: Contains code for scraping ingredients lists, calories, and numbers of servings from www.allrecipes.com for both cupcakes and muffins. Exports `muffin_raw.rds` and `cupcake_raw.rds`
2. `2-wrangling.Rmd`: Extracts ingredients, units, and amounts from raw ingredient lists. Converts amounts/units of all ingredients into cups or ounces. Filters data in various ways to ensure integrity of data. Imports `muffin_raw.rds` and `cupcake_raw.rds`, exports `recipes_tidy.rds` and `nofrosting_tidy.rds`
3. `3-EDA-outlier-removal.Rmd`: Does some exploratory data analysis to detect anomalies and outliers.  Exports `recipes_wide.rds`

And the following .rds files:

1. `cupcake_raw.rds`: a list of data frames of raw ingredients lists, servings, and calories from cupcake recipes.
2. `muffin_raw.rds`: a list of data frames of raw ingredients lists, servings, and calories from muffin recipes.
3. `recipes_tidy.rds`: finalized dataframe containing all acceptable muffin and cupcake recipes with ingredients categorized and amounts summarized by recipe (e.g. if there are two kinds of sugar, they are added together).  This dataframe also contains number of servings and calories.
4. `nofrosting_tidy.rds`: obviously cupcakes have frosting and muffins do not.  In this dataset, frosting and decoration ingredients are removed, as is the calories column since it is no longer accurate.
5. `recipes_wide.rds`: A wide data frame (each ingredient in its own column) ready for multivariate analysis.
