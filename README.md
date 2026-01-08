# Landsat NDVI and NBR Time Series Analysis

## Project Overview  
This project analyzes Landsat-derived Normalized Difference Vegetation Index (NDVI) and Normalized Burn Ratio (NBR) time series data obtained from Google Earth Engine. The goal is to assess vegetation health and burn severity over time using statistical and time series analysis techniques.

## Data  
- Source: Landsat satellite imagery via Google Earth Engine  
- Data: NDVI and NBR values with daily timestamps (NDVI) and irregular timestamps (NBR)  
- Processed CSV files: `landsat_ndvi.csv`, `nbr.csv`

## Methods  
- Stationarity Testing: Augmented Dickey-Fuller (ADF) test to check if the time series are stationary  
- Missing Data Handling: Cubic spline interpolation for daily NDVI data  
- Resampling: Downsampled to monthly and yearly averages for both NDVI and NBR  
- Visualization: Time series plots for original and resampled data  

## Key Concepts  
- **Augmented Dickey-Fuller Test:**  
  - Null hypothesis (H0): Time series is non-stationary  
  - Alternative hypothesis (H1): Time series is stationary  
  - Decision based on p-value threshold 0.05

## Results  
- NDVI and NBR time series were interpolated and resampled to monthly and yearly scales  
- Stationarity of NDVI assessed with ADF test (example test statistic: -5.38, indicating stationarity)  
- Visualizations illustrate temporal trends and seasonal patterns  

## Usage  
1. Load CSV files into pandas DataFrames  
2. Perform ADF test for stationarity  
3. Interpolate missing values (NDVI) using cubic spline  
4. Resample data to desired frequency (monthly, yearly)  
5. Plot and analyze trends  

## Dependencies  
- pandas  
- numpy  
- scipy  
- matplotlib  
- statsmodels  

## Conclusion  
This workflow enables robust temporal analysis of vegetation indices from Landsat data, supporting environmental monitoring such as drought, vegetation health, and burn severity assessment.
