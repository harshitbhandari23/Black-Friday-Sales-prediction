🛍️ Black Friday Sales Analysis

This project analyzes the Black Friday dataset to uncover insights about customer demographics, purchasing behavior, and product popularity.
The analysis is done using Python, Pandas, Seaborn, and Matplotlib in Google Colab.

📁 Dataset Information

The dataset used is BlackFriday.csv, which contains customer purchase data including:

User demographics (Gender, Age, City, Marital Status, Occupation)

Product details (Product_ID, Product_Category_1, 2, 3)

Purchase amount

⚙️ Steps Performed
1. 📤 Uploading the Dataset
from google.colab import files
uploaded = files.upload()


Loaded BlackFriday.csv and displayed the first few rows using pandas.

2. 🧹 Data Cleaning

Checked for null values and removed Product_Category_2 and Product_Category_3 columns.

Verified unique values and column data types.

del df["Product_Category_2"]
del df["Product_Category_3"]

3. 🔍 Data Exploration
🧑‍🤝‍🧑 Gender Analysis

Count of males and females

Pie chart for gender distribution

Total and average purchase amount by gender

👶 Age Group Analysis

Distribution of customers by age group

Unique products purchased per age group

Total and average spending by each age group

💍 Marital Status

Count of married vs unmarried

Purchases made by marital status

🏙️ City Analysis

Number of customers per city

Gender and age distribution in each city

Spending habits based on years lived in current city

💼 Occupation

Distribution of customers across occupations

Total purchases and unique products by occupation

📦 Product Categories

Most popular product categories

Spending distribution across categories

Top 10 most purchased products

4. 🧩 Multi-Column Analysis

Age vs Gender

Gender vs Marital Status

City vs Marital Status

Stay duration vs Gender, Age, and City

Created a combined column gender_status:

df["gender_status"] = df["Gender"] + "_" + df["Marital_Status"].astype(str)


Analyzed purchase patterns based on this combined demographic.

📊 Visualization Highlights

Used Seaborn and Matplotlib for:

Count plots

Bar charts

Pie charts

Comparative analyses

Examples:

snp.countplot(data=df, x="Gender", palette="plasma")
snp.barplot(data=df, x="Age", y="Purchase", palette="pastel")
plt.pie(...)

🧠 Insights Derived

Males tend to spend more than females on average.

Age group 26–35 has the highest purchase rate.

Most customers live in City Category B.

Occupations with IDs 4, 7, and 10 show higher purchase totals.

Product categories 1, 5, and 8 are most popular.

🧰 Tools & Libraries

Google Colab

Python 3

Pandas

Seaborn

Matplotlib

📈 Future Enhancements

Apply Machine Learning models for purchase prediction.

Perform time-series or trend analysis (if data available).

Build an interactive dashboard using Plotly or Power BI.
