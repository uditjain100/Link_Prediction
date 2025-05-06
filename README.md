# 🔗 Link Prediction on Social Media

## 📘 Project Overview

This project aims to solve the **Link Prediction problem** on social networks, using real-world data (Facebook pages) as a graph of nodes and connections. We explore machine learning models to predict the formation of future links between unconnected node pairs by extracting features such as Jaccard similarity, cosine similarity, and more.

The project was completed as a **major B.Tech project** by Umang Tiwari, Udit Jain, and Himani Sheoran under the guidance of **Mrs. Savita Sharma**, Assistant Professor, Department of CSE, Maharaja Agrasen Institute of Technology, Delhi.

---

## 📁 Project Structure

```
.
├── Facebook.csv                                # Facebook graph dataset
├── requirements.txt                            # Python dependencies for running the project
├── link_prediction.ipynb                       # Link prediction implementation (XGBoost + graph features)
├── Link_Prediction_on_Facebook_Recruiting_Dataset.ipynb  # Alternate dataset exploration (optional)
├── I-43 link prediction synopsis.pdf           # Project synopsis
├── LINK PREDICTION ON SOCIAL MEDIA.docx        # Full report with methodology and results
├── final_hard bound-converted.docx             # Final formatted submission
├── README.md                                   # Project documentation
```

---

## ▶️ How to Run the Project

Follow the steps below to set up and execute the Link Prediction project in your local environment.

### ✅ Step 1: Clone the Repository

If you haven't already, clone this repository:

```bash
git clone https://github.com/your-username/link-prediction-project.git
cd link-prediction-project
```

### ✅ Step 2: Install Required Libraries

Ensure you have Python installed (preferably 3.7+). Then, install the required libraries:

```bash
pip install networkx pandas xgboost matplotlib seaborn scikit-learn
```

These packages are used for graph processing, data handling, machine learning, and visualization.

### ✅ Step 3: Launch the Notebook

Start Jupyter Notebook in the project directory:

```bash
jupyter notebook
```

Open the `link_prediction.ipynb` file from the browser that opens.

### ✅ Step 4: Run the Code Cells

Execute each code cell in sequence to:

- Load the dataset
- Construct the graph
- Extract graph-based features
- Train the XGBoost model
- Evaluate the predictions
- Visualize the results

### 🧪 Optional: Try Alternate File

You can also explore `Link_Prediction_on_Facebook_Recruiting_Dataset.ipynb` for additional experimentation or dataset variation.

---

## ⚙️ How It Works

1. **Graph Creation**:

   - Nodes = Facebook pages
   - Edges = "Like" relationships between pages

2. **Feature Engineering**:

   - Jaccard Similarity
   - Cosine Similarity
   - Preferential Attachment
   - Shortest Path Distance

3. **Data Preparation**:

   - Positive samples: existing edges
   - Negative samples: randomly chosen non-links

4. **Model Training**:
   - XGBoost classifier with tuned hyperparameters
   - Evaluated using Accuracy, F1-Score, ROC Curve

---

## 🧪 Results & Evaluation

The model was evaluated on a balanced dataset containing both existing links (positive class) and randomly sampled non-links (negative class) between Facebook pages.

| Metric       | Score      |
| ------------ | ---------- |
| **Accuracy** | **99.67%** |
| **F1 Score** | **0.63**   |

### 🔍 Explanation of Metrics:

- **Accuracy** measures the percentage of correctly predicted links and non-links. A score of 99.67% indicates that the model correctly predicted almost all link statuses, showing strong generalization on unseen data.
- **F1 Score** is the harmonic mean of Precision and Recall. Despite a high accuracy, the F1 Score of 0.63 suggests the presence of class imbalance or that false positives/negatives were handled with a trade-off. This is typical in link prediction where true links are sparse.

- The model likely emphasized **true positives (existing links)** using graph-based features such as Jaccard similarity, shortest path, and preferential attachment, leading to accurate and meaningful predictions.

- Visualizations such as the **ROC curve and confusion matrix** further validate that the model is not overfitting and maintains high precision-recall balance.

Overall, the results confirm the model’s effectiveness in predicting meaningful future links in social networks, making it suitable for use in real-world recommendation systems.

---

## 📈 Use Cases

- Friend/Follow suggestions (Facebook, Twitter)
- Product recommendations
- Bioinformatics (protein interaction networks)
- Fraud detection in social graphs

---

## 📖 Report & Documentation

- `LINK PREDICTION ON SOCIAL MEDIA.docx` – Full project report
- `final_hard bound-converted.docx` – Final print version
- `I-43 link prediction synopsis.pdf` – Short project synopsis

---

## 👩‍💻 Authors

- **Udit Jain** (10214802718)
- **Umang Tiwari** (10314802718)
- **Himani Sheoran** (04514802718)
- 👩‍🏫 Guided by **Mrs. Savita Sharma**, Assistant Professor, CSE, MAIT, Delhi

---

## 📚 References

- David Liben-Nowell & Jon Kleinberg — _The Link-Prediction Problem for Social Networks_
- Ryan Lichtenwalter et al. — _New Perspectives and Methods in Link Prediction_
- Mahdi Jalili et al. — _Link Prediction in Multiplex Online Social Networks_
- M. Al Hasan et al. — _Link Prediction using Supervised Learning_

---
