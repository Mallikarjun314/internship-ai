# Decision Trees


\
\
\
\
\


## What is a Decision Tree?

> A **Decision Tree** is a supervised machine learning algorithm used for **classification** and **regression** problems.

- Think of it like a **flowchart**:
- At each **internal node**, a decision is made based on a feature.
- At the **leaf nodes**, a final prediction is made.

#### Example :

- Imagine you're deciding whether to play tennis:
- If it's sunny → check humidity → if high → don’t play.
- If it’s overcast → always play.
- If it’s rainy → check wind → if strong → don’t play.
- This logic forms a **tree**: feature-based splits leading to outcomes.

\
\
\
\
\


## Building a Decision Tree (Step-by-Step)

### 2.1 The Data

> Let’s say we have this sample data:

| Weather  | Humidity | Play Tennis |
| -------- | -------- | ----------- |
| Sunny    | High     | No          |
| Overcast | Normal   | Yes         |
| Rainy    | High     | No          |
| Sunny    | Normal   | Yes         |

> We want the tree to **learn rules** from the data.

\
\
\
\
\


### 2.2 Splitting Criteria

To decide **which feature to split on**, we use **metrics** like:

* **Gini Impurity**
* **Entropy / Information Gain**
* **Mean Squared Error (for regression)**

> **Entropy** measures the "purity" of the data at a node.

**Entropy formula:**

- $Entropy(S) = - \sum p_i \log_2(p_i)$

- The goal is to **maximize Information Gain**, which is:

- $IG = Entropy(parent) - \sum (\text{Weighted entropy of children})$

\
\
\
\
\

### 2.3 Building the Tree

The tree is built recursively:

* Choose the best feature to split.
* Partition the data.
* Recurse on each subset.

This continues until:

* All data is pure (i.e., same label)
* Maximum depth reached
* Minimum number of samples per node

\
\
\
\
\


### Visualizing the Tree

> Tools like **Scikit-learn** provide `DecisionTreeClassifier` and `plot_tree()` to visualize the tree.

Each node shows:

* Feature used for split
* Threshold value
* Class distribution
* Gini/Entropy score

\
\
\
\
\


### Advantages & Limitations

#### ✅ Pros:

* Easy to understand and interpret
* No need for feature scaling
* Can handle numerical and categorical data

#### ❌ Cons:

* Prone to **overfitting**
* Unstable to small changes in data
* Greedy splitting may miss optimal solutions

\
\
\
\
\

### Pruning Decision Trees

A tree that grows too deep can **overfit** the training data.

- **Pruning** means cutting back the tree to improve generalization.
- **Pre-pruning** (limit depth, min samples)
- **Post-pruning** (grow full tree → then trim)

> Tools: Scikit-learn uses parameters like `max_depth`, `min_samples_split`, `ccp_alpha` (Cost Complexity Pruning).

\
\
\
\
\


### Implementation

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.datasets import load_iris
from sklearn import tree

X, y = load_iris(return_X_y=True)
clf = DecisionTreeClassifier(max_depth=3)
clf.fit(X, y)

tree.plot_tree(clf, feature_names=load_iris().feature_names)
```


# Classification Task - Evaluation Metrics

## 1. Confusion Matrix

* Table showing **TP**, **FP**, **TN**, **FN** per class
* Useful for **detailed error analysis**

Example for binary:

```text
               Predicted
              |    0    |  1
       -------------------------
          0   |   TN    |  FP
Actual -------------------------
          1   |   FN    |  TP
```

\
\
\
\
\
\


## 2. Basic Metrics ⭐

### ✅ **Accuracy**

$$
\text{Accuracy} = \frac{\text{TP + TN}}{\text{TP + TN + FP + FN}}
$$

* **Best for**: Balanced datasets
* **Misleading if**: Classes are imbalanced

---

### ✅ **Precision**

$$
\text{Precision} = \frac{\text{TP}}{\text{TP + FP}}
$$

* **Tells you**: Out of all predicted positives, how many were correct
* **Important for**: Minimizing false positives (e.g., spam detection)

---

### ✅ **Recall (Sensitivity, TPR)**

$$
\text{Recall} = \frac{\text{TP}}{\text{TP + FN}}
$$

* **Tells you**: Out of all actual positives, how many were correctly predicted
* **Important for**: Minimizing false negatives (e.g., disease diagnosis)

---

### ✅ **F1 Score**

$$
\text{F1} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision + Recall}}
$$

* **Best for**: Imbalanced datasets
* **Balances**: Precision and Recall

\
\
\
\
\
\
\

## 3. Multi-Class and Averaging Metrics ⭐

* **Normal Average**: Mean of metric for each class (treats all classes equally)
* **Weighted Average**: Like macro, but weighted by number of instances per class

\
\
\
\
\
\


## **4. ROC and AUC**

### ✅ **ROC Curve**

* Plots **True Positive Rate** (Recall) vs **False Positive Rate**

### ✅ **AUC (Area Under Curve)**

* **AUC = 1.0**: Perfect
* **AUC = 0.5**: Random guessing
* Useful for **binary classifiers**

\
\
\
\
\
\


## **5. Precision-Recall (PR) Curve**

* More informative than ROC when **positive class is rare**
* Plots **Precision vs Recall** at different thresholds

\
\
\
\
\
\


## **6. Log Loss (Cross-Entropy Loss)**

$$
\text{LogLoss} = -\frac{1}{N} \sum_{i=1}^{N} y_i \log(p_i)
$$

* Penalizes **confident but wrong** predictions
* Lower is better
* Often used during training and evaluation

\
\
\
\
\
\


## 7. Matthews Correlation Coefficient (MCC)

$$
\text{MCC} = \frac{(TP \cdot TN - FP \cdot FN)}{\sqrt{(TP+FP)(TP+FN)(TN+FP)(TN+FN)}}
$$

* Balanced measure even for **imbalanced datasets**
* Range: –1 (inverse) to +1 (perfect)

\
\
\
\
\
\


## Summary Table

| Metric           | Best For                  | Notes                               |
| ---------------- | ------------------------- | ----------------------------------- |
| Accuracy         | Balanced datasets         | Misleading with imbalance           |
| Precision        | Reducing false positives  | Spam filters                        |
| Recall           | Reducing false negatives  | Medical, fraud detection            |
| F1 Score         | Imbalanced data           | Harmonic mean of precision & recall |
| ROC-AUC          | Probabilistic classifiers | Good for ranking ability            |
| PR-AUC           | Imbalanced positive class | Better than ROC in this case        |
| Confusion Matrix | All classifiers           | Visual error breakdown              |
| Log Loss         | Probabilistic output      | Lower is better                     |
| Top-K Accuracy   | Image, NLP (multi-class)  | Used with softmax outputs           |
| MCC              | Any class balance         | Balanced metric for binary class    |
| Cohen’s Kappa    | Human-level tasks         | Inter-rater agreement adjustment    |
