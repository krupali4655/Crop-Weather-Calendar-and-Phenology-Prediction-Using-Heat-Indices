# Phenology-prediction-using-Heat-indices-and-crop-weather-calender.

 Methodology
Data Sources= In this project, two major sources of data were used:
Phenology Data= The phenological data was obtained 
This table recorded the number of days from sowing to each key growth stage of wheat, such as emergence, crown root initiation (CRI), tillering, booting, flowering, anthesis/flowering, milking, dough, and maturity.
The data spanned five cropping seasons (2019–20 to 2023–24), making it possible to analyze stage durations across years under different weather conditions.
Weather Data=Daily weather data was obtained for the years 2019–2024.The dataset included maximum temperature, minimum temperature, and date fields.Since the data was stored in multiple Excel files (year-wise or season-wise), a major preprocessing step involved merging all these files into a single master dataset.

The weather data was crucial for calculating heat indices, specifically the Growing Degree Days (GDD), which form the foundation for phenology prediction.
Data Preprocessing= Raw data often comes with inconsistencies and requires careful cleaning before it can be used for analysis. The preprocessing in this project involved the following steps:
Phenology Data Cleaning =Extracted the phenology table from the Word file and converted it into a tabular DataFrame.
Removed duplicate columns that arose due to formatting issues.
Standardized growth stage names (e.g., “Crown Root Initiation (CRI)” kept consistent across all years).
Converted “days from sowing” values into numeric form to enable calculations.
Weather Data Cleaning and Merging=Imported all Excel weather files (2019–2024).
Renamed column headers to maintain consistency (e.g., “max” → “maxt”, “min” → “mint”).
Merged all files into one continuous dataset indexed by date.
Checked for missing values and filled small gaps using linear interpolation.
Ensured no duplicate dates and confirmed date continuity across years.
Computation of Heat Indices
The most important step was calculating the Growing Degree Days (GDD).
Aggregation for Each Phenology Stage
For each growth stage (e.g., tillering, booting), the corresponding cumulative GDD and average temperature up to that date were calculated.
This linked phenological observations with weather data, creating the dataset used for machine learning.

in this project I used Linear regration, RF, SVM, XGBOOST.And  Predictions were compared against actual phenology observations.
Used statistical metrics:
MSE (Mean Squared Error) : penalizes large errors.
RMSE (Root Mean Squared Error) : error in actual days.
MAE (Mean Absolute Error) –:average error in days.
R² (Coefficient of Determination) :proportion of variance explained.

and the conclusion i find out is The study demonstrated that wheat phenology can be effectively predicted using heat indices (GDD) combined with machine learning models. Among the models tested, Random Forest and XGBoost provided the most accurate predictions, closely matching actual stage durations, while Linear Regression showed underfitting and SVM gave moderate results. This highlights the potential of integrating weather-based indices with ML to develop dynamic crop calendars, which can improve agricultural planning and resource management.


