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

> Each node shows:
>
> * Feature used for split
> * Threshold value
> * Class distribution
> * Gini/Entropy score

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

- Let’s implement a simple decision tree using **Scikit-learn**:

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.datasets import load_iris
from sklearn import tree

X, y = load_iris(return_X_y=True)
clf = DecisionTreeClassifier(max_depth=3)
clf.fit(X, y)

tree.plot_tree(clf, feature_names=load_iris().feature_names)
```