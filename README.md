# Flight-Delay-Data-Pipeline

This project performs ETL and visualization on the `Airline_Delay_Cause.csv` dataset.

## Step 3: ETL Pipeline

### Extract (Load CSV)
- Load `Airline_Delay_Cause.csv` using pandas.

### Transform (Clean Data and Transform Data if Needed)
- Remove duplicate rows.
- Check/fix missing values.
- Validate and fix data types.
- Create helpful features like delay/cancel/divert rates.

### Load (Save the Cleaned Data in CSV File)
- Save final cleaned data as `Airline_Delay_Cleaned.csv`.

## Step 4: Data Visualization (Seaborn)

Required visualizations included in `Airline_delay.ipynb`:
1. Distribution of values in an attribute: `delay_rate_%` (histogram).
2. Correlation of attributes (heatmap).
3. Average Delay Rate by Month (bar chart).
4. Top 10 Airlines by Average Delay Rate (bar chart).
5. Total Delay Minutes by Cause (bar chart).

### Insights Generated
- Delay rate distribution is right-skewed: most cases have lower delay rates, with fewer extreme high-delay cases.
- Monthly averages reveal seasonality in delay behavior.
- Airline ranking shows which carriers have higher average delay rates in this dataset.
- Cause totals show dominant contributors to overall delay minutes.
- Correlation heatmap highlights attributes that move together strongly.

## Requirements
Install from `requirements.txt`:
- pandas
- numpy
- matplotlib
- seaborn
- ipykernel

## Run Locally
```powershell
cd "C:\Users\Hp\Desktop\APython\Data Pipeline\Flight-Delay-Data-Pipeline"
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name flight-delay-venv --display-name "Python (flight-delay-venv)"
jupyter notebook
```

## Kernel Loading Troubleshooting
1. In Jupyter, select kernel: `Python (flight-delay-venv)`.
2. Use `Kernel` -> `Restart Kernel and Clear Outputs`.
3. If still stuck, close processes and reopen:
```powershell
Get-Process python,python3,jupyter -ErrorAction SilentlyContinue | Stop-Process -Force
```
