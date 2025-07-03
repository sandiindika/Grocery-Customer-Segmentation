# Customer Segmentation Analysis

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project aims to perform customer segmentation based on demographic and transaction data from a wholesale company. Using *unsupervised clustering* techniques, customers will be grouped into several segments based on shared characteristics. The goal is to better understand customer behavior, allowing the company to maximize the value of each customer and tailor more effective marketing strategies.

## 🎯 The Challenge

Understanding a diverse customer base is crucial for any business. Treating all customers the same can lead to ineffective marketing and missed opportunities. The challenge is to move beyond a one-size-fits-all approach and identify distinct groups within the customer data.

The goal of this project is to build a clustering model that answers the question: *"What are the distinct customer archetypes in our data?"* by using customer personality and transaction data. This will enable the business to create targeted campaigns and improve customer satisfaction.

## 💾 Dataset

The dataset used in this project is **"Customer Personality Analysis"** available on Kaggle.

**[Dataset Link](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)**

## 🛠️ Tech Stack

*   **Data Manipulation & Analysis**: `pandas`, `numpy`
*   **Data Visualization**: `matplotlib`, `seaborn`, `plotly`
*   **Machine Learning**: `scikit-learn`, `scikit-learn-extra`, `yellowbrick`
*   **Environment**: Jupyter Notebook

## 🚀 Getting Started

1.  **Clone the repository or download the project files.**

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # Create the environment
    python -m venv .venv

    # Activate on Windows (PowerShell)
    .\.venv\Scripts\Activate.ps1

    # Activate on macOS/Linux
    source .venv/bin/activate
    ```

3.  **Install the required dependencies from within the notebook:**
    Run the first few cells in the notebook to install `scikit-learn-extra` and `yellowbrick`.

4.  **Launch Jupyter Notebook and open `notebook.ipynb`**.

## 📊 Analysis Workflow

The analysis in this notebook follows these steps:

1.  **Data Cleaning:**
    *   Handling missing values in the `Income` column by removing the corresponding rows.

2.  **Feature Engineering:**
    *   Created new features like `Customer_For`, `Age`, `Spent`, `Living_With`, `Children`, `Family_Size`, and `Is_Parent` to better represent customer characteristics.
    *   Simplified the `Education` and `Marital_Status` categories.
    *   Removed redundant or irrelevant features.

3.  **Outlier Handling:**
    *   Removing outliers in the `Age` and `Income` features to improve model quality.

4.  **Data Preprocessing:**
    *   **Label Encoding:** Converting categorical features (`Education`, `Living_With`) into a numerical format.
    *   **Standard Scaling:** Scaling all numerical features to have a uniform distribution.

5.  **Dimensionality Reduction:**
    *   Using **Principal Component Analysis (PCA)** to reduce the data's dimensions to 3 principal components, which capture most of the data's variance.

6.  **Clustering Modeling:**
    *   **Elbow Method:** Using `KElbowVisualizer` with a K-Means model to determine the optimal number of clusters (`k`). The result shows that **k=4** is the best number of clusters.
    *   **K-Medoids:** Applying the K-Medoids algorithm to group the data into the 4 determined segments.

7.  **Visualization:**
    *   Creating a 3D scatter plot visualization of the clustering results to see the distribution of each customer segment.

## 📄 License

This project is licensed under the MIT License.