# Capstone_Project

## Overview

​​​​​​​​​​​​​​​​​​​​​​​​The California Geologic Energy M​anagement Division (CalGEM) prioritizes protecting public health, safety, and the environment in its oversight of the oil, natural gas, and geothermal industries, while working to help California achieve its climate change and clean energy goals. To do that, CalGEM uses science and sound engineering practices to regulate the drilling, operation, and permanent closure of energy resource wells.

### Summary

This capstone project looks at CalGEM production and injection data from 2020 through 2023. The focus is to find out which operators were the top producers of oil, gas, and water and present it in a Tableau dashboard to stakeholders.

**Order Of Operations:**

Note: The CalGEM_Capstone script is performing the following tasks:

- Iterates over the specified years (2020, 2021, 2022, 2023).

- Creates filenames for three datasets related to California oil and gas wells for each year.

- Constructs URLs to download the datasets from CalGEM.

- Utilizes a custom header to request and retrieve the data from the URLs.

- Creates pandas dataframes for each dataset.

- Adds a 'ReportYear' column to each dataframe indicating the year of the data.

- Writes each dataframe to a CSV file with the corresponding filename.

- Establishes a connection to an SQLite database ('C://sqlite//capstone.db').

- Inserts the data from each dataframe into separate tables ('wells_data', 'production_data', 'injection_data') in the database.

- Adds a 5-second delay before processing the next year's data.

- Prints a message when processing for each year is complete.

- Finally, prints "Download Complete" when all years' data have been processed.


Once the production data was succesfully gathered from the CalGEM website and turned into dataframes I needed to flatten the data before analyzing the data.

**The Flatten_production_csv script performs the following tasks:**

- Specifies the paths for the output CSV files: wells_flattened_data.csv, production_flattened_data.csv, and injection_flattened_data.csv.

- Defines dictionaries containing the filenames for wells, production, and injection data - for the years 2020 to 2023.

- Iterates through the specified files for each category (wells, production, injection).

- Reads each CSV file using pandas and appends the data to the corresponding flattened output CSV file.

### Conclusion
Once the production and injection data was flattened it was moved into Sqlite for analysis. The analyzed data was then presented in a Tableau dashboard to stakeholders. You can find the dashboard here https://public.tableau.com/shared/PMZRHQX6F?:display_count=n&:origin=viz_share_link. 