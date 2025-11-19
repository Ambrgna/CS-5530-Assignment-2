# Findings Report

### Look for the missing values:
##### The New_Price column has more than 80% missing values, so I dropped the entire column. With that much missing data, imputing would not be meaningful and the column would not contribute reliable information.

##### The missing values in Mileage, Engine, Power, and Seats are each less than 1% of the dataset. Because so few rows are affected, dropping these rows does not significantly reduce the dataset or impact the analysis. Imputing such a small number of values is unnecessary.

### Remove the units:
##### The columns Mileage, Engine, and Power contained units that needed to be standardized.

###### Engine and Power used single units (CC and bhp respectively). The units were removed, and the numeric values were converted to floats.

###### Mileage contained two units: kmpl and km/kg. To standardize, values in km/kg were converted to kmpl assuming km/kg corresponds to LPG fuel, while kmpl values were kept unchanged.

##### This ensures all three columns are now numeric and comparable, allowing for analysis and modeling.

### New Feature:
##### A new column Yearly_Mileage was added to the dataset. This feature represents the average kilometers driven per year and is calculated as:

###### Yearly_Mileage = Kilometers_Driven ÷ (Current_Year − Year)


##### This provides a standardized measure of car usage regardless of the car’s age, allowing for better comparisons and analysis across vehicles of different years.