
# 🏙️ Airbnb NYC 2019 Analysis & Price Prediction  

## 📌 Project Overview  
This project analyzes the **Airbnb NYC 2019 dataset** to uncover insights into hosts, neighbourhoods, pricing, availability, and reviews.  
It also includes **machine learning models** to predict listing prices and identify key factors influencing them.  

---

## 📊 Dataset  
- **Source**: Airbnb Open Data (2019)  
- **Rows**: 48,895 (after cleaning → 48,631)  
- **Columns**: 16  
- **Features**: Listing ID, host details, neighbourhood group, neighbourhood, latitude/longitude, room type, price, minimum nights, number of reviews, last review, reviews per month, host listing count, availability (days).  

---

## 🛠️ Steps in the Project  

### 1. Data Cleaning  
- Filled missing `name` and `host_name` with `"Unknown"`.  
- Filled missing `reviews_per_month` with `0`.  
- Converted `last_review` to datetime (kept missing as NaT).  
- **Outlier handling**:  
  - Removed listings with price = 0 or > 1000.  
  - Capped minimum nights at 365.  
- Final dataset: **48,631 rows × 16 columns**.  

### 2. Exploratory Data Analysis (EDA)  
- **Neighbourhoods**: Manhattan & Brooklyn dominate listings.  
- **Room types**: Entire homes/apartments most common in Manhattan; private rooms dominate Brooklyn.  
- **Price distribution**: Manhattan most expensive, Bronx & Staten Island cheapest.  
- **Availability**: Listings are either rarely available (0 days) or fully available (365 days).  
- **Top hosts**: Companies like Sonder (NYC) & Blueground manage hundreds of listings.  
- **Most reviewed**: Rooms near JFK/LaGuardia airports (Queens) and Manhattan private rooms.  

### 3. Machine Learning Models  
- **Linear Regression**:  
  - MAE ≈ 56.39  
  - R² ≈ 0.32  
- **Random Forest Regressor**:  
  - MAE ≈ 54.98  
  - R² ≈ 0.33  
- Random Forest performed slightly better.  

### 4. Feature Importance  
Top predictors of price:  
1. Availability (days per year)  
2. Room type (Private room vs Entire home)  
3. Reviews per month  
4. Number of reviews  
5. Minimum nights  

---

## 📈 Key Insights  
- Manhattan & Brooklyn dominate Airbnb activity.  
- Price differences are significant between boroughs.  
- Corporate hosts manage a large share of listings.  
- Guest demand is high near airports and central Manhattan.  
- Availability and room type matter more than neighbourhood in predicting price.  

---

## 📂 Files in Repository  
- `airbnb_nyc_analysis.ipynb` → Jupyter Notebook with code, cleaning, EDA, and ML models  
- `Airbnb_NYC_Report.docx` → Detailed written report  
- `Airbnb_NYC_Analysis_Report.pptx` → Presentation with graphs and conclusions  
- `README.md` → Project summary (this file)  

---

## 🚀 How to Run  
1. Clone this repo:  
   ```bash
   git clone https://github.com/yourusername/airbnb-nyc-analysis.git
   cd airbnb-nyc-analysis
   ```  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Open Jupyter Notebook:  
   ```bash
   jupyter notebook airbnb_nyc_analysis.ipynb
   ```  

---

## 🏆 Conclusion  
- Airbnb NYC data shows strong concentration in Manhattan & Brooklyn.  
- Outlier cleaning improves analysis quality.  
- Prediction models show moderate accuracy, but reveal availability & room type as key pricing drivers.  
- This project is both an **EDA case study** and a **baseline predictive modeling project**.  

---

✨ Feel free to fork, improve, and extend this analysis with advanced ML models or interactive dashboards!  
