# **ETF Classification and Recommendation System**

This project aims to classify **ETFs (Exchange-Traded Funds)** and **recommend** an ETF to a user based on their financial preferences. Using **machine learning techniques**, we embed ETFs and users into a **shared feature space** to provide personalized recommendations.

---

## **📌 Project Overview**
This project leverages **dimensionality reduction, clustering, and deep learning** to build an ETF recommendation model. The key steps include:

- **Data Preprocessing**: Cleaning and normalizing ETF financial data.
- **Feature Engineering**: Extracting financial and sector-specific features.
- **Dimensionality Reduction**: Applying **PCA (Principal Component Analysis)** to reduce feature space.
- **Clustering ETFs**: Using **K-Means clustering** to categorize ETFs based on financial similarities.
- **Synthetic User Preference Generation**: Simulating user preferences for ETFs.
- **Recommendation Model**: Using **deep learning** to map users and ETFs into a common space and predict ETF preferences.

---

## **📂 Repository Structure**
```
etf-recommendation-system/
├── clustering.ipynb         # ETF clustering & visualization
├── README.md                    # Project documentation
└── LICENSE                       # Open-source license
```

---

## **📊 Data Preprocessing & Feature Engineering**
1. **Dropped irrelevant columns**: Removed identifiers (e.g., ISIN, ticker, labels, etc.).
2. **Converted numerical features**: Standardized financial metrics.
3. **Extracted sector exposure**: Included industry sector breakdowns.
4. **Handled missing values**: Imputed missing values with mean imputation.

---

## **📈 Clustering ETFs**
We used **K-Means clustering** to group ETFs based on financial attributes:
- **Feature selection**: Selected key metrics such as **volatility, Sharpe ratio, sector exposure**.
- **Dimensionality reduction**: Applied **PCA** to avoid the curse of dimensionality.
- **Optimal clusters**: Used the **Elbow method** and **Silhouette score** to determine the best number of clusters.

---

## **🤖 Recommendation Model**
The deep learning model consists of:
- **User & ETF embedding layers**
- **Cosine similarity loss function** to measure ETF-user affinity
- **Contrastive loss for feature space separation**
- **Cross-entropy loss for classification accuracy**

Training strategy:
- **Optimized using Adam optimizer**
- **Batch training for efficiency**
- **Regularization to prevent overfitting**

---

## **🚀 Running the Project**
### **1️⃣ Installation**
Clone the repository and install dependencies:
```bash
git clone https://github.com/your-username/etf-recommendation-system.git
cd etf-recommendation-system
pip install -r requirements.txt
```

### **2️⃣ Data Preprocessing**
Run the preprocessing script to clean and prepare the dataset:
```bash
python src/preprocess.py
```

### **3️⃣ Training the Model**
Train the recommendation system:
```bash
python src/train.py
```

### **4️⃣ Running Recommendations**
Generate ETF recommendations for a user:
```bash
python src/recommend.py --user_id 123
```

---

## **📜 License**
This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## **👤 Author**
**Marc Saliba**  
- **MIT Sloan School of Management (MBAn 2025)**  
- **Operations Research Center (ORC) - Research Assistant**  
- **HEC Paris - Master in Management**  

---

Feel free to reach out with questions or suggestions! 🚀
