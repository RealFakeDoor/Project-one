# Federal Fund Rate and Sector Performance Analysis

## Overview
Welcome to the Federal Fund Rate and Sector Performance Analysis repository! This project provides a comprehensive investigation into the relationship between changes in the Federal Fund Rate and the performance of various sectors within the S&P 500 index. By analyzing historical data, we aim to uncover insights that can inform investment strategies and deepen our understanding of economic dynamics.

## Contents
1. **Sector_data_MERGE.pynb**: This Jupyter notebook facilitates the merging of sector data extracted from CSV files. It is a crucial step in preparing the data for subsequent analysis.
   
2. **Main.pybn**: The Python script `Main.pybn` is designed to handle the cleaning and processing of Federal Fund Rate data and sector performance data. It serves as the backbone of our analytical pipeline.

## Dependencies
To run the scripts in this repository, ensure you have the following dependencies installed:
- `pandas`
- `matplotlib`
- `scipy`
- `numpy`

## Inputs
Before running the scripts, make sure to have the following input datasets available:

1. **FEDFUND_DF.csv**: Federal Fund Rate data showing the monthly targeted federal fund rate (Interest Rates) from 2003 to 2010. This CSV file contains two columns: Date (observation period: 2003 - 2010) and Federal Fund Rate Target (target federal fund rate).

2. **Sector_data_TOTAL.csv**: Sector performance data showing the weekly share values for indexes representing each sector in the S&P 500. This CSV file contains columns for Date (observation period) and weekly share price values for 9 different sectors.

## Usage
1. Begin by executing `Sector_data_MERGE.pynb` to merge sector data from CSV files. This notebook streamlines the process of consolidating data from multiple sources.
   
2. Once the sector data is merged, proceed to run `Main.pybn` for data cleaning and processing. This script prepares the Federal Fund Rate data and sector performance data for analysis, enabling us to derive meaningful insights.

## Outputs
Upon running the scripts, you can expect the following outputs:
- Filtered datasets reflecting sector performance in rising and falling interest rate environments.
- Visualizations, including correlation heatmaps, line plots, boxplots, and bar graphs, to elucidate trends and relationships.
- Summary statistics detailing sector performance metrics during different interest rate cycles.

## List of Variables Used
- **path**: Path to the datasets.
- **df**: DataFrame containing Federal Fund Rate data.
- **start_date, end_date**: Lists of start and end dates for filtering data.
- **FedFund_TS**: Filtered DataFrame for a specific date range.
- **Sector_Data_Total**: DataFrame containing sector performance data.
- **labels**: Labels for different interest rate environments.
- **df_Rising_FEDFUND, df_Lowering_FEDFUND, df_Total_FEDFUND_Cycle**: DataFrames containing sector performance during rising, falling, and total interest rate cycles, respectively.
- **Correlation_matrix_rising, Correlation_matrix_lowering**: Correlation matrices for sector performance during rising and falling interest rate environments.
- **roi_Rising_df, roi_Lowering_df, roi_Total_df**: DataFrames containing ROI of sectors during rising, falling, and total interest rate cycles, respectively.
- **summary_rising, summary_lowering**: Summary statistics for sector performance during rising and falling interest rate environments.
- **std_rising, std_lowering**: Standard deviations of sector performance during rising and falling interest rate environments.
- **volatility**: Volatility of each sector over time.

## Limitations
It's essential to acknowledge the limitations of our analysis:
- The assumption of a linear relationship between changes in the Federal Fund Rate and sector performance may oversimplify complex economic interactions.
- External factors beyond interest rates, such as geopolitical events or industry-specific developments, may significantly influence sector behavior.
- While we strive for robustness, variations in datasets and timeframes may impact the reproducibility of results.
- Our analysis does not incorporate hypothesis testing or causal inference techniques to establish definitive relationships.

## Conclusion
In conclusion, the Federal Fund Rate and Sector Performance Analysis project offers a valuable framework for examining the interplay between monetary policy and market dynamics. By leveraging data-driven insights, investors and researchers can make informed decisions and navigate the complexities of the financial landscape.
