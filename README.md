# global_power_plant_electricity_generation exploration

## by Gladens Popoola


## Dataset

The dataset is from the World Resources Institute and Data Contributors and can be downloaded from [here](https://wri-dataportal-prod.s3.amazonaws.com/manual/global_power_plant_database_v_1_3.zip).There are 34936 power plants in the dataset with 36 features(country, country_long, name, gppd_idnr, capacity_mw, latitude, longitude, primary_fuel, other_fuel1, other_fuel2, other_fuel3, commissioning_year, owner, source, url, geolocation_source, wepp_id, year_of_capacity_data, generation_gwh_2013, generation_gwh_2014, generation_gwh_2015, generation_gwh_2016, generation_gwh_2017, generation_gwh_2018, generation_gwh_2019, generation_data_source, estimated_generation_gwh_2013, estimated_generation_gwh_2014, estimated_generation_gwh_2015, estimated_generation_gwh_2016, estimated_generation_gwh_2017, estimated_generation_note_2013, estimated_generation_note_2014, estimated_generation_note_2015, estimated_generation_note_2016, estimated_generation_note_2017). For my analysis, I'll be focusing on the generation and estimated generation for the year 2017 alone so I'll be making use of the following columns: country_long, name, capacity_mw, primary_fuel, generation_gwh_2017, and estimated_generation_gwh_2017. So I created a new dataframe called power_plant_2017 containing these columns only. This dataframe contains 33007 powwer plants and 6 features(needed for my analysis). Of the 6 features, 3 are categorical and 3 are numerical.


## Summary of Findings

In my exploration, I found that there is a stronger relationship between 'capacity_mw and generation_gwh_2017', 'capacity_mw and estimated_generation_gwh_2017' on a logarithmic scale. I also discovered that power plants that make use of Nuclear primary_fuel have the highest capacity_mw, generation_gwh_2017 and estimated_generation_gwh_2017 on average. There is no correlation between number of power plants per country and average capacity_mw, so the determining factor for high average capacity_mw, generation_gwh_2017 and estimated_generation_gwh_2017 is majorly the type of fuel used in the power plants. Unsuprisingly, I also found that the country where power plant is located has no influence on the capacity_mw, generation_gwh_2017 and estimated_generation_gwh_2017.


## Key Insights for Presentation

For the presentation, I focus on the influence of primary_fuel, capacity_mw, and country on estimated_generation_gwh_2017 leaving out most of the intermediate logarithmic transformations. I start by introducing generation_gwh_2017 and estimated_generation_gwh_2017 features, followed by the capacity_mw. 
Then I do a log transformed scatterplot of 'capacity_mw and generation_gwh_2017' and 'capacity_mw and estimated_generation_gwh_2017'. Finally, I do a clustered barplot of the distribution of estimated_generation_gwh_2017 by country and primary_fuel.