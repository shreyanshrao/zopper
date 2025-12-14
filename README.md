📊 Retail Attach Rate Analysis & Forecasting
📌 Project Overview

This project is a data analytics pipeline built to evaluate and forecast Attach Rate performance of retail stores across multiple branches. It processes raw monthly sales data to uncover trends, classify store performance, and predict future metrics using statistical techniques.

The pipeline converts static spreadsheets into actionable business intelligence, enabling leadership to:

Identify Top Performing stores to replicate best practices

Detect Low Performing stores requiring corrective actions

Monitor consistency and seasonality across branches

🚀 Key Features

Data Normalization

Converts wide-format Excel data (months as columns) into long-format time-series data for analysis.

Trend Analysis

Computes linear trends (slope) for each store using regression to classify performance as:

Improving

Stable

Declining

Performance Categorization

Dynamically segments stores into:

Top Performers

Mid Performers

Low Performers

Variance Calculation

Measures performance consistency to flag unstable stores with high variability.

Forecasting

Predicts next month’s performance (January) using a 3-month moving average.

🛠️ Tech Stack

Language: Python 3.x

Libraries:

pandas – Data manipulation & transformation

numpy – Statistical calculations (trend slope, variance)

📂 Input Data Structure

The script expects a CSV file named:

Jumbo & Company_ Attach % .xls - Sheet1.csv

Expected Format:
Branch	Store_Name	Dec	Nov	Oct	Sep	Aug
Delhi_NCR	Store A	0.23	0.17	0.16	0.25	0.24
Pune	Store B	0.33	0.33	0.36	0.13	0.32

📌 Note:
The script automatically unpivots month columns into time-series format—no manual preprocessing required.

⚙️ Installation & Usage
1️⃣ Clone the Repository
git clone https://github.com/yourusername/attach-rate-analysis.git
cd attach-rate-analysis

2️⃣ Install Dependencies
pip install pandas numpy

3️⃣ Run the Analysis
python analysis_script.py

📊 Output

The pipeline generates an enriched dataset:

Processed_Store_Analysis.csv

Included Metrics:

Avg_Attach_Pct – Average attach rate over the analysis period

Trend_Status – Improving / Stable / Declining

Variance – Performance stability indicator

Category – Top / Mid / Low Performer

Jan_Forecast – Predicted attach rate for January

Best_Month – Highest performing month

Worst_Month – Lowest performing month

💡 Key Insights (Sample Data)

From the sample dataset analysis:

🏆 Top Branch: Pune (27.7% average) outperforms all other regions

⚠️ Critical Lag: Telangana shows significant underperformance (11.8%)

📈 Seasonality: Company-wide upward trend, peaking in November–December

🎯 Benchmark Store: Delhi (Hauz Khas) leads with a 62.2% average attach rate

🔮 Future Improvements

📉 Add visualizations using Matplotlib / Seaborn for trend comparison

📊 Implement weighted moving averages for improved forecasting accuracy

📄 Automate PDF report generation for branch managers

🔄 Integrate real-time data ingestion from retail systems
