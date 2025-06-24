# Analysis of the Nebraska Tractor Test Data

## Introduction
This project uses a dataset from the University of Nebraska Tractor Test Laboratory (NTTL), the officially designated tractor testing station in the United States. The laboratory tests tractor horsepower in accordance with the codes established by the Organisation for Economic Co-operation and Development (OECD).

The dataset, in tabular format, is provided as an Excel file (.xlsx), and includes 3,846 rows and 15 columns spanning from 1920 to 2022.

---

## Environment

| Library     | Version |
| ---         | ---     |
| Python      | 3.10.6 |
| Numpy       | 2.1.0  |
| Pandas      | 2.2.3   |
| Matplotlib  | 3.10.3  |
| Seaborn     | 0.13.2  |
| Scipy       | 1.15.3   |
| Statsmodels | 0.14.4   |

---

## Research Questions, Hypotheses, and Analysis Methodology
This project establishes three research questions along with their corresponding hypotheses and analysis methodology:

1. Is drawbar horsepower associated with tractor specifications?
   - H0: There is no statistically significant relationship between tractor specifications (year, transmission, chassis, fuel, belt horsepower, and PTO horsepower) and drawbar horsepower.
   - H1: At least one of the tractor specifications (year, transmission, chassis, fuel, belt horsepower, or PTO horsepower) has a statistically significant effect on drawbar horsepower.
   - Statistical method: Multiple Linear Regression

2. Do Manufacturers Differ in PTO Adoption Year?
   - H0: The average year of first PTO-equipped tractor introduction is the same across all manufacturers.
   - H1: At least one manufacturer introduced PTO-equipped tractors significantly earlier or later than others.
   - Statistical method: Kruskal-Wallis test

3. Is the Use of Diesel Fuel Increasing Over Time?
   - H0: Year has no effect on the probability that a tractor uses diesel fuel.
   - H1: Year has a significant effect on the probability that a tractor uses diesel fuel.
   - Statistical method: Logistic Regression

---

## Exploratory Data Analysis and Statistical Tests

Please refer to the notebook: `nebraska_tractor_analysis.ipynb`

---

## Conclusions

1. The analysis confirmed a strong association between tractor specifications and drawbar horsepower. Several transmission and chassis types, one fuel type, and newer production years showed significant positive effects, while some chassis types were negatively associated with drawbar horsepower.

2. This project examined whether manufacturers adopted PTO-equipped tractors at different times. Although the result did not reveal statistically significant differences, some variation was still observed in the distribution of years across manufacturers. Some manufacturers transitioned to PTO systems as early as the 1950s, while others adopted the technology much later. 

3. The analysis results showed a statistically significant relationship between production year and the likelihood of using diesel fuel. Over time, the use of diesel has steadily increased, and in recent years, it has become the sole type of fuel used in tractors.
