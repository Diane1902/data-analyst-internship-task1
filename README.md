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
- Date columns had timezone suffixes that were stripped and reformatted
- Column names had typos (Hipertension) and inconsistent formatting
