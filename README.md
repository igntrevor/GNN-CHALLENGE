# 🎓 GNN-Challenge: The Neural Citation Network

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Library](https://img.shields.io/badge/Library-DGL%20%26%20PyTorch-orange) ![Status](https://img.shields.io/badge/Auto--Grader-Active-green)

**Can you predict the topic of a scientific paper using Graph Neural Networks?**

## 🧠 The Objective
You are tasked with building a node classification model for the **CiteSeer** citation network. 
* **Nodes:** 3,327 Papers.
* **Edges:** 4,732 Citations.
* **Classes:** 6 Research Topics (AI, ML, DB, etc.).

**The Challenge:** You must beat the baseline **GCN** (Graph Convolutional Network) by implementing a **GAT** (Graph Attention Network) and tuning your hyperparameters.

---

## 🏁 How to Participate (The Workflow)

### 1. Setup
1.  **Fork** this repository to your own GitHub account.
2.  **Clone** your fork to your local machine (or open it in Google Colab).
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

### 2. The Baseline (Task 1)
Run the starter code to generate your first prediction.
```bash
python starter_code/baseline.py

This trains a simple GCN.

It generates a file: submissions/my_submission.csv.

Goal: Pass the baseline threshold (> 65%).

3. The Upgrade (Task 2 & 3)
Modify starter_code/baseline.py to improve your accuracy (see Tasks & References below).

. Submit & Get Graded
Commit your changes and the new CSV file:

git add starter_code/baseline.py submissions/my_submission.csv
git commit -m "My GNN Submission"
git push origin main

Go to your GitHub repository and open a Pull Request to the original repository.

🤖 Wait 30 seconds... The Auto-Grader Robot will post a comment on your Pull Request with your accuracy score!

!📚 Tasks & Lecture References
Task 1: 

Establish a Baseline (GCN)The baseline.py file implements a standard 2-layer GCN.
Reference: Video 3.4: Graph Convolutional Networks 
(GCN)Target Accuracy: ~68-70%Task 

2: Implement Graph Attention (GAT)
Modify the model class to use GATConv layers instead of GraphConv.
Reference: Video 3.5: Graph Attention Networks (GAT)Theory: How does the attention mechanism ($\alpha_{ij}$) change how neighbor information is aggregated?
Target Accuracy: > 75%

Task 3: Hyperparameter TuningYou will likely need to tune the model to reach the Distinction level.
Reference: Video 4.2: Neighbor Sampling & TrainingExperiments to try:num_heads (Essential for GAT).hidden_feats (Try increasing from 16 to 64).dropout (Try 0.5 to prevent overfitting).

Level,Requirement,Status
Fail,< 65% Accuracy,❌ Keep Trying
Pass,> 65% Accuracy,✅ Completed Task 1
Distinction,> 75% Accuracy,🌟 Completed Task 2 (GAT)

Project Structure
starter_code/baseline.py: The main script. Edit this!

data/: Contains the public training and validation data.

submissions/: Where your results are saved.

requirements.txt: Python dependencies.

GOOD LUCK! 