Project Report:
🧑‍💼 Customer Segmentation using K-Means Clustering
📌 Overview
This project demonstrates an end-to-end Data Analytics workflow using K-Means Clustering to segment customers based on their age and spending behavior.
The objective is to:
•	Identify different customer groups
•	Understand spending patterns
•	Enable data-driven business decisions
This project showcases strong skills in EDA, clustering, visualization, and business interpretation.

📊 Dataset
•	Source:
o	Real dataset (customers.csv) (if available)
o	Synthetic dataset generated using make_blobs (fallback)
•	Features:
o	Age
o	Spending Score (1–15000)

🛠️ Tools & Technologies
•	Python 🐍
•	Pandas & NumPy
•	Matplotlib & Seaborn
•	Scikit-learn (K-Means Clustering)

🔄 Project Workflow (Step-by-Step)
1️⃣ Data Loading
•	Loaded dataset from CSV
•	If unavailable, generated synthetic dataset
df = pd.read_csv("customers.csv")

2️⃣ Data Visualization (Before Clustering)
•	Scatter plot to understand raw data distribution
•	Observed patterns between Age and Spending Score
plt.scatter(df["Age"], df["Spending Score (1-15000)"])

3️⃣ Feature Selection
•	Selected relevant features for clustering
X = df[["Age", "Spending Score (1-15000)"]]

4️⃣ Finding Optimal Clusters (Elbow Method)
•	Calculated inertia for different K values
•	Identified optimal number of clusters
kmeans = KMeans(n_clusters=k)
kmeans.fit(X)
📊 Insight:
•	Elbow point observed at K = 4 → optimal clusters

5️⃣ Apply K-Means Clustering
•	Trained model with optimal clusters
kmeans = KMeans(n_clusters=4)
df["Cluster"] = kmeans.fit_predict(X)

6️⃣ Cluster Visualization
•	Visualized clusters using scatter plot
•	Different colors represent different customer segments
plt.scatter(df["Age"], df["Spending Score"], c=df["Cluster"])

7️⃣ Customer Segmentation (Business Labels)
Assigned meaningful labels to clusters:
Cluster	Segment
0	High Spenders (Young)
1	Low Spenders (Older)
2	Moderate Spenders
3	High Spenders (Older)

8️⃣ Insights & Interpretation
•	Identified 4 distinct customer groups
•	High-value customers detected
•	Clear separation based on age and spending behavior

📊 Key Results
•	Successfully segmented customers into 4 groups
•	Provided business-friendly labels for decision-making
•	Visualized patterns clearly using clustering

📈 Sample Output
High Spenders (Young): 50
Moderate Spenders: 60
Low Spenders (Older): 45
High Spenders (Older): 45

📁 Project Structure
📁 customer-segmentation
│
├── data/
├── notebooks/
├── clustering.py
├── README.md

🚀 How to Run the Project
1. Clone Repository
git clone https://github.com/your-username/customer-segmentation.git
cd customer-segmentation
2. Install Dependencies
pip install pandas numpy matplotlib seaborn scikit-learn
3. Run the Script
python clustering.py

📊 Dashboard & Reporting (Optional Enhancement)
•	Create Power BI Dashboard:
o	Customer segments distribution
o	Spending behavior analysis
o	Age vs Spending trends
•	Create presentation using Gamma / PowerPoint:
o	Problem statement
o	Approach
o	Visual insights
o	Business recommendations

💡 Future Improvements
•	Use real-world customer dataset
•	Apply advanced clustering (DBSCAN, Hierarchical)
•	Add feature scaling for better accuracy
•	Deploy as interactive app (Streamlit)

👨‍💻 Author
Taqhi Ma
Data Analyst | Machine Learning Enthusiast & Reseacher 🚀
