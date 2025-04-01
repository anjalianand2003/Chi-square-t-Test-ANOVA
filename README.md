# Chi-square-t-Test-ANOVA
# 📊 Page View & Product Knowledge Analysis

This project explores the relationship between **user profile types** (Parent, Teacher, etc.) and their **product knowledge** and **browsing behavior (page views)** using e-commerce data.

## 📦 Dataset

- **File:** `ecommerce-data.csv`
- **Rows:** Anonymous user sessions
- **Key variables:**
  - `profile`: User type (e.g., Parent, Teacher)
  - `productKnewWhatWanted`: "Yes", "No", or "Somewhat"
  - `behavPageviews`: Categorical page view data ("0", "1", "2 to 3", ..., "10+")

---

## 🎯 Analysis Goals

- Determine if **Parents and Teachers differ in product awareness**
- Compare **page viewing behavior** across all user profiles
- Conduct **statistical testing** (chi-square, binomial, t-tests, ANOVA)
- Visualize confidence intervals of average page views per profile

---

## 🔍 Key Methods

### ✅ Product Knowledge Comparison

- Filtered for “Yes” and “No” responses
- Compared proportions across Parents and Teachers
- Performed:
  - Chi-Square Test
  - Binomial Test (Teacher vs Parent baseline)

### ✅ Page View Behavior

- Converted categorical page view ranges to numeric estimates
- Compared group means using:
  - T-Test (Parent vs Teacher)
  - ANOVA (all profiles)
  - Tukey’s HSD test for post-hoc comparisons

---

## 📊 Findings

| Test                    | Result Highlights                                        |
|-------------------------|----------------------------------------------------------|
| Chi-Square Test         | Significant difference in product knowledge awareness    |
| Binomial Test           | Teachers significantly differed from Parent baseline     |
| T-Test (Page Views)     | Mean page views differ significantly between groups      |
| ANOVA + Tukey HSD       | Multiple significant differences between profiles        |

---

## 📈 Visuals

- Histograms by profile
- 95% CI plots for mean page views across profiles

---

## 💻 How to Run

```r
install.packages(c("lattice", "multcomp"))
source("pageview_analysis.R")
