
## Findings / Report

### (a) Glucose: Sample of 25 vs Population
[Findings / Report

### (a) Glucose: Sample of 25 vs Population

- Population mean Glucose ≈ 120.89.
- With seed = 123, sample (n=25) mean Glucose ≈ 130.36, which is a bit higher than the population mean.  
- Population max Glucose = 199, sample max Glucose ≈ 197.  
- The bar chart shows that for this small sample, the sample statistics are close but not exactly equal to the population values. This illustrates sampling variability.

### (b) 98th Percentile of BMI: Sample vs Population

- Population 98th percentile of BMI ≈ 47.53.
- Sample (n=25) 98th percentile of BMI ≈ 45.26 (with seed = 123), slightly lower than the population value.  
- The bar chart comparison shows that extreme percentiles (like 98th) can be quite sensitive to small sample sizes.

### (c) Bootstrap for BloodPressure

- Population BloodPressure:
  - Mean ≈ 69.11  
  - Standard deviation ≈ 19.36  
  - 98th percentile ≈ 99.32  

- From 500 bootstrap samples of size 150:
  - Average of bootstrap means ≈ 69.15 (very close to population mean).
  - Average of bootstrap standard deviations ≈ 19.19 (close to population SD).
  - Average of bootstrap 98th percentiles ≈ 98.03 (reasonably close to the population 98th percentile).

- The comparison bar chart shows that bootstrap averages are very close to the population values.
- The histograms of bootstrap statistics show that:
  - The bootstrap distribution of the mean is tightly centered around the population mean.
  - The SD and 98th percentile also fluctuate around the population values, but with more spread.
- Overall, the bootstrap results support the idea that bootstrapping can approximate the sampling distribution and provide good estimates of population statistics using resampling.
]

