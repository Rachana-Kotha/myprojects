# USDA Food Nutrient Analysis

This project provides an exploratory data analysis (EDA) of the USDA food nutrient dataset using Python. The objective is to transform and analyze food composition data to extract meaningful insights about nutrient content across various food groups.

## Dataset Overview

- **Source:** [USDA National Nutrient Database](https://github.com/wesm/pydata-book/tree/2nd-edition/datasets/usda_food)
- **File:** `database.json`
- **Records:** 6,636 food items
- **Features include:**
  - Food description
  - Manufacturer
  - Food group
  - Nutrients (e.g., protein, fat, carbohydrates, minerals, vitamins)

## Project Setup

### Requirements

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

### Dataset

Download the dataset from the source:

```bash
wget https://raw.githubusercontent.com/wesm/pydata-book/2nd-edition/datasets/usda_food/database.json
```

# USDA Food Nutrient Analysis

## Aim

The objective of this project is to perform an exploratory data analysis (EDA) on the USDA National Nutrient Database. The goal is to extract, clean, and analyze nutritional information across a wide range of food items to identify trends, compare nutrient values, and generate insights that can support dietary research, health recommendations, and food science studies.

---

## Approach

1. **Data Acquisition and Loading**  
   - The dataset `database.json` was sourced from the USDA National Nutrient Database which can be found in my repository via [Rachana's PyData GitHub repository]([https://github.com/Rachana-Kotha/myprojects/blob/main/USDA-Food-nutrient-predictor/database.json]).
   - It contains 6,636 food items with nested nutrient information.

2. **Data Inspection and Parsing**  
   - Food-level metadata such as description, group, ID, and manufacturer were extracted into a flat structure.
   - Nutrient data, originally nested under each food item, was normalized and expanded into a structured format.

3. **Data Cleaning and Merging**  
   - Duplicate and missing values were handled appropriately.
   - The food metadata and nutrient data were merged to enable cross-analysis.

4. **Analysis and Visualization**  
   - Group-level statistics such as counts and medians were calculated.
   - Plots were generated to compare nutrient content across food groups.
   - Top foods for each nutrient were identified based on maximum values.

5. **Tools Used**  
   - **Python Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
   - **Data Format:** JSON, structured into DataFrames for analysis

## Project Structure

- **Load and Inspect Data:** Load the `database.json` file and explore its structure.
- **Extract Food Metadata:** Parse basic attributes such as description, group, ID, and manufacturer.
- **Normalize Nutrient Data:** Flatten the nested nutrient dictionaries and clean the dataset.
- **Merge and Analyze:** Combine nutrient and food metadata for comprehensive analysis.
- **Visualizations:** Generate summary plots to highlight patterns and trends in nutrient content.

## Example Analyses

- Identify the top food groups by count.
- Determine the highest-nutrient food item within each nutrient group.
- Visualize median nutrient values across food groups.

## Sample Output

The cleaned and merged dataset (`ndata`) includes the following columns:

| nutrient | nutgroup     | units | value | id   | food            | fgroup                 | manufacturer |
|----------|--------------|-------|-------|------|------------------|-------------------------|--------------|
| Protein  | Composition  | g     | 25.18 | 1008 | Cheese, caraway | Dairy and Egg Products | N/A          |

---

## Observations

- **Food Group Distribution:**  
  Certain groups like “Vegetables and Vegetable Products” and “Beef Products” have higher representation in the dataset.

<img src="/USDA-Food-nutrient-predictor/countsvsgroup.png" height="400" align="center">

- **Nutrient Leaders:**  
  Some individual food items significantly stand out in terms of nutrient density (e.g., high protein cheese or vitamin-rich leafy greens).

<img src="/USDA-Food-nutrient-predictor/medianbynutrientgroup.png" height="400" align="center">

- **Group-wise Nutrient Trends:**  
  - Meats typically have higher protein content.
  - Fruits and vegetables are prominent sources of vitamins and fiber.
  - Grain-based foods exhibit higher carbohydrate content.

- **Manufacturer Data:**  
  Many entries lack manufacturer information, suggesting the data primarily focuses on general food types rather than branded products.

---

## Future Directions

- Develop interactive dashboards to explore nutrients by group or food item.
- Standardize units across energy values (e.g., converting between kcal and kJ).
- Explore clustering algorithms to group similar foods based on nutrient profiles.
- Enhance visual analysis with advanced techniques like heatmaps and radar charts.

## File Summary

```
.
├── database.json           # Raw USDA nutrient data
├── analysis.ipynb / .py    # Jupyter notebook or script for analysis
├── README.md               # Project documentation
```

## Author
Rachana Kotha
