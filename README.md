# The Efficiency of Joy: Steam Market Value Analysis

## 📌 Project Overview

As the gaming industry shifts toward a standard **₹5,000 ($70) price tag** for blockbuster titles, consumers are increasingly questioning the return on their investment. This project analyzes a dataset of **1,400+ Steam games** to quantify "Value-per-Rupee."

By developing a custom **Joy Efficiency Score (JES)**, I compared the performance of **AAA giants** against **Indie/AA studios** to determine which segment provides the most satisfaction relative to its cost.

---

## 🛠️ Tech Stack & Methodology

* **Language:** Python 3.x
* **Libraries:** Pandas (Data Wrangling), Matplotlib & Seaborn (Visualization)
* **Currency Conversion:** Prices converted from USD to INR (Fixed Rate: 1 USD = 83 INR) for localized market analysis.
* **Iterative Data Cleaning:** * **The Publisher Filter:** A simple price-based filter failed to capture older AAA titles on sale. I engineered a keyword-matching algorithm to cross-reference publishers (e.g., EA, Ubisoft, Sony, Bandai Namco) to accurately categorize **294 AAA games** versus **1,201 Indie/AA titles**.
* **Review Thresholds:** Games with fewer than 500 total reviews were excluded to ensure statistical significance in user ratings.

---

## 📐 The "Joy" Metrics

To measure value objectively, I created two custom metrics:

1. **User Rating %**: Standardized satisfaction calculated as $\frac{Positive\ Reviews}{Total\ Reviews} \times 100$.
2. **Joy Efficiency Score (JES)**:

$$JES = \frac{User\ Rating\ \%}{Price\ (INR) + 1}$$


*Note: The "+1" in the denominator prevents division-by-zero for free games while maintaining a logical ranking.*
3. **Joy per 1,000 INR**: A normalized version of the JES used specifically to compare high-priced AAA titles without the scale being skewed by free-to-play games.

---

## 🚀 Key Insights

### 1. The Efficiency Gap (Indie vs. AAA)

The analysis revealed a massive disparity in value. Because of their lower price points, **Indie/AA games are statistically 1,300x more "efficient"** than AAA titles. While a AAA game requires a ₹5,000 investment for a ~80% satisfaction rate, an Indie game often provides 90%+ satisfaction for under ₹500.

### 2. The Quality Paradox

Surprisingly, the data shows that paying more doesn't always buy more quality.

* **Average Indie/AA Rating:** 80.5%
* **Average AAA Rating:** 75.8%
Indie studios currently hold a higher satisfaction "ceiling" than corporate giants in this dataset.

### 3. AAA Standouts

Despite the cost, some AAA titles justify their price. **Baldur's Gate 3** and **Sekiro: Shadows Die Twice** led the AAA bracket in "Joy per 1,000 INR," proving that extreme quality can overcome the "efficiency penalty" of a high price.

---

## 📊 Visualizations

### The Value Sweet Spot

This scatter plot identifies the "Hidden Gems"—games priced under ₹3,000 that maintain a user rating above 70%.


### AAA Efficiency Leaderboard

A focused look at which high-budget games actually deliver the most "Joy" per ₹1,000 spent.


### Market Composition

A breakdown of the 1,400+ games analyzed, showing the dominance of Indie/AA releases in the modern Steam ecosystem.


---

## 📁 Files in this Repository

* `final_steam_data_analysis_v3.csv`: Master dataset containing all calculated metrics and publisher tiers.
* `visuals/`: Directory containing all high-resolution distribution and comparison charts.
* `analysis_script.py`: (Optional) The Python code used for cleaning and JES calculation.

## 💡 Conclusion

For the average consumer, **Indie/AA titles represent the most logical financial choice** for consistent satisfaction. However, the data proves that AAA titles with "Overwhelmingly Positive" ratings still offer a competitive value proposition when normalized against their high production costs.
