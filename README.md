# Scooter Rental Analysis
**By: Taran Schlichtmann**
**Date: 10/23/2025**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/18dmzh-YLIPU1qkfAKmw7ZZfIv-sRhUdR)

---

## Business Context
Analyze scooter-sharing usage patterns and predict daily rentals using linear regression. Leverage two years of rental data to uncover trends influenced by seasonality, workdays, and weather, providing insights for operational planning and demand forecasting.

---

## Learning Objectives
- Perform **data cleaning** and **feature engineering**.
- Visualize rental patterns by season, workday, and weather conditions.
- Build and evaluate a **linear regression model** to predict daily rentals.

---

## Repository Structure
```
.
├── gb881_final_project_schlichtmann_t.py   # Core analysis script
└── README.md                                # Project documentation
```

---

## Tech Stack
- Python 3.x
- Pandas — Data manipulation
- Seaborn & Matplotlib — Visualization
- SciPy — Statistical analysis
- scikit-learn — Regression modeling

---

## Dataset
- **Source**: [Scooter Rental Dataset](https://bit.ly/scooter-rentals)
- Loaded via:
```python
URL_Scooter_Rentals = 'https://bit.ly/scooter-rentals'
Dataframe_Scooter_Rentals = pd.read_csv(URL_Scooter_Rentals)
```

---

## Objective
Understand factors influencing scooter rentals and predict daily rental counts using linear regression.

---

## Methodology
1. **Load & Inspect Data**: `.shape`, `.info()`, `.head()`
2. **Rename Columns** for clarity
3. **Feature Engineering**: Create `rentals_total`
4. **Exploratory Analysis**:
   - Histograms, scatterplots, swarmplots, line plots
   - Correlation heatmap and pairplots
5. **Modeling**:
   - Train/test split
   - Fit linear regression model using temperature
   - Evaluate performance (R²)

---

## Results Summary
- Seasonal trends and workday status strongly influence rentals.
- Temperature shows positive correlation with rental volume.
- Linear regression model using temperature achieved R² ≈ 0.375.

> **Conclusion**: Temperature is a meaningful predictor, but additional features could improve accuracy.

---

## Visualizations
- Histogram of total rentals
- Scatterplot: registered vs. unregistered rentals
- Swarmplot by season
- Line plot by month and year
- Pairplot and heatmap for weather indicators

---

## How to Run
### Google Colab
Open: [Colab Notebook](https://colab.research.google.com/drive/18dmzh-YLIPU1qkfAKmw7ZZfIv-sRhUdR)

### Local Environment
```bash
# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Install dependencies
pip install pandas seaborn matplotlib scipy scikit-learn

# Run script
python gb881_final_project_schlichtmann_t.py
```

---

## Statistical Notes
- Linear regression assumes linearity and independence.
- Consider adding multiple predictors for better performance.

---

## Future Work
- Incorporate additional weather and calendar features.
- Explore **multivariate regression** or **machine learning models**.
- Add **cross-validation** for robust evaluation.

---

## References
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [scikit-learn Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

---

## 📄 License
MIT License — Educational use only.

