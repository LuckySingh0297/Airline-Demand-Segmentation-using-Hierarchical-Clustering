# Airline-Demand-Segmentation-using-Hierarchical-Clustering
Segment airlines based on passenger traffic and flight frequency using Hierarchical Clustering to improve airport resource allocation and operational efficiency.
# ✈️ Airline Demand Segmentation using Hierarchical Clustering

---

## 📌 Business Problem

Airports and airline companies need to optimize **operational efficiency** and **resource allocation** in the face of increasing air traffic.

Different airlines operate at varying levels of passenger demand and flight frequency, making it difficult to:

* Allocate gates and staff efficiently
* Reduce congestion and delays
* Maximize revenue opportunities

👉 **Goal:** Segment airlines based on traffic demand to enable data-driven decision-making.

---

## 🎯 Objective

Cluster airlines based on:

* **Flight Count** (number of flights per airline)
* **Total Passengers** (overall passenger traffic)

👉 Identify:

* High-demand airlines
* Medium-demand airlines
* Low-demand airlines

---

## 💼 Business Impact

This project helps:

* Optimize **airport resource allocation** (gates, staff, scheduling)
* Reduce **congestion and delays**
* Improve **passenger experience**
* Enable **data-driven revenue strategies**

---

## 🔄 Approach (CRISP-ML(Q))

### 1. Business & Data Understanding

* Defined objective: Airline segmentation
* Dataset includes airline names and passenger traffic

### 2. Data Preparation

* Loaded dataset using Pandas
* Stored and processed data using SQL
* Aggregated:

  * Flight count per airline
  * Total passengers per airline

### 3. Feature Engineering

* Created key features:

  * `flight_count`
  * `total_passengers`
  * `passenger_per_flight` *(efficiency metric)*

### 4. Data Preprocessing

* Removed outliers using **IQR method**
* Applied **Standard Scaling**

### 5. Model Building

* Algorithm: **Hierarchical Clustering (Agglomerative)**
* Linkage method: **Ward**
* Used **Dendrogram** to determine optimal clusters

### 6. Model Evaluation

Used multiple metrics:

* **Silhouette Score** → cluster separation
* **Calinski-Harabasz Score** → cluster compactness
* **Davies-Bouldin Index** → cluster similarity (lower is better)

---

## 📊 Results & Insights

### 🔹 Cluster Summary

| Cluster | Description                          |
| ------- | ------------------------------------ |
| 0       | High Traffic / Dominant Airlines     |
| 1       | Medium Demand / Stable Airlines      |
| 2       | Low Traffic / Underutilized Airlines |

---

### 🔹 Key Insights

* A small number of airlines contribute to the majority of passenger traffic (**Pareto principle**)
* High-demand airlines are the **primary drivers of airport congestion**
* Medium-demand airlines show **growth potential**
* Low-demand airlines can help **balance airport load**

---

### 💡 Business Recommendations

* Prioritize high-demand airlines for **gate allocation and scheduling**
* Optimize medium-demand airlines to increase efficiency
* Use low-demand airlines to manage **off-peak operations**

---

## 🛠 Tech Stack

* **Python** (Pandas, NumPy, Matplotlib, Scikit-learn)
* **SQL (MySQL + SQLAlchemy)**
* **SciPy (Dendrogram)**

---

## 📁 Project Structure

```
Airline-Clustering/
│
├── data/
│   └── AirTraffic_Passenger_Statistics.csv
│
├── src/
│   └── clustering.py
│
├── output/
│   └── Airline_Clusters.csv
│
└── README.md
```

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/airline-clustering.git
```

2. Install dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn scipy sqlalchemy pymysql
```

3. Run the project:

```bash
python clustering.py
```

---

## ⚠️ Limitations

* Limited features (no route-level or time-based data)
* Static analysis (no real-time updates)
* Outlier removal may impact interpretation

---

## 🔮 Future Improvements

* Add time-series analysis (seasonal demand)
* Include route-level and pricing data
* Compare with other clustering methods (K-Means, DBSCAN)
* Build interactive dashboard (Power BI / Dash)

---

## 🧠 Key Learnings

* Importance of **feature scaling in clustering**
* Impact of **outlier removal on model performance**
* Value of combining **SQL + ML pipeline**
* Translating clustering results into **business decisions**

---

## 🙋‍♂️ Author

**Lucky Singh**
Aspiring Data Scientist | Python | Machine Learning

---

## ⭐ Final Note

This project demonstrates how **unsupervised learning** can be applied to solve real-world business problems and drive **data-driven decision-making** in the aviation industry.

---
