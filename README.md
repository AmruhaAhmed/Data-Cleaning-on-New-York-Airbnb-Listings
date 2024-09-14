# 🧹 Data Cleaning on New York City Airbnb Listings

I have used a dataset from Kaggle (public domain) related to Airbnb listings and metrics in New York City for the year 2019 to perform extensive data cleaning.

![image](https://github.com/user-attachments/assets/0b0983b1-05f1-43d2-b31b-c71153def12f)


### 📁 Dataset Link:
[New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data/data)

---

### 📝 Columns in the Dataset:
- `id`: Listing ID
- `name`: Description of the Airbnb listing
- `host_id`
- `host_name`
- `neighbourhood_group`: Location of the listing
- `neighbourhood`: Area of the listing
- `latitude`
- `longitude`
- `room_type`: Type of space listed
- `price`: Price in US dollars

---

## 🏗️ Project Structure:
1. **Initial Data Exploration**
2. **Imputation**
3. **Date Parsing**
4. **Outlier Detection and Handling**
5. **Text Preprocessing**
6. **Label Encoding**
7. **Column Removal**
8. **Min-Max Scaling**

---

### 1️⃣ Initial Data Exploration:
In this phase, I performed the following:
- Imported all necessary libraries.
- Observed the following points:
  - The `name`, `neighbourhood_group`, `last_review`, and `reviews_per_month` columns have NaN values.
  - No duplicate values in the dataset.



### 2️⃣ Imputation:
- Imputed the NaN values in `name`, `neighbourhood_group`, `last_review`, and `reviews_per_month` columns using statistical functions like mean and mode.



### 3️⃣ Date Parsing:
- Standardized the format of dates in the `last_review` column.



### 4️⃣ Outlier Detection and Handling:
- Outliers were removed to avoid issues during model building.
- Used the z-score technique to detect outliers in `latitude`, `longitude`, and `price` columns.
- Outliers with z-scores outside the range of -3 to +3 were removed in the `latitude` and `longitude` columns.
- Price outliers were retained as they are justifiable by listing descriptions.



### 5️⃣ Text Preprocessing:
- Cleaned text-based columns (`name`, `host_name`, `neighbourhood_group`, and `neighbourhood`):
  - Removed stopwords.
  - Removed punctuation.
  - Converted all text to lowercase.



### 6️⃣ Label Encoding:
- Converted text-based columns into numeric form for easier handling using label encoding.



### 7️⃣ Column Removal:
- Removed columns `id`, `host_name`, `z_latitude`, `z_longitude`, and `z_price` as they had minimal contribution to further analysis.



### 8️⃣ Min-Max Scaling:
- Performed Min-Max Scaling on the numeric columns to standardize the dataset for machine learning algorithms.
- Created separate data frames for scaled and non-scaled features, then concatenated them into the final cleaned dataset `df`.

---

