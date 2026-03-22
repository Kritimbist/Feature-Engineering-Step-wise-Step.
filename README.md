# Feature Engineering
In this project, I begin my journey into Feature Engineering by first performing Exploratory Data Analysis (EDA). I believe that before creating or transforming features, it is important to understand the dataset deeply, identify patterns, and discover relationships between variables. EDA helps me gain insights into the structure of the data and prepares me to build meaningful features.

For this project, I will be using a Housing Price dataset (CSV file) to analyze different aspects that influence house prices. Through this dataset, I aim to explore variables such as location, number of rooms, area, and other housing characteristics. By carefully studying these attributes, I can start identifying which features are important and how they interact with the target variable, which is the house price.

My goal with this analysis is not only to explore the dataset but also to broaden my understanding of Feature Engineering concepts. By examining the data step by step, I can learn how raw variables can be transformed into more informative features that improve machine learning models.

During the EDA process, I will focus on:

- Understanding the structure of the dataset

- Identifying missing values and outliers

- Analyzing relationships between features

- Visualizing distributions of variables

- Observing correlations with housing prices

This step allows me to build a strong foundation before moving into deeper Feature Engineering techniques, such as feature creation, transformation, encoding categorical variables, and selecting the most useful features for modeling.

Through this project, I aim to strengthen my understanding of Feature Engineering in both breadth and depth, using practical analysis on the housing price dataset to guide my learning process.


I imported the required libararies and datasets to perform data manipulation,visualization etc. I use hosing price prediction  in this Project
 - Dataset : https://www.kaggle.com/datasets/muhammadbinimran/housing-price-prediction-data

  - df.head() : used to print out five data variable from the dataset.

    <img width="723" height="239" alt="image" src="https://github.com/user-attachments/assets/f9e6ea54-cecf-41e8-b97c-eb9b3b4255b7" />

    - df.shape() : used to show no. of rows & columns in dataset.
    - df.isnull().sum() : shows the no. of null values in dataset.
      
      <img width="251" height="140" alt="image" src="https://github.com/user-attachments/assets/605f885f-e420-43af-8576-099e7cc8ce77" />

The df.hist(figsize=(12,10)) function creates a grid of histogram plots with an appropriate figure size for clarity, while plt.show() displays the output. This is commonly used during exploratory data analysis (EDA) to understand patterns, detect skewness, and identify potential outliers in the dataset.

<img width="804" height="674" alt="image" src="https://github.com/user-attachments/assets/a8cba75f-cce2-43cb-a2cc-126b299de2ea" />


The sns.boxplot(x=df["Price"]) function displays the median, quartiles, and potential outliers in the data, making it useful for identifying spread and unusual values. The plt.show() command then renders the plot, making it easier to analyze data variability and detect anomalies during exploratory data analysis (EDA).


<img width="434" height="347" alt="image" src="https://github.com/user-attachments/assets/692cec85-c35b-49c6-b103-d7d9aa535ab7" />

-Most house prices fall roughly between 180,000 and 280,000.
- The median price appears around 230,000.
- There are outliers on both sides:
- Very cheap houses near 0–50k
- Very expensive houses around 450k–500k 

The numeric columns — SquareFeet, Bedrooms, Bathrooms, YearBuilt, and Price — are converted to numeric values using pd.to_numeric with errors="coerce", which replaces any invalid entries with NaN. The Neighborhood column is converted to a categorical type and stripped of any leading or trailing spaces to ensure consistency. Finally, print(df.dtypes) displays the updated data types of all columns, helping verify that the data is ready for analysis and modeling.

<img width="239" height="131" alt="image" src="https://github.com/user-attachments/assets/5a5aeff4-c06b-4a21-b77b-20f8404728ae" />

- print(df["Bedrooms"].value_counts()) shows the count of properties for each number of bedrooms, helping to understand the distribution of bedroom counts in the dataset.

- print(df["YearBuilt"].min()) displays the oldest year a property was built,
- while print(df["YearBuilt"].max()) shows the newest, giving a sense of the age range of properties in the dataset.
- 
  <img width="575" height="297" alt="image" src="https://github.com/user-attachments/assets/bd5c7b90-2508-4c46-a6ea-b7ae728551c7" />
  

  The df["Bedrooms"].value_counts() function displays how many properties fall under each bedroom category, helping to understand the distribution. The df["YearBuilt"].min() and df["YearBuilt"].max() functions return the oldest and newest construction years in the dataset, giving insight into the range of property ages. Together, these help identify patterns and check for any unusual values in the data.

  
  <img width="402" height="204" alt="image" src="https://github.com/user-attachments/assets/928b0d5e-8177-4ab9-86d4-54ef7fd4de87" />
  

The sns.boxplot(x=df["Price"]) function highlights key statistics such as the median, quartiles, and potential outliers, making it easier to understand the spread and detect unusual price values. The plt.show() command then displays the plot, which is useful during exploratory data analysis (EDA) to identify variability and anomalies in property prices.

<img width="526" height="427" alt="image" src="https://github.com/user-attachments/assets/b265f4f4-58e2-4eeb-aa34-8203d851c71e" />


- Most house prices fall roughly between 180,000 and 280,000.

- The median price appears around 230,000.

- There are outliers on both sides:

- Very cheap houses near 0–50k

- Very expensive houses around 450k–500k

