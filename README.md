# AL-ML_Kaggle_Competition_Sage
Competition of "Sage" company for AI/ML Internship Role

You are provided with emissions data for most countries over the years 2015-2021. This data has been assembled by hand. The goal is to explore which countries have emissions profiles similar to the United States over the 2015-2021 time period by considering two factors: their total CO2 emissions and their change in CO2 emissions. You will have to do some data cleaning, calculate the relevant metrics per-country, and then use those metrics to compare vs the US.

# Instructions

1. Download the our Electricity Generation dataset, "train.csv"
2. It is likely that some mistakes have been made when collecting and aggregating this data. Do your best to resolve any issues. Reasonable substitutions are acceptable when original data is unrecoverable. Consider how your choices could impact the result of steps 3 and 4 below. Use your best judgement.
3. We are going to focus on the emissions_quantity column. Calculate the per-country sum of all "co2" over all years (i.e., where the value of gas is "co2", not "co2e_20yr", "co2e_100yr", etc.). Call this column emissions_quantity_sum.
Hint: If you are using a Pandas DataFrame, try .groupby()
4. Calculate the per-country total change in "co2" between 2015 and 2021 (i.e. "co2" in 2021 - "co2" in 2015), call this column emissions_change.
5. Normalize emissions_quantity_sum and emissions_change using StandardScaler from scikit-learn or another method that is mathematically equivalent. Name the normalized columns emissions_quantity_sum_norm and emissions_change_norm.
6. Using the two normalized columns as a two-dimensional vector, calculate the euclidean distance of each country from USA. Call this column distance. You could try using sklearn.metrics.pairwise.euclidean_distances.
7. Save your results in CSV format with the only the following columns: iso3_country, emissions_quantity_sum_norm, emissions_change_norm, and distance. There should only be one row per country.
8. Submit your resulting CSV.
