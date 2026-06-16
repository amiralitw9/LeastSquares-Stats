# Linear Regression & Error Analysis Tool (C++) 📈

A lightweight, high-performance C++ utility designed for scientific data analysis. It computes the **Linear Regression** line using the **Least Squares Method**, calculates the correlation/regression coefficient ($R$), and performs rigorous **statistical error estimation** for both slope and intercept.

This tool is highly optimized for laboratory data processing, physics experiments, and calibration modeling.

---

## 🛠️ Mathematical Foundations

The program models a linear relationship between independent variables ($x$) and dependent variables ($y$) as $y = ax + b$, executing the following analytical steps:

1. **Slope ($a$) and Intercept ($b$):**
   $$a = \frac{\sum (x_i - \bar{x})y_i}{\sum (x_i - \bar{x})^2}$$
   $$b = \bar{y} - a\bar{x}$$

2. **Error Quantification:**
   - **Slope Uncertainty ($\Delta a$):** Calculates standard error bounds for the slope across $(n-2)$ degrees of freedom.
   - **Intercept Uncertainty ($\Delta b$):** Estimates confidence interval offsets based on data variance and center-of-mass distance.

---

## ✨ Features

- **Least Squares Regression:** Computes perfect-fit parameters ($a$ and $b$) for any paired dataset.
- **Error Analysis:** Generates precise uncertainty metrics ($\Delta a$ and $\Delta b$) for academic and laboratory reports.
- **Regression Factor ($R$):** Analyzes fitting quality against baseline prediction values.
- **Fast and Self-Contained:** Zero external dependencies, utilizing standard C++ streams.

---

## 🚀 How to Run

### Input Data Format
The program reads input from the standard console. 
1. First line: An integer $n$ (the total number of data points).
2. Subsequent $n$ lines: Two space-separated floating-point numbers representing $x_i$ and $y_i$.

#### Example Input:
```text
3
1.0 2.5
2.0 5.1
3.0 7.4
