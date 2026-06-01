# data-analyst-internship-task1
Data cleaning and preprocessing of Medical Appointment No-Shows dataset using Python and Pandas. Task 1 of Data Analyst Internship.
# Task 1: Data Cleaning and Preprocessing
## Data Analyst Internship - Elevate Labs

## Objective
Clean and prepare a raw Medical Appointment No-Shows dataset by handling nulls, 
duplicates, and inconsistent formats using Python and Pandas.

## Dataset
- **Source:** Kaggle - Medical Appointment No Shows
- **Original size:** 110,527 rows × 14 columns
- **Final size:** 110,526 rows × 14 columns

## Tools Used
- Python 3
- Pandas
- Google Colab

## Cleaning Steps Performed
1. Renamed all column headers to lowercase with underscores
2. Converted date columns to consistent dd-mm-yyyy format
3. Removed 1 row with invalid negative age (-1)
4. Standardized gender and no_show columns to uppercase
5. Confirmed no missing values in any column
6. Confirmed no duplicate rows

## Files
| File | Description |
|------|-------------|
| `KaggleV2-May-2016.csv` | Original raw dataset |
| `medical_appointments_cleaned.csv` | Cleaned dataset |
| `notebook.ipynb` | Python cleaning code |

## Key Findings
- No missing values were found in the dataset
- 1 row had an impossible negative age and was removed


## Interview Questions & Answers

**1. What are missing values and how do you handle them?**
Missing values are empty or null entries in a dataset. I handle them by first 
checking with df.isnull().sum(), then either dropping rows with dropna() or 
filling them with a mean/median/mode value using fillna() depending on the context.

**2. How do you treat duplicate records?**
I identify duplicates using df.duplicated().sum() and remove them using 
df.drop_duplicates(). In this dataset, no duplicates were found.

**3. Difference between dropna() and fillna() in Pandas?**
dropna() removes rows or columns that contain missing values entirely. 
fillna() replaces missing values with a specified value like mean, median, 
or a fixed number. I use dropna() when missing data is minimal and fillna() 
when I don't want to lose rows.

**4. What is outlier treatment and why is it important?**
Outliers are extreme values that differ significantly from other data points. 
They are important to treat because they can skew analysis and give misleading 
results. I handle them by checking with describe() and removing or capping values 
that are statistically impossible like the negative age (-1) found in this dataset.

**5. Explain the process of standardizing data.**
Standardizing means making data consistent across the dataset. For example, 
making sure gender values are all uppercase (F/M not f/m), date formats are 
all dd-mm-yyyy, and column names follow the same naming convention like 
lowercase with underscores.

**6. How do you handle inconsistent data formats (e.g., date/time)?**
I use pd.to_datetime() to convert date columns to a proper datetime format, 
then use .dt.strftime() to reformat them to a consistent pattern like dd-mm-yyyy. 
This removes timezone suffixes and other inconsistencies.

**7. What are common data cleaning challenges?**
Common challenges include missing values, duplicate rows, inconsistent text 
formats, wrong data types, outliers, and messy date formats. Each requires 
a different approach depending on the data.

**8. How can you check data quality?**
I check data quality using df.info() to see data types and null counts, 
df.describe() for statistical summary, df.isnull().sum() for missing values, 
and df.duplicated().sum() for duplicates. These give a full picture of the 
data's condition.
- Date columns had timezone suffixes that were stripped and reformatted
- Column names had typos (Hipertension) and inconsistent formatting
