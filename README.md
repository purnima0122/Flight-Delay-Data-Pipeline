# Flight Delay Data Pipeline

## Problem Statement
Create a data pipeline for this dataset:  
https://www.kaggle.com/datasets/sriharshaeedala/airline-delay/data

The pipeline should include:
1. Extract (load CSV)
2. Transform (clean data and transform data if needed)
3. Load (save the cleaned data in CSV file)
4. Visualizations using Seaborn:
- Correlation of attributes
- Distribution of values in attributes
- Any 3 additional graphs
5. Generate insights from the visualizations and explain them.

## Dataset Description 
This dataset provides detailed information on flight arrivals and delays for U.S. airports, categorized by carriers. It includes metrics such as arriving flights, delays over 15 minutes, cancellations, diversions, and delay-minute breakdown by carrier, weather, NAS (National Airspace System), security, and late aircraft. It can be used to analyze carrier and airport performance and understand key factors contributing to delays.

## Project Workflow

### 1. Extract (Load CSV)
- Input file: `Airline_Delay_Cause.csv`
- Loaded using `pandas.read_csv()`

### 2. Transform (Clean and Prepare)
- Remove duplicates
- Handle missing values
- Fix data types
- Create derived metrics such as delay rate, cancellation rate, and diversion rate

### 3. Load (Save Cleaned Data)
- Output file: `Airline_Delay_Cleaned.csv`
- Saved using `DataFrame.to_csv(..., index=False)`

### 4. Data Visualization (Seaborn)
The notebook includes:
1. Distribution of delay rate (histogram)
2. Correlation heatmap of key numerical attributes
3. Average delay rate by month (bar chart)
4. Top 10 airlines by average delay rate (bar chart)
5. Total delay minutes by cause (bar chart)

## Insights (Summary)
- Delay rate is right-skewed: most observations have lower delay rates, with fewer extreme high-delay cases.
- Delay behavior varies by month, indicating seasonal patterns.
- Some airlines consistently show higher average delay rates than others.
- Certain delay causes contribute much more total delay minutes than others.
- Correlation analysis helps identify attributes that move together and can guide further modeling.

## How To Run
```powershell
cd "C:\Users\Hp\Desktop\APython\Data Pipeline\Flight-Delay-Data-Pipeline"
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

## Requirements
- pandas
- numpy
- matplotlib
- seaborn
- ipykernel
