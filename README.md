# Crop-Growth-stage-prediction
Estimating Crop Growth stages based on NDVI values 
This repository contains code to estimate crop growth stages based on Normalized Difference Vegetation Index (NDVI) values. NDVI is a widely used remote sensing technique to monitor crop health and growth. By analyzing NDVI time series data, it's possible to infer key growth stages of various crops.
# Dataset
The dataset used in this project (LSTM_Model_all_crops.csv) contains NDVI values for multiple crops over time. Each row represents a specific location and each column represents NDVI values for a particular date.
# Preprocessing
Shuffling: The dataset is shuffled to randomize the order of entries.
NaN Handling: NDVI values less than 0.1 are replaced with NaN to indicate missing or unreliable data.
Interpolation: Missing NDVI values are interpolated using neighboring values to maintain temporal continuity.
# Estimation Methodology
Growth Stages
For each crop, specific growth stages are defined along with their corresponding time differences from key stages like flowering or maturity. These growth stages are determined based on domain knowledge and literature review.

Max NDVI Stage
For each crop, the stage with the maximum NDVI value is identified. This stage is often indicative of peak vegetative growth or maturity.

Estimation
The timing of each growth stage is estimated relative to the max NDVI stage. Time differences defined earlier are used to calculate the estimated time of each growth stage.

# Output
The estimated growth stages for each crop are printed, showing the stage name and the corresponding estimated time.

# Supported Crops
The following crops are currently supported along with their growth stages:

Bajra
Cotton
Gram
Groundnut
Maize
Mustard
Onion
Potato
Rice
Soyabean
Wheat
