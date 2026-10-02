# Uber Rides Data Analysis Using Python

A data analysis project that explores Uber ride data using Python. The project focuses on data preprocessing, exploratory data analysis, visualization, feature transformation, and correlation analysis to identify meaningful patterns in Uber rides.

## Project Overview

This project analyzes Uber ride data to understand ride patterns based on different attributes such as:

- Ride category
- Ride purpose
- Date and time
- Time of day
- Day of the week
- Month
- Distance traveled

The project demonstrates how Python-based data analysis tools can be used to clean, transform, visualize, and analyze real-world datasets.

## Problem Statement

Uber ride datasets contain information about different rides, including their category, purpose, date, time, and distance. Analyzing this information can help identify patterns in ride usage and understand how ride activity varies across different time periods, purposes, and categories.

The objective of this project is to perform exploratory data analysis on Uber ride data and extract meaningful insights through data preprocessing and visualization.

## Objectives

- Load and understand the Uber rides dataset.
- Identify the structure and characteristics of the dataset.
- Handle missing and duplicate values.
- Convert date and time columns into appropriate formats.
- Extract useful features such as date, time, month, and day of the week.
- Analyze ride categories and purposes.
- Analyze ride activity across different times of the day.
- Analyze monthly and weekly ride patterns.
- Analyze the distribution of ride distances.
- Transform categorical variables using One-Hot Encoding.
- Analyze correlations between numerical and transformed variables.
- Visualize important patterns using Python libraries.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Kaggle

## Dataset

The project uses an Uber rides dataset containing information about individual Uber trips.

The dataset includes attributes related to:

- Start date
- End date
- Ride category
- Start location
- Stop location
- Ride purpose
- Miles traveled

The dataset is not included in this repository.

The analysis was originally developed and executed using Kaggle.

### Kaggle Notebook

[View the Kaggle Notebook](https://www.kaggle.com/code/nemisruparel/uber-rides-analysis)

## Project Workflow

```text
Dataset
   │
   ▼
Data Loading
   │
   ▼
Dataset Inspection
   │
   ▼
Data Preprocessing
   │
   ├── Handle Missing Values
   ├── Convert Date and Time
   ├── Extract Date/Time Features
   └── Remove Duplicate Records
   │
   ▼
Exploratory Data Analysis
   │
   ├── Category Analysis
   ├── Purpose Analysis
   ├── Time-of-Day Analysis
   ├── Monthly Analysis
   ├── Day-of-Week Analysis
   └── Miles Analysis
   │
   ▼
Feature Transformation
   │
   └── One-Hot Encoding
   │
   ▼
Correlation Analysis
   │
   └── Correlation Heatmap
   │
   ▼
Insights and Conclusion
```

## Data Preprocessing

The following preprocessing steps were performed:

### Handling Missing Values

Missing values in the `PURPOSE` column were replaced with `NOT` to represent unavailable ride purpose information.

### Date and Time Conversion

The `START_DATE` and `END_DATE` columns were converted into datetime format using Pandas.

### Feature Extraction

Additional features were extracted from the start date:

- Date
- Hour
- Time of day
- Month
- Day of the week

The ride time was categorized into:

- Morning
- Afternoon
- Evening
- Night

### Removing Missing Values

Remaining records containing missing values were removed from the dataset.

### Removing Duplicate Records

Duplicate records were identified and removed to improve data consistency.

## Exploratory Data Analysis

Several exploratory analyses were performed to understand the dataset.

### Ride Category and Purpose

The distribution of rides was analyzed based on:

- Ride category
- Ride purpose

Count plots were used to visualize the frequency of different categories and purposes.

### Time of Day

Ride activity was analyzed across different times of the day:

- Morning
- Afternoon
- Evening
- Night

### Ride Purpose by Category

The relationship between ride purpose and ride category was visualized using grouped count plots.

### Monthly Ride Analysis

The number of Uber rides was analyzed across different months to identify variations in monthly ride activity.

### Day-of-Week Analysis

Ride frequency was analyzed across the days of the week.

### Miles Analysis

The distribution of ride distances was analyzed using:

- Box plots
- Filtered box plots
- Histogram with KDE

Additional analysis was performed for rides below 100 miles and below 40 miles.

## Feature Transformation

Categorical variables such as `CATEGORY` and `PURPOSE` were transformed into numerical form using **One-Hot Encoding**.

Scikit-learn's `OneHotEncoder` was used with:

```python
OneHotEncoder(
    sparse_output=False,
    handle_unknown='ignore'
)
```

This transformation makes categorical information suitable for numerical analysis.

## Correlation Analysis

A correlation heatmap was created using numerical and one-hot encoded variables.

The heatmap helps examine the linear relationships between variables and provides correlation coefficients ranging from `-1` to `+1`.

## Visualizations

The project uses several visualization techniques:

- Count plots
- Bar plots
- Line plots
- Box plots
- Histograms
- KDE plots
- Correlation heatmap

These visualizations help identify patterns and distributions within the Uber rides dataset.

## Key Areas of Analysis

The project focuses on understanding:

- Distribution of rides across categories and purposes
- Ride frequency during different times of the day
- Ride activity across different days of the week
- Monthly variations in Uber ride activity
- Distribution of ride distances
- Unusually long or short rides
- Relationships between numerical and one-hot encoded variables

## Project Structure

```text
Uber-Rides-Data-Analysis/
│
├── README.md
├── Uber_Rides_Data_Analysis.ipynb
├── requirements.txt
└── .gitignore
```

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/NemisRuparel/Uber-Rides-Data-Analysis.git
```

### 2. Navigate to the Project Directory

```bash
cd Uber-Rides-Data-Analysis
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Virtual Environment

#### Linux / macOS

```bash
source .venv/bin/activate
```

#### Windows

```bash
.venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Open the Notebook

```bash
jupyter notebook
```

Then open:

```text
Uber_Rides_Data_Analysis.ipynb
```

## Running on Kaggle

The notebook was originally developed using Kaggle Notebook.

If you run the notebook on Kaggle, upload or attach the required dataset to the notebook and update the dataset path if necessary.

## Requirements

The required Python libraries are listed in `requirements.txt`.

## Future Improvements

Possible future improvements include:

- Adding more advanced statistical analysis.
- Creating an interactive dashboard using Power BI, Tableau, or Streamlit.
- Performing geographical analysis using pickup and drop-off locations.
- Analyzing ride duration if the required information is available.
- Comparing ride patterns between different categories.
- Applying machine learning techniques for prediction or classification.
- Adding interactive visualizations.

## Conclusion

This project demonstrates the use of Python for data preprocessing, exploratory data analysis, feature transformation, visualization, and correlation analysis.

By analyzing Uber ride data, the project provides insights into ride categories, purposes, time-based patterns, and ride distances. It also demonstrates how libraries such as Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn can be combined to analyze real-world datasets.

## Author

**Nemis Ruparel**

Computer Engineering Student

GitHub: [NemisRuparel](https://github.com/NemisRuparel)

Kaggle: [nemisruparel](https://www.kaggle.com/nemisruparel)
