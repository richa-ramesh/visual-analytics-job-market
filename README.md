# Visual Analytics of LinkedIn Job Postings

[Banner image here]

## Group Information

| Name | Email |
|------|-------|
| Sunil Kuruba | skuru@uic.edu 
| Richa Rameshkrishna | rrame11@uic.edu |

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Assignment 1: Data Selection & Preprocessing](#assignment-1)
4. [Assignment 2: Visualization Design](#assignment-2)
5. [Assignment 3: Static & Interactive Visualizations](#assignment-3)
6. [Assignment 4: Linked Views & Spatial Analysis](#assignment-4)
7. [Assignment 5: Dimensionality Reduction](#assignment-5)
8. [Technologies](#technologies)
9. [How to Run](#how-to-run)
10. [Key Insights](#key-insights)

---

## Overview

[Copy from your first README]

## Dataset

**Source:** [LinkedIn Job Postings](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings/data)

[Copy dataset description from your READMEs]

---

## Assignment 1: Data Selection & Preprocessing

[Copy content from first README]

**Notebook:** [`notebooks/assignment-1/1-Data_Import_preprocessing.ipynb`](notebooks/assignment-1/1-Data_Import_preprocessing.ipynb)

---

## Assignment 2: Visualization Design

### Sketches

![Sketch Q1a](sketches/Q1a.png)
![Sketch Q1b](sketches/Q1b.png)
![Sketch Q2a](sketches/Q2a.png)
![Sketch Q2b](sketches/Q2b.png)
![Sketch Q3a](sketches/Q3a.png)
![Sketch Q3b](sketches/Q3b.png)

[Copy descriptions from README]

**Notebooks:**
- [`notebooks/assignment-2/2-Data_visualization.ipynb`](notebooks/assignment-2/2-Data_visualization.ipynb)
- [`notebooks/assignment-2/3-Data_Vizualization-2.ipynb`](notebooks/assignment-2/3-Data_Vizualization-2.ipynb)

---

## Assignment 3: Static & Interactive Visualizations

### Question 1: Temporal Trends

![Temporal Trends](visualizations/temporal-trends-in-job-postings.png)

[Copy Q1 description]

### Question 2: Skill Demand

![Skill Demand Ranking](visualizations/skill-demand-ranking.png)
![Skill Demand by Industry](visualizations/skill-demand-by-industry.png)

[Copy Q2 description]

### Question 3: Salary Analysis

![Salary Distribution](visualizations/salary-distribution-by-industry.png)

[Copy Q3 description]

### Question 4: Geographic Analysis

![US States Salary Map](visualizations/us-states-median-salary-map.png)

[Copy Q4 description]

### Interactive Enhancements

![Bubble Animation](visualizations/Bubble.gif)
![Heat Animation](visualizations/Heat.gif)
![Box Animation](visualizations/Box.gif)

**Notebook:** [`notebooks/assignment-3/3-Interactive-visuals.ipynb`](notebooks/assignment-3/3-Interactive-visuals.ipynb)

---

## Assignment 4: Linked Views & Spatial Analysis

### Task 1: Linked View Visualizations

[Copy description]

### Task 2: Spatial Visualization

[Copy description]

### Task 3: Coordinated Multi-View Dashboard

[Copy description]

**Notebooks:**
- [`notebooks/assignment-4/Task_1.ipynb`](notebooks/assignment-4/Task_1.ipynb)
- [`notebooks/assignment-4/Task_2.ipynb`](notebooks/assignment-4/Task_2.ipynb)
- [`notebooks/assignment-4/Task_3.ipynb`](notebooks/assignment-4/Task_3.ipynb)

---

## Assignment 5: Dimensionality Reduction

### Embedding Generation

[Copy description]

### UMAP & t-SNE

[Copy description]

### PCA Analysis

[Copy description]

### Interactive Web App

🌐 **[Live Demo](https://yourusername.github.io/linkedin-job-analytics/web-app/)** (if hosted)

**Notebooks:**
- [`notebooks/assignment-5/0_Data_cleaning.ipynb`](notebooks/assignment-5/0_Data_cleaning.ipynb)
- [`notebooks/assignment-5/1_Generate_Embedding.ipynb`](notebooks/assignment-5/1_Generate_Embedding.ipynb)
- [`notebooks/assignment-5/2_TSNE_and_UMAP.ipynb`](notebooks/assignment-5/2_TSNE_and_UMAP.ipynb)
- [`notebooks/assignment-5/3_PCA.ipynb`](notebooks/assignment-5/3_PCA.ipynb)

---

## Technologies Used

- **Python:** pandas, numpy, altair, scikit-learn
- **Visualization:** Vega-Lite, Altair
- **Web:** HTML, CSS, JavaScript
- **Tools:** Jupyter Notebook

---

## How to Run

### Prerequisites
```bash
pip install -r requirements.txt
```

### Run Notebooks
1. Navigate to notebook folder
2. Open Jupyter: `jupyter notebook`
3. Run cells in order

### Run Web App
1. Open `web-app/index.html` in browser
2. Or host on local server: `python -m http.server`

---

## Key Insights

[Copy key findings from your READMEs]

---

## References

- Dataset: [LinkedIn Job Postings - Kaggle](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings/data)
- Libraries: Altair, pandas, scikit-learn
```

---

### Step 5: Create requirements.txt

In root folder:
```
pandas>=1.5.0
numpy>=1.23.0
altair>=5.0.0
vega_datasets>=0.9.0
scikit-learn>=1.3.0
jupyter>=1.0.0
matplotlib>=3.7.0
```

---

### Step 6: Update .gitignore

Add to `.gitignore`:
```
# Large data files
data/*.csv
!data/README.md

# Jupyter
.ipynb_checkpoints/

# Python
__pycache__/
*.pyc

# OS
.DS_Store
```

---

### Step 7: Final Structure
```
linkedin-job-analytics/
├── README.md                    ← Single comprehensive
├── requirements.txt
├── .gitignore
├── data/
│   └── postings.csv
├── notebooks/
│   ├── assignment-1/
│   ├── assignment-2/
│   ├── assignment-3/
│   ├── assignment-4/
│   └── assignment-5/
├── visualizations/
│   ├── Q1a.png
│   ├── Bubble.gif
│   └── ... (all with original names)
├── sketches/
│   ├── Q1a.png
│   └── ...
└── web-app/
    ├── index.html
    ├── script.js
    ├── styles.css
    └── data/
