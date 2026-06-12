# 🎬 Netflix Recommendation System

A comprehensive movie recommendation system built using the Netflix Prize Dataset. This project explores multiple collaborative filtering approaches and evaluates their effectiveness in generating personalized movie recommendations.

---

## 📌 Project Overview

Recommendation systems play a crucial role in modern streaming platforms by helping users discover relevant content from massive catalogs.

This project implements and compares multiple recommendation algorithms using the Netflix Prize Dataset to:

* Predict user ratings for unseen movies
* Generate personalized movie recommendations
* Compare recommendation approaches
* Evaluate ranking and prediction performance

---

## 🎯 Objectives

* Learn user preferences from historical ratings
* Generate Top-K movie recommendations
* Compare different collaborative filtering techniques
* Evaluate recommendation quality using industry-standard metrics
* Analyze strengths and limitations of recommendation algorithms

---

## 📂 Dataset

### Netflix Prize Dataset

The Netflix Prize Dataset is one of the most widely used benchmark datasets in recommendation system research.

#### Dataset Statistics

* **100,480,507 ratings**
* **480,189 users**
* **17,770 movies**
* Ratings on a **1–5 star scale**
* Rating timestamps included

Each record contains:

* User ID
* Movie ID
* Rating
* Date

Dataset Source:

https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data

---

## 📊 Exploratory Data Analysis

Several exploratory analyses were conducted to understand user behavior and dataset characteristics.

### Key Findings

* Dataset exhibits **extreme sparsity (>99%)**
* Ratings are positively skewed toward **3–4 stars**
* User activity follows a **power-law distribution**
* Movie popularity follows a **long-tail distribution**
* Approximately **20% of users contribute nearly 80% of ratings**

### Visualizations

* Rating Distribution
* User Activity Distribution
* Movie Popularity Distribution
* Data Sparsity Analysis
* Model Performance Comparison

---

## 🤖 Models Implemented

### 1. User-Based Collaborative Filtering

Recommends movies based on preferences of similar users.

#### Advantages

* Interpretable recommendations
* Simple implementation

#### Limitations

* Sensitive to sparsity
* Scalability challenges

---

### 2. Item-Based Collaborative Filtering

Recommends movies similar to those previously liked by a user.

#### Advantages

* Better scalability
* Stable similarity estimates

#### Limitations

* Reduced effectiveness for rare items

---

### 3. Singular Value Decomposition (SVD)

Matrix factorization approach that learns latent user and movie features.

#### Advantages

* Handles sparse data effectively
* Captures hidden user preferences
* Produces highly personalized recommendations

---

## 📈 Evaluation Metrics

The models were evaluated using:

### RMSE (Root Mean Squared Error)

Measures rating prediction accuracy.

Lower values indicate better performance.

### MAP@10 (Mean Average Precision @ 10)

Measures recommendation ranking quality.

A movie is considered relevant if:

```text
Rating ≥ 3.5
```

Higher values indicate better recommendation quality.

---

## 🏆 Results

| Model         | RMSE       | MAP@10     |
| ------------- | ---------- | ---------- |
| SVD           | **0.9606** | **0.0121** |
| User-Based CF | 1.0008     | 0.0001     |
| Item-Based CF | 1.0167     | 0.0000     |

### Best Model

🏆 **SVD (Matrix Factorization)**

SVD achieved the best performance in both rating prediction and recommendation ranking.

---

## 💡 Key Insights

### Data Characteristics

* Extreme sparsity is the primary challenge.
* User engagement is highly uneven.
* Popular movies dominate interaction data.

### Model Performance

* SVD significantly outperforms neighborhood-based methods.
* User-Based CF struggles with sparse interactions.
* Item-Based CF provides explainable recommendations but lower accuracy.

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/netflix-recommendation-system.git
cd netflix-recommendation-system
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Netflix_Recommendation_System.ipynb
```

Run all cells sequentially.

---

## 📁 Project Structure

```text
Netflix-Recommendation-System/
│
├── notebooks/
│   └── Netflix_Recommendation_System.ipynb
│
├── images/
│   ├── rating_distribution.png
│   ├── user_activity.png
│   ├── sparsity_analysis.png
│   └── model_comparison.png
│
├── report/
│   └── Technical_Report.pdf
│
├── presentation/
│   └── Final_Presentation.pdf
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 🔮 Future Improvements

Potential enhancements include:

* Neural Collaborative Filtering (NCF)
* Hybrid Recommendation Systems
* Graph Neural Networks
* Transformer-Based Recommendation Models
* Session-Based Recommendations
* Real-Time Recommendation Pipelines
* Cold-Start Mitigation Strategies

---

## 📚 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Surprise Library
* Jupyter Notebook

---

## 👨‍💻 Author

**Rudraksh**
B.Tech Civil Engineering
Indian Institute of Technology Roorkee

---

## 📜 License

This project is developed for academic and educational purposes as part of a recommendation system research and competition project.

---

⭐ If you found this project useful, consider giving the repository a star.


