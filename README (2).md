# Visual Analytics of LinkedIn Job Postings

A comprehensive visual analytics project analyzing LinkedIn job postings through interactive visualizations, spatial analysis, and dimensionality reduction techniques using Altair and Vega-Lite.

---

## 👥 Group Information

| Name | Email |
|------|-------|
| Sunil Kuruba | skuru@uic.edu |
| Richa Rameshkrishna | rrame11@uic.edu |

---

## 📋 Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Project Structure](#project-structure)
4. [Assignments](#assignments)
   - [Assignment 1: Data Preprocessing](#assignment-1-data-preprocessing)
   - [Assignment 2: Exploratory Visualizations](#assignment-2-exploratory-visualizations)
   - [Assignment 3: Interactive Visualizations](#assignment-3-interactive-visualizations)
   - [Assignment 4: Linked Views & Spatial Analysis](#assignment-4-linked-views--spatial-analysis)
   - [Assignment 5: Dimensionality Reduction](#assignment-5-dimensionality-reduction)
5. [Technologies](#technologies)
6. [How to Run](#how-to-run)
7. [Key Insights](#key-insights)
8. [References](#references)

---

## 🎯 Overview

This project performs comprehensive visual analytics on LinkedIn job postings data, exploring:
- **Temporal trends** in hiring patterns across months and seasons
- **Skill demand** across industries, roles, and experience levels
- **Salary distributions** by geography, experience level, and work type
- **Geographic patterns** in job markets across US states
- **Interactive dashboards** with linked views and coordinated selections
- **Dimensionality reduction** for job posting embeddings using PCA, t-SNE, and UMAP

Through a series of five assignments, we progressively build from basic data preprocessing to sophisticated interactive dashboards with coordinated multi-view visualizations and machine learning-powered embedding analysis.

---

## 📊 Dataset

**Source:** [LinkedIn Job Postings - Kaggle](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings/data)

The dataset contains comprehensive information about job postings from LinkedIn, including:
- **Job Details:** Titles, descriptions, experience levels, work types
- **Company Information:** Company names, industries, sizes, headquarters
- **Compensation:** Salary ranges, pay periods, benefits
- **Geographic Data:** Locations, states, FIPS codes
- **Engagement Metrics:** Views, applications, engagement rates
- **Skills:** Required and preferred skills for each posting
- **Temporal Data:** Posting dates, expiry dates, listing times

**Dataset Size:** Multiple CSV files with thousands of job postings across various industries and locations.

---

## 📁 Project Structure

```
linkedin-job-analytics/
├── README.md
├── requirements.txt
├── data/
│   ├── postings.csv
│   ├── data_science_job_posts_2025.csv
│   ├── data_science_job_posts_2025_clean.csv
│   └── data_science_job_posts_2025_embeddings.csv
├── notebooks/
│   ├── 01-data-preprocessing.ipynb
│   ├── 02-exploratory-visualizations-a.ipynb
│   ├── 02-exploratory-visualizations-b.ipynb
│   ├── 03-interactive-visualizations.ipynb
│   ├── 1-Linked-view-visualizations.ipynb
│   ├── 2-Spatial-visualization.ipynb
│   ├── 3-Linked-spatial-visualization.ipynb
│   ├── Task_1.ipynb
│   ├── Task_2.ipynb
│   ├── Task_3.ipynb
│   ├── 0_Data_cleaning.ipynb
│   ├── 1_Generate_Embedding.ipynb
│   ├── 2_TSNE_and_UMAP.ipynb
│   └── 3_PCA.ipynb
├── visualizations/
│   ├── static/
│   └── interactive/
└── web-app/
    ├── index.html
    ├── script.js
    └── styles.css
```

---

## 📚 Assignments

### Assignment 1: Data Preprocessing

**Notebook:** `01-data-preprocessing.ipynb`

**Objective:** Load, clean, and prepare the LinkedIn job postings dataset for analysis.

**Key Tasks:**
- Loaded multiple CSV files (companies, job postings, benefits, skills)
- Cleaned and standardized column names and data types
- Handled missing values and outliers
- Created derived features (engagement rates, salary calculations, state extraction)
- Merged related datasets for comprehensive analysis
- Exported cleaned data for visualization tasks

**Output:** Clean, structured dataset ready for exploratory data analysis and visualization.

---

### Assignment 2: Exploratory Visualizations

**Notebooks:** 
- `02-exploratory-visualizations-a.ipynb`
- `02-exploratory-visualizations-b.ipynb`

**Objective:** Create static visualizations to explore different dimensions of the job posting data.

#### Visualization 1: Monthly Job Posting Trends (Temporal)
- **Type:** Line chart with area fill
- **Insight:** Job postings show seasonality with peaks in March and September
- **Analytical Dimension:** Temporal patterns

#### Visualization 2: Skill Demand Ranking (Categorical)
- **Type:** Horizontal bar chart
- **Insight:** Python, SQL, and machine learning are top requested skills
- **Analytical Dimension:** Categorical comparison

#### Visualization 3: Remote Work Distribution by State (Bubble Chart)
- **Type:** Bubble chart
- **Variables:** 
  - Size = Total postings per state
  - Color = Percentage of remote jobs
- **Insight:** California and New York lead in total postings; some states show higher remote work percentages

#### Visualization 4: Salary Distribution by Experience Level (Box Plot)
- **Type:** Box plot with annualized salary normalization
- **Insight:** Clear salary progression from entry-level to executive positions
- **Analytical Dimension:** Distribution and comparison

#### Visualization 5: Job Postings by State and Experience Level (Heatmap)
- **Type:** 2D heatmap
- **Insight:** Most jobs concentrated in major tech hubs at mid-senior levels
- **Analytical Dimension:** Hierarchical/categorical

---

### Assignment 3: Interactive Visualizations

**Notebook:** `03-interactive-visualizations.ipynb`

**Objective:** Enhance static visualizations with Vega-Lite interactivity features.

#### Interactive Feature 1: Skill Demand with Top-N Slider
- **Interaction:** Parameter-driven slider (5-50 skills)
- **Feature:** Dynamic filtering with click-to-highlight
- **Benefit:** Users explore different skill ranking depths

#### Interactive Feature 2: Salary Distribution with Faceted Views
- **Interaction:** Multi-view composition with tooltips
- **Feature:** Layered visualizations showing different aggregations
- **Benefit:** Compare salary patterns across multiple dimensions

#### Interactive Feature 3: Geographic Salary Map
- **Interaction:** Hover tooltips on choropleth map
- **Feature:** Color-coded US states by average salary
- **Benefit:** Immediate geographic salary comparison

**Enhanced Elements:**
- Rich tooltips showing multiple data points
- Conditional formatting based on selections
- Smooth animations and transitions
- Responsive design for different screen sizes

---

### Assignment 4: Linked Views & Spatial Analysis

**Notebooks:**
- `Task_1.ipynb` - Linked View Visualizations
- `Task_2.ipynb` - Spatial Visualization
- `Task_3.ipynb` - Coordinated Multi-View Dashboard
- `1-Linked-view-visualizations.ipynb`
- `2-Spatial-visualization.ipynb`
- `3-Linked-spatial-visualization.ipynb`

**Objective:** Create coordinated visualizations with linked interactions and spatial analysis.

#### Task 1: Linked View Visualizations

**Visualization 1: Brush Selection**
- **Components:** Scatter plot (salary vs engagement) + linked bar chart
- **Interaction:** Brush selection on scatter → filters bar chart
- **Insight:** Identify salary-engagement patterns and corresponding work types

**Visualization 2: Click Selection with Detail View**
- **Components:** Heatmap (experience × work type) + detail histogram
- **Interaction:** Click heatmap cell → shows detailed salary distribution
- **Insight:** Drill down from aggregate patterns to detailed distributions

#### Task 2: Spatial Visualization

**Geographic Choropleth Map**
- **Type:** US states map with Albers USA projection
- **Encoding:** Color = average salary by state
- **Features:** 
  - FIPS code mapping for accurate state identification
  - Tooltip showing job count, avg salary, remote percentage
  - Clean state extraction and validation

#### Task 3: Coordinated Multi-View Dashboard

**Comprehensive Dashboard with Three-Level Interaction:**

1. **Map → All Views** (Geographic filtering)
   - Click state on map → filters scatter and bar charts
   - Visual feedback: selected states highlighted, others dimmed

2. **Scatter → Bar Chart** (Attribute filtering)
   - Brush scatter plot → filters work type distribution
   - Works in conjunction with map selection

3. **Hover Tooltips** (Details on demand)
   - All views provide rich contextual information
   - Coordinated highlighting across views

**User Flow:**
- Start with geographic overview (map)
- Filter to specific state
- Explore salary-engagement patterns (scatter)
- Drill down to work type distributions (bar chart)

---

### Assignment 5: Dimensionality Reduction

**Notebooks:**
- `0_Data_cleaning.ipynb` - Advanced data cleaning
- `1_Generate_Embedding.ipynb` - Feature engineering and embedding generation
- `2_TSNE_and_UMAP.ipynb` - Non-linear dimensionality reduction
- `3_PCA.ipynb` - Linear dimensionality reduction

**Objective:** Apply machine learning techniques to visualize high-dimensional job posting features.

#### Data Cleaning Pipeline
**Notebook:** `0_Data_cleaning.ipynb`

**Features:**
- State extraction using regex from headquarter locations
- FIPS code mapping for geographic data
- Salary parsing (range to numeric conversion, K notation handling)
- Seniority level normalization
- Skills list parsing and cleaning
- Deduplication using composite keys

#### Embedding Generation
**Notebook:** `1_Generate_Embedding.ipynb`

**Process:**
- Feature engineering from job descriptions, titles, skills
- Text vectorization using TF-IDF or word embeddings
- Numerical feature scaling and normalization
- Combined feature matrix creation
- Output: High-dimensional embedding vectors (941 jobs × 105 features)

#### t-SNE and UMAP Analysis
**Notebook:** `2_TSNE_and_UMAP.ipynb`

**Techniques:**
- **t-SNE:** Preserves local structure, reveals clusters
- **UMAP:** Faster, preserves both local and global structure
- **Comparison:** Evaluate different perplexity/n_neighbors settings

**Visualizations:**
- 2D scatter plots colored by industry, experience level, salary
- Interactive exploration of job clusters
- Pattern identification in job similarities

#### PCA Analysis
**Notebook:** `3_PCA.ipynb`

**Process:**
1. Feature standardization (mean=0, variance=1)
2. PCA transformation to 2 components
3. Explained variance analysis

**Results:**
- PC1 explains 5.91% of variance
- PC2 explains 4.31% of variance
- Total: 10.22% variance captured in 2D
- Linear relationships between job features

**Interpretation:**
- PCA captures broad patterns (industry, seniority)
- Low explained variance suggests complex non-linear relationships
- Complements t-SNE/UMAP for comprehensive analysis

---

## 🛠 Technologies Used

### Data Processing
- **pandas** - Data manipulation and cleaning
- **numpy** - Numerical computations
- **scikit-learn** - Machine learning and dimensionality reduction

### Visualization
- **Altair** - Declarative statistical visualization
- **Vega-Lite** - Grammar of interactive graphics
- **vega_datasets** - Sample and geographic datasets

### Dimensionality Reduction
- **PCA** - Linear dimensionality reduction
- **t-SNE** - Non-linear manifold learning
- **UMAP** - Uniform Manifold Approximation and Projection

### Web Technologies
- **HTML/CSS** - Web app structure and styling
- **JavaScript** - Interactivity and dynamic content
- **Jupyter Notebook** - Interactive development environment

---

## 🚀 How to Run

### Prerequisites

```bash
# Install Python 3.8+
# Install required packages
pip install -r requirements.txt
```

### Requirements File Content

```
pandas>=1.5.0
numpy>=1.23.0
altair>=5.0.0
vega_datasets>=0.9.0
scikit-learn>=1.3.0
jupyter>=1.0.0
matplotlib>=3.7.0
umap-learn>=0.5.0
```

### Running Notebooks

1. **Navigate to project directory:**
   ```bash
   cd linkedin-job-analytics
   ```

2. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

3. **Open notebooks in order:**
   - Start with `01-data-preprocessing.ipynb`
   - Proceed through exploratory and interactive visualizations
   - Complete with dimensionality reduction notebooks

4. **Run cells sequentially:**
   - Execute cells from top to bottom
   - Wait for each cell to complete before proceeding
   - Check outputs and visualizations

### Running Web Application

1. **Option 1 - Direct File Opening:**
   - Navigate to `web-app/` directory
   - Double-click `index.html`

2. **Option 2 - Local Server:**
   ```bash
   cd web-app
   python -m http.server 8000
   ```
   - Open browser to `http://localhost:8000`

---

## 💡 Key Insights

### Temporal Patterns
- **Hiring Seasonality:** Clear peaks in March and September suggest academic calendar and fiscal year influences
- **Low Periods:** February, August, and November show consistent hiring slowdowns

### Geographic Distribution
- **Tech Hubs Dominate:** California, New York, and Washington lead in job postings
- **Salary Variation:** Coastal states show 20-30% higher average salaries
- **Remote Work:** Increasing trend, with some states offering 40%+ remote positions

### Skill Demands
- **Core Technical Skills:** Python, SQL, Machine Learning top every category
- **Soft Skills Gap:** Communication and leadership mentioned less frequently
- **Emerging Technologies:** Cloud platforms, Docker, Kubernetes showing growth

### Compensation Insights
- **Experience Premium:** Executive roles earn 3-4x entry-level positions
- **Salary Transparency:** Only ~60% of postings disclose salary information
- **Pay Period Variance:** Annual vs hourly significant factor after normalization

### Job Market Structure
- **Clustering Patterns:** Distinct clusters by industry, seniority, and location
- **Work Type Distribution:** Full-time dominates (85%), contract growing
- **Engagement Correlation:** Higher salaries don't always mean higher engagement

### Dimensionality Reduction Findings
- **PCA Limitations:** 10% variance suggests non-linear relationships
- **t-SNE Clusters:** Reveals 5-6 distinct job category clusters
- **UMAP Performance:** Better preserves global structure than t-SNE

---

## 📖 References

### Dataset
- [LinkedIn Job Postings - Kaggle](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings/data)

### Libraries & Tools
- [Altair Documentation](https://altair-viz.github.io/)
- [Vega-Lite Specification](https://vega.github.io/vega-lite/)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [UMAP Documentation](https://umap-learn.readthedocs.io/)

### Visualization Techniques
- Interactive Visualization Grammar (Vega-Lite)
- Coordinated Multiple Views (CMV)
- Brushing and Linking
- Focus + Context Techniques

### Dimensionality Reduction
- Principal Component Analysis (PCA)
- t-Distributed Stochastic Neighbor Embedding (t-SNE)
- Uniform Manifold Approximation and Projection (UMAP)

---

## 📄 License

This project is created for educational purposes as part of a visual analytics course.

---

## 🤝 Contributing

This is an academic project. For questions or suggestions, please contact:
- Sunil Kuruba: skuru@uic.edu
- Richa Rameshkrishna: rrame11@uic.edu

---

**Last Updated:** January 2026
