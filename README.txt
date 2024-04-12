
README

Introduction
This repository contains two Python scripts.

Sector_data_MERGE.pynb - Gets a list of indexes, one for each sector, imports a CSV file for each index, removes unwanted data columns and then merges all 9 sectors data into one dataframe then saves as a csv to be used in the analysis.

MAIN.pybn - Cleans a reprocesses data for analyzing the performance of and, relationship between sectors during changes in the Federal Fund Rates. 

Dependencies:
pandas 
matplotlib
scipy
numpy

LOGIC:
Sector_data_MERGE.pynb


MAIN.pybn
Data Cleanup and reprocessing:

	Inputs:

	FEDFUND_DF.csv
	Federal Fund Rate data showing the monthly targeted federal fund rate (Interest Rates) from 2003 - 2010.
	Two Columns- Date: Date of observation (2003 - 2010). Federal Fund Rate Target: Target Federal Fund Rate.

	Sector_data_TOTAL.csv
	Sector performance data showing the weekly share values for indexes representing each sector in the S&P 500.
	Columns- Date: Date of observation. 
	Weekly share price values for 9 different sectors - 

1. Imports datasets containing Federal Fund Rate data (FEDFUND_DF.csv) and sector performance data (Sector_data_TOTAL.csv).

2. The Federal Fund Rate data is filtered into two different datasets based on specific date ranges denoted by lists start_dates 	and end_dates.
	The start and end dates were selected based on the period of time when interest rates were rising between 2003 - 2006, 	and falling from 2006- 2010.
	The two datasets are then saved into separate CSV files based on rising and falling interest rate environments.

3. Visualisations were created for each dataset in order to investigate relationships between sectors during interest rate rising and falling environments.
	

OUTPUTS:
	Filtered Sector Data (Separated into Rising and Falling Interest Rate Environments)
	
	Filtered Federal Fund Rate Data (FedFund_TS)		
	
	Data Visualization:
		Correlation heatmaps for sector performance during rising and falling interest rate environments.

		Line plots showing ROI of sectors during rising and falling interest rate environments.

		Boxplots comparing the distribution of sector values during rising and falling interest rate environments.

		Bar graphs comparing the standard deviation of each sector during rising and falling interest rate environments.

		Line plots visualizing the volatility of each sector over time.

		Summary statistics for sector performance during rising and falling interest rate environments.


Statistical Analysis:
	Summary statistics such as mean, median, minimum, maximum, and standard deviation are calculated for sector performance 	during rising and falling interest rate environments.


Important Steps and Highlights:

The script filters sector data based on specific date ranges corresponding to rising and falling interest rate environments.
Various visualizations such as heatmaps, line plots, boxplots, and bar graphs are utilized to analyze sector performance and volatility.
Summary statistics provide insights into the distribution and variability of sector performance during different interest rate environments.
Limitations
The analysis assumes a linear relationship between changes in the Federal Fund Rate and sector performance, which may not always hold true.
The script does not account for other economic factors that may influence sector performance.
The analysis is limited to the datasets and date ranges provided, and results may vary with different datasets or time periods.
The script does not include hypothesis testing or causal inference to establish a definitive relationship between the Federal Fund Rate and sector performance.


List of Variables Used
path: Path to the datasets.

df: 
DataFrame containing Federal Fund Rate data.

start_date, end_date: 
Lists of start and end dates for filtering data.

FedFund_TS: 
Filtered DataFrame for a specific date range.

Sector_Data_Total: 
DataFrame containing sector performance data.

labels: 
Labels for different interest rate environments.

df_Rising_FEDFUND, df_Lowering_FEDFUND, df_Total_FEDFUND_Cycle: 
DataFrames containing sector performance during rising, falling, and total interest rate cycles, respectively.

Correlation_matrix_rising, Correlation_matrix_lowering: 
Correlation matrices for sector performance during rising and falling interest rate environments.

roi_Rising_df, roi_Lowering_df, roi_Total_df: 
DataFrames containing ROI of sectors during rising, falling, and total interest rate cycles, respectively.

summary_rising, summary_lowering: 
Summary statistics for sector performance during rising and falling interest rate environments.

std_rising, std_lowering: 
Standard deviations of sector performance during rising and falling interest rate environments.

volatility: 
Volatility of each sector over time.

Conclusion
This Python script provides a comprehensive analysis of the relationship between changes in the Federal Fund Rate and sector performance. It offers insights into how different sectors react to changes in interest rates and can be used for further research or investment decision-making. However, it's essential to consider the limitations and external factors that may influence sector performance beyond interest rate changes.