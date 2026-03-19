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

## Step 1 — Load & First Look
I imported the required libararies and datasets to perform data manipulation,visualization etc. I use hosing price prediction  in this Project
 - Dataset : https://www.kaggle.com/datasets/muhammadbinimran/housing-price-prediction-data

  - df.head() : used to print out five data variable from the dataset.

    <img width="723" height="239" alt="image" src="https://github.com/user-attachments/assets/f9e6ea54-cecf-41e8-b97c-eb9b3b4255b7" />

    - df.shape() : used to show no. of rows & columns in dataset.
    - df.isnull().sum() : shows the no. of null values in dataset.
      
      <img width="251" height="140" alt="image" src="https://github.com/user-attachments/assets/605f885f-e420-43af-8576-099e7cc8ce77" />




