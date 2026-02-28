# Data Preprocessing
Today I learned about data preprocessing, which is one of the most important steps in any machine learning project. Raw data is usually messy, incomplete, and inconsistent, so preprocessing is needed to make the data suitable for training a model.

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/e7bd838c-5647-4b2e-aae9-d706be8733e5" />

## Data Cleaning

I learned that data cleaning is the process of fixing errors and inconsistencies in raw data so it becomes reliable and usable for analysis or machine learning. Real-world data is often messy, containing missing values, duplicate records, incorrect entries, and outliers. If I do not clean the data properly, even a good model can give poor and misleading results.

### Handling Missing Values
First, I learned how to handle missing values by either removing rows with missing data or filling them using mean, median, or mode, depending on the situation. This helps prevent errors during training.

To understand the process of handling missing value ,I first created a small dataset with missing values using NaN. Then I checked how many missing values were present in each column. For numerical columns like Age and Salary, I replaced missing values with the mean of the column. For the categorical column Department, I filled the missing value using the mode, which is the most frequent category.
- Output:

  <img width="584" height="480" alt="image" src="https://github.com/user-attachments/assets/7d15a4f3-ea0d-4155-aa19-b974eb239e2c" />

  - Source :https://www.geeksforgeeks.org/data-science/data-preprocessing-in-data-mining/
  - Code :https://github.com/Kritimbist/365-Days-of-GitHub-Challenge-AI-Machine-learning/blob/main/Data%20Preprocessing/code/Handle_missing_Value.py

## Fixing incorrect or inconsistent data
I learned that incorrect or inconsistent data can seriously affect model performance. These issues usually appear as impossible values, inconsistent category names, or wrong data formats. Before training a model, I need to identify and fix these problems so the data becomes reliable.
###  Common Problems I Fixed
- Negative values where they should not exist (e.g., age = -5)
- Different spellings for the same category (e.g., "Male", "male", "M")
- Extra spaces or mixed cases in text data
- Numerical values stored as strings

  <img width="705" height="344" alt="image" src="https://github.com/user-attachments/assets/136ec75c-b596-4cbb-b1a8-05d4b3690bf9" />


I first identified incorrect values in the Age column, such as negative numbers and unrealistic ages, and replaced them with NaN. Then I fixed inconsistent values in the Gender column by removing extra spaces, converting all text to lowercase, and mapping different representations to a single standard format. Finally, I converted the Salary column from text to numeric values, forcing invalid entries to become missing values so they can be handled later. This process helped me make the dataset consistent and reliable.

## Removing Duplicate Data
I learned that duplicate data means repeated rows that contain the same information. These duplicates can occur due to data collection errors, merging datasets, or repeated entries. If I do not remove duplicates, the model may learn biased patterns because the same data is counted multiple times.

I first created a dataset that contained duplicate rows. I used the duplicated() function to check how many duplicate records were present in the dataset. Then I removed those duplicates using the drop_duplicates() method. This ensured that each record appeared only once, making the dataset more accurate and reliable for further analysis or machine learning.

<img width="615" height="279" alt="image" src="https://github.com/user-attachments/assets/220ebae7-618f-4d5d-a28f-8172a6d2ccb2" />
<img width="587" height="176" alt="image" src="https://github.com/user-attachments/assets/82fed956-1ecd-4db7-bc03-3d4a8c923d56" />


## Handling outliers
I learned that outliers are extreme or unusual values that do not follow the general pattern of the data. Outliers can occur due to data entry errors, measurement issues, or rare but valid cases. If I do not handle outliers properly, they can distort the model and affect predictions.

I learned how to detect outliers using the IQR (Interquartile Range) method. I first created a simple dataset of house prices and intentionally added extreme values to represent outliers. I calculated the first quartile (Q1) and third quartile (Q3), then computed the IQR as the difference between them. Using the standard 1.5 × IQR rule, I defined lower and upper bounds and classified data points outside this range as outliers. Finally, I visualized the normal values and detected outliers using a scatter plot along with the IQR boundaries.


<img width="941" height="630" alt="image" src="https://github.com/user-attachments/assets/263264e6-ba4b-4958-80f1-65db328ccb36" />


## Correcting data types
Today I learned how to correct data types as an important step in data cleaning. When I load a real-world dataset, many columns are not in the correct format. Some numerical values are stored as strings, dates appear as plain text, and categorical values are treated as generic objects. If I do not fix these issues, data analysis and machine learning models may produce incorrect results.

I created a random dataset where numeric, boolean, and date values were incorrectly stored as text. I first checked the existing data types and then converted numeric columns using to_numeric, fixed boolean values using mapping, and converted the date column to datetime format. This process ensured my dataset had correct and meaningful data types, making it ready for analysis or machine learning.

<img width="667" height="316" alt="image" src="https://github.com/user-attachments/assets/40dd8b5c-9868-47cc-a8f9-304c1bf7ee86" />



# Data Integration
It involves merging data from various sources into a single, unified dataset. It can be challenging due to differences in data formats, structures, and meanings. Techniques like record linkage and data fusion help in combining data efficiently, ensuring consistency and accuracy.

## Record Linkage
Record linkage is the process where I match and connect records from different datasets that refer to the same entity. I handle differences in names, formats, or missing identifiers by comparing common attributes such as phone numbers, dates, or text similarity.

<img width="1098" height="521" alt="image" src="https://github.com/user-attachments/assets/faa0953e-243f-4400-b753-86c9b401b809" />

<img width="1047" height="506" alt="image" src="https://github.com/user-attachments/assets/65ac965a-3627-49cc-b0b8-b80fbd2ca470" />

<img width="977" height="676" alt="image" src="https://github.com/user-attachments/assets/beff9edb-1db2-4b06-9ce5-2c60d305bacf" />

In this code, I created two small datasets to represent data coming from different sources. The first dataset contains names and phone numbers, while the second dataset contains similar information but with different column names and slightly different name formats. I then used pd.merge() to perform record linkage by matching the phone number column from the first dataset with the contact column from the second dataset. By doing this, I linked records that refer to the same person based on a common identifier, even though their names are written differently. This allowed me to combine related information from both datasets into a single unified view.

## Data Fusion

Today I learned about data fusion, which is the process where I combine information from multiple data sources to produce more accurate, complete, and reliable results. I understood that data fusion goes beyond simply merging datasets; it focuses on resolving conflicts, reducing uncertainty, and improving the quality of information. By using data fusion, I can take advantage of the strengths of different data sources and create a unified view that is more meaningful for analysis and decision-making.
I do simple example of data fusion where i combine temperature readings from two different sensors. I first merged the datasets based on time, then fused the values by averaging them while handling missing data. This allowed me to produce a final temperature value that is more reliable than using data from a single source

<img width="905" height="671" alt="image" src="https://github.com/user-attachments/assets/640d6e0d-453e-4765-a13e-0c39d7f642cb" />

# Data Transformation
Today I learned that data transformation is the process where I convert raw and unstructured data into a clean, consistent, and usable format. I transform data by changing data types, scaling numerical values, encoding categorical variables, and restructuring the dataset. This step helps me prepare the data for analysis and machine learning by improving consistency, reducing errors, and making the data suitable for model training

 ## Data Normalization

 Today I learned how to normalize data using Min-Max scaling. I applied normalization to numerical features so that all values fall within the same range. This step helps machine learning models perform better by preventing features with large values from dominating the learning process.

 <img width="822" height="169" alt="image" src="https://github.com/user-attachments/assets/81e7471c-c54d-4bed-b182-aa719ca9a24f" />

 Example:

 <img width="903" height="711" alt="image" src="https://github.com/user-attachments/assets/2365d0c7-66fa-495c-a9f1-1e5a88ccb1cd" />
 <img width="795" height="572" alt="image" src="https://github.com/user-attachments/assets/8e2ed5ab-7e17-489a-b672-00bce3ab36ca" />

 ## Standardization
 Today I learned how to standardize data using Z-score. I transformed numerical features so they have zero mean and unit variance. This step helps machine learning algorithms perform better by ensuring all features contribute equally during training.

 <img width="743" height="256" alt="image" src="https://github.com/user-attachments/assets/76af387d-534e-4c33-a239-c75bc2608493" />

<img width="906" height="693" alt="image" src="https://github.com/user-attachments/assets/be5e1449-6859-49dd-976f-9405b73386f4" />

<img width="893" height="717" alt="image" src="https://github.com/user-attachments/assets/74a4accc-b25f-4f5c-895c-557cda8762d9" />

## Discretization
Today I learned about discretization, where I transformed continuous numerical data into discrete categories using binning. This helped simplify the dataset and made it more interpretable for analysis and machine learning models.


<img width="796" height="551" alt="image" src="https://github.com/user-attachments/assets/73c5990d-f56d-4e55-b834-87d490dcffb5" />

<img width="793" height="849" alt="image" src="https://github.com/user-attachments/assets/daf2d766-ede3-4968-81b6-5123de1705d8" />

I converted continuous age values into discrete categories using binning. This made the data easier to interpret and useful for models that work better with categorical features.


## Data Aggregation
Today I learned about Data Aggregation.

Data aggregation is a process where I combine multiple data points into summary values so the data becomes easier to analyze and understand. Instead of working with raw, detailed records, I group the data and apply functions like sum, mean, count, min, or max to get higher-level insights.

<img width="909" height="651" alt="image" src="https://github.com/user-attachments/assets/eeb85ebc-23e3-4a90-986a-43169616a206" />

<img width="872" height="498" alt="image" src="https://github.com/user-attachments/assets/dd0ef2d9-4179-4284-be95-5508af734626" />


 ## Concept Hierarchy Generation

Today I learned about Domain-Based Discretization.

Domain-based discretization is a technique where I convert continuous numerical data into categories using real-world knowledge or expert rules, not just mathematical ranges. Instead of letting the data decide the bins, I define the bins based on how the domain actually understands the values.


I have data about employees with their ages. I want to create a hierarchy of age groups:

Individual ages → Young/Adult/Senior → Child/Adult/Senior

<img width="767" height="695" alt="image" src="https://github.com/user-attachments/assets/9466f3ae-5a83-4996-a368-4739a4a3c6a7" />
