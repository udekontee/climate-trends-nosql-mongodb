# climate-trends-nosql-mongodb

# Project Overview
This project analyzes long-term temperature trends in the Colorado River Basin using a NoSQL data pipeline built on MongoDB. Raw climate data is ingested into MongoDB as document-based records, processed using Python and pandas, and visualized to uncover long-term warming patterns.

The project demonstrates how NoSQL databases can be effectively used for time-series climate analytics, including trend analysis, rolling averages, and decadal aggregation. It emphasizes practical data engineering and analytical workflows rather than theoretical database concepts.

The final outputs include publication-quality visualizations and a cleaned, analysis-ready dataset suitable for further modeling or reporting.

## Tech Stack
- **Database:** MongoDB (NoSQL document store)
- **Programming Language:** Python
- **Data Processing:** pandas, NumPy
- **Visualization:** Matplotlib
- **Data Source:** Public climate temperature records (Colorado River Basin)

## Data Pipeline & Architecture
The project follows a structured NoSQL-based data pipeline:
1. **Raw Data Ingestion**
   - Monthly climate temperature data is loaded into MongoDB as documents.
   - Each document represents a time-based observation.

2. **MongoDB Storage**
   - Data is stored in a MongoDB collection without a fixed schema, leveraging NoSQL flexibility.
   - Yearly averages are computed and stored for downstream analysis.

3. **Data Extraction**
   - MongoDB data is queried and converted into a pandas DataFrame for analysis.

4. **Analytical Processing**
   - Yearly temperature trends are analyzed.
   - A 10-year rolling average is calculated to smooth short-term variability.
   - Decadal averages are computed to highlight long-term structural changes.

5. **Output Generation**
   - Visualizations are saved as image files.
   - A cleaned yearly dataset is exported as a CSV file for reuse.
  
## Visualizations

### Average Annual Temperature Trend
Shows year-to-year temperature variability and the overall warming trend.

<img width="837" height="413" alt="image" src="https://github.com/user-attachments/assets/4ec37453-aa67-48ba-8d9e-c51b23f46c94" />

### 10-Year Rolling Average Temperature
Smooths short-term fluctuations to highlight long-term climate trends.

<img width="843" height="414" alt="image" src="https://github.com/user-attachments/assets/92cf8394-2a0d-4928-bd4c-8c3fa62fd21f" />

### Decadal Average Temperature
Aggregates temperature data by decade to emphasize long-term structural warming patterns.

<img width="845" height="416" alt="image" src="https://github.com/user-attachments/assets/e79a7dfd-9a18-4f9d-819d-c9a7b0e7e563" />

## Key Insights
- The Colorado River Basin shows a clear long-term warming trend over the observed period.
- Short-term variability is present year-to-year, but rolling averages reveal sustained increases.
- Decadal averages highlight accelerated warming in recent decades.
- Combining NoSQL storage with Python analytics enables flexible and scalable climate analysis.

## How to Run

1. Install dependencies:
```bash
pip install -r requirements.txt

## Ingest data into MongoDB:
python scripts/ingest_to_mongodb.py

## Run analysis and generate outputs:
python scripts/climate_trend_analysis.py

## Future Enhancements
- Seasonal temperature analysis (DJF, MAM, JJA, SON)
- Temperature anomaly analysis using a historical baseline
- MongoDB aggregation pipelines for in-database analytics
- Interactive dashboards for climate exploration



