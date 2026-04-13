# Entrance Exam Admission Analysis: Normal Distribution Model

> A statistical analysis tool built to determine an optimal university admission cutoff based on seat capacity and student performance distribution.

---

## Project Overview

University entrance exams often face the challenge of fluctuating difficulty levels year-over-year. A fixed "passing mark" fails to account for these variations. This project implements a **Relative Performance Model** using the Normal (Gaussian) Distribution to dynamically calculate a cutoff score that ensures exactly **1,500 seats** are filled from a pool of **10,433 applicants**.

---

## Key Features

- **Data Cleaning** — Automated removal of redundant metadata using Pandas.
- **Statistical Modeling** — Implementation of Z-score normalization to handle relative merit.
- **Dynamic Cutoff** — Calculation based on actual seat capacity rather than arbitrary percentages.
- **High-Contrast Visualization** — Custom dark-themed Matplotlib plots for clear data interpretation.

---

## Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation and cleaning |
| `numpy` | Numerical operations and array handling |
| `matplotlib` | Custom visualization and distribution plotting |
| `scipy.stats` | Probability density functions and Z-score calculations |

---

## The Model

The admission logic follows the Standard Normal Distribution formula:

$$z = \frac{x - \mu}{\sigma}$$

To find the cutoff $x$ for the top $N$ seats:

1. Calculate the required percentile: $1 - (\text{seats} / \text{total applicants})$
2. Determine the critical $z$-value using the **PPF** (Percent Point Function)
3. Solve for $x$: $x = \mu + (z \cdot \sigma)$

---

## Results

| Metric | Value |
|---|---|
| Mean ($\mu$) | ~99.97 |
| Standard Deviation ($\sigma$) | ~58.08 |
| Admission Capacity | 1,500 seats |
| **Calculated Cutoff Score** | **161.54** |

---

## Repository Structure

```
.
├── mathassignment.ipynb   # Primary notebook: cleaning, analysis, visualization
└── dataset.csv                      # Raw and processed CSV file
```

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/daksheshsharma2409/exam_score_distribution_assignment.git
cd exam_score_distribution_assignment
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib scipy
```

**3. Open the Jupyter Notebook**
```bash
jupyter notebook admission_analysis.ipynb
```

---

## Links

- **Kaggle Dataset** — [[Link to dataset](https://www.kaggle.com/datasets/kundanbedmutha/college-admission-dataset-india)]

---
