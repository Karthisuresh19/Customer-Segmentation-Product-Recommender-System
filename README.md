# Customer Segmentation & Product Recommender System

An end-to-end data science project focused on analyzing customer behavior, segmenting customers using RFM analysis, and providing personalized product recommendations based on user similarities.

---

## Table of Contents
- [Introduction](#introduction)
- [Key Features](#key-features)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
  - [Customer Segmentation (RFM)](#customer-segmentation-rfm)
  - [Product Recommender System](#product-recommender-system)
- [Getting Started](#getting-started)
  - [Dependencies](#dependencies)
  - [Installation & Usage](#installation--usage)
- [Dataset](#dataset)

---

## Introduction
Understanding customer behavior and preferences is crucial for tailoring marketing strategies and enhancing customer satisfaction. This project employs **RFM (Recency, Frequency, Monetary)** analysis to segment customers intelligently based on their transaction history. Subsequently, it builds a **collaborative filtering** product recommender system using cosine similarity to suggest highly relevant, unpurchased products to existing users.

## Key Features
- **RFM Analysis:** Data-driven segmentation of customers based on recency, frequency, and monetary values of their purchases.
- **Collaborative Recommender System:** Utilizes user-user cosine similarity to identify relevant unbought products for a user.
- **Data Analytics:** Extensive exploratory data analysis and modeling stored cleanly in Jupyter Notebooks.

## Project Structure
```text
Customer-Segmentation-Product-Recommender-System/
│
├── Customer_Segmentation_RFM.ipynb    # Jupyter Notebook for RFM Analysis & Segmentation
├── Product_Recommender_System.ipynb   # Jupyter Notebook for Cosine Similarity Recommendation
├── Online_shopping.xlsx               # Source dataset (Customer transaction history)
├── DataFrame/                         # Directory containing processed data / dataframes
└── README.md                          # Project documentation (You are here)
```

## Methodology

### Customer Segmentation (RFM)
Customer segmentation is performed using the robust RFM model, which categorizes customers based on three critical criteria:
- **Recency:** How recently a customer has made a purchase.
- **Frequency:** How often a customer makes purchases.
- **Monetary:** The total amount of money a customer has spent.

By analyzing these factors, customers are clustered into distinct groups, allowing businesses to target their marketing efforts effectively.

### Product Recommender System
The recommendation engine identifies similar users using **Cosine Similarity**. The intuition is that if User A and User B share similar purchase histories, products bought by User B (but not yet by User A) can be confidently recommended to User A.

**Workflow:**
1. Compute the cosine similarity matrix between users based on their purchase history.
2. Identify users with the highest similarity scores to a target user.
3. Extract products purchased by those similar users.
4. Filter out products already bought by the target user.
5. Recommend the highest-ranking candidate products.

## Getting Started

### Dependencies
This project requires **Python 3.x** and the following libraries:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib` & `seaborn` (for data visualizations and plots)
- `jupyter` (to run the notebooks)

### Installation & Usage
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Karthisuresh19/Customer-Segmentation-Product-Recommender-System.git
   cd Customer-Segmentation-Product-Recommender-System
   ```

2. **Install the required packages:**
   ```bash
   pip install numpy pandas scikit-learn matplotlib seaborn jupyter
   ```

3. **Ensure Data Availability:**
   Make sure the `Online_shopping.xlsx` dataset file is present in the project root directory.

4. **Run the Notebooks:**
   Launch Jupyter Notebook from your terminal:
   ```bash
   jupyter notebook
   ```
   - Open `Customer_Segmentation_RFM.ipynb` and execute the cells to perform the RFM segmentation.
   - Open `Product_Recommender_System.ipynb` to explore and execute the recommender system.

## Dataset
The project currently uses the dataset provided in the `Online_shopping.xlsx` file. If you use an external or updated dataset, ensure it contains the necessary standard fields (e.g., customer ID, transaction dates, product details, purchase amounts) to remain compatible with the analysis.
