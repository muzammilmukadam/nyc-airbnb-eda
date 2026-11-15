# NYC Airbnb Analysis - Exploratory Data Analysis Project

## Overview
This project performs an exploratory data analysis (EDA) on NYC Airbnb listings data from 2019. The analysis examines the characteristics of Airbnb properties across New York City's five boroughs, exploring relationships between property features, pricing, reviews, and location.

## Dataset
- **Source**: Airbnb listings data for New York City (2019)
- **Total Records**: 48,895 listings
- **Features Analyzed**: 16 columns including price, room type, neighborhood, reviews, and availability

## Project Structure
```
├── Nyc_Airbnb_Analyis.ipynb    # Jupyter Notebook with complete analysis
├── AB_NYC_2019.csv            # Raw dataset (original)
└── AB_NYC_2019_Cleaned.csv    # Cleaned and preprocessed dataset
```

## Key Analyses Performed

### 1. Data Cleaning
- Handled missing values (reviews_per_month and last_review columns)
- Removed unnecessary columns: id, name, host_name
- Converted last_review to datetime format
- Verified no duplicate entries existed

### 2. Feature Engineering
- One-hot encoding for categorical variables:
  - neighbourhood_group (5 boroughs)
  - neighbourhood (221 neighborhoods)
  - room_type (3 types)
- Total of 239 features after encoding

### 3. Statistical Analysis
- Outlier detection using Interquartile Range (IQR) method:
  - Price: 2,972 outliers identified (including extreme values up to $10,000/night)
  - Reviews per month: 3,312 outliers
  - Minimum nights: 6,607 outliers
- Feature scaling using StandardScaler and MinMaxScaler

### 4. Visual Explorations
- Price distribution histogram and box plot
- Listings by room type and neighborhood group
- Average price comparisons
- Correlation heatmap of numerical features
- Price vs number of reviews scatter plot
- Availability distribution visualization

## Key Findings

### Price Analysis
- Most listings range between $50-$250 per night
- Extreme outliers include luxury properties priced up to $10,000/night
- Private rooms are generally cheaper than entire home/apts

### Neighborhood Insights
- Manhattan and Brooklyn have the most listings
- Different room types vary by neighborhood

### Reviews and Availability
- Strong correlation between number of reviews and price
- Most listings have varying availability throughout the year

## Libraries Used
- pandas, numpy: Data manipulation and analysis
- matplotlib, seaborn: Data visualization
- sklearn: Preprocessing (LabelEncoder, OneHotEncoder, StandardScaler, MinMaxScaler)
- PIL: Image processing

## How to Run

1. Clone this repository
2. Ensure you have Jupyter Notebook installed
3. Install required Python packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn pillow
   ```
4. Open `Nyc_Airbnb_Analyis.ipynb` in Jupyter Notebook
5. Run all cells to reproduce the analysis

## Data Source
The dataset used is publicly available Airbnb data for NYC. This is for educational and analytical purposes only.

## Author
Created by Muzammil mukadam for exploratory data analysis project