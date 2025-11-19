#**Part 1 — Used Cars Dataset (train.csv)**

Objective

Perform data cleaning, preprocessing, and basic data manipulation operations on a used cars dataset.

**(a) Missing Value Treatment**

Steps

Missing values were inspected across all columns.

Columns with few missing values (Mileage, Engine, Power, Seats) were imputed using the median.

New_Price contained ~86% missing values and was removed due to unreliability.

**Output**

Table of missing values

Cleaned dataset containing no missing values

**(b) Removal of Units**

Steps

The following columns originally contained text units and were converted into numeric form:

Column	Example Before	Example After
Mileage	“19.67 kmpl”	19.67
Engine	“1582 CC”	1582
Power	“126.2 bhp”	126.2
New_Price	“8.61 Lakh”	8.61

A function extracted the leading numeric value from each entry.

**Output**

Updated dataset preview showing unit-free numeric values

**(c) One-Hot Encoding**

Steps

The categorical variables:

Fuel_Type

Transmission

were encoded into multiple binary columns using one-hot encoding.

**Output**

New columns created:

Fuel_Type_Petrol, Fuel_Type_Diesel, Fuel_Type_Electric

Transmission_Manual, Transmission_Automatic

**(d) Feature Engineering**

Steps

A new feature was created:

Car_Age = Current_Year − Year


Using the current year from Python.

**Output**

Table displaying Year and corresponding Car_Age

**(e) Data Manipulation Tasks**

Performed using pandas equivalents of:

select()

filter()

rename()

mutate()

arrange()

summarize() with group_by()

**Output**

Tables of selected columns

Filtered records (e.g., older cars priced under a threshold)

Renamed columns

New calculated metrics (Price_per_1000km)

Sorted lists by price

Grouped summaries by Fuel_Type



#**Part 2 — Diabetes Dataset (diabetes.csv)**

Objective

Treat the dataset as a population and study sampling behavior and bootstrap distributions.
Total: 20 points

**(a) Random Sample of 25 & Glucose Comparison**

Steps

A seed was set for reproducibility.

A random sample of 25 observations was selected.

Sample statistics:

Mean Glucose

Maximum Glucose

Compared with population statistics.

**Results**
Statistic	Population	Sample (n=25)
Mean Glucose	~120.89	~130.36
Max Glucose	199	197
**Output**

Bar chart comparing sample vs population values

**(b) 98th Percentile of BMI**

Steps

Computed the 98th percentile of BMI for the population and the sample.

**Results**
Statistic	Population	Sample (n=25)
98th Percentile (BMI)	~47.53	~45.26
**Output**

Bar chart comparing sample vs population BMI 98th percentiles

**(c) Bootstrap Analysis (500 Samples of Size 150)**

Steps

500 bootstrap samples (replace=True) were generated.

For each bootstrap sample, the following were computed for BloodPressure:

Mean

Standard deviation

98th percentile

The average of these bootstrap statistics was compared with the actual population values.

**Results**
Statistic	Population	Bootstrap Average
Mean	~69.11	~69.15
Standard Deviation	~19.36	~19.19
98th Percentile	~99.32	~98.03

**Findings**

Bootstrap mean closely matches the population mean.

Bootstrap SD approximates the population SD well.

Bootstrap 98th percentile shows more variability, which is expected for high percentiles.

**Output**

Bar chart comparing population vs bootstrap average statistics

Histograms of bootstrap means, SDs, and percentiles

**Software & Libraries**

Python

pandas

numpy

matplotlib

Google Colab environment

**Reproducibility**

Random seeds were used to ensure reproducible sampling and bootstrap results.

All calculations and visualizations can be reproduced by running the notebook cells sequentially.

**Files Included**

**notebook/usedcars.ipynb**

Full preprocessing, feature engineering, and manipulation for Part 1.

**notebook/part2diabetes.ipynb**

Sampling, percentile estimation, and bootstrap analysis for Part 2.

**reports/part2_diabetes_findings.md**

Written findings summarizing Part 2 results.

**data/train.csv, data/diabetes.csv**

Datasets used in this process.
