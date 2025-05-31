# **Seaborn Visualization Guide**

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## **1. Bar Plot**

### **Dataset Import**

```python
# Part - 1
import seaborn as sns

# part - 2
import matplotlib.pyplot as plt

# Part -3
df = sns.load_dataset("penguins")

# Part - 4
print(df.head())
```

<br/>
<br/>

### **API Outline**
| Input       | Description                          |
| ----------- | ------------------------------------ |
| `x`         | categorical variable (str)           |
| `y`         | numeric variable (str)               |
| `data`      | DataFrame                            |
| `hue`       | category for color separation        |
| `ci`        | confidence interval                  |
| `palette`   | color palette                        |
| `estimator` | aggregation function (default: mean) |

<br/>
<br/>

### **Sample Example**

```python
# Part - 1
sns.barplot(
    y="body_mass_g",
    x="island",
    data=df,
    palette="Blues",
    estimator=sum,
)

# Part - 2
plt.title("Total Body Mass by Island")

# Part - 3
plt.show()
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## **2. Scatter Plot**

### **Dataset Import**

```python
df = sns.load_dataset("penguins")
print(df.head())
```

<br/>
<br/>

### **API Outline**

| Input     | Description              |
| --------- | ------------------------ |
| `x`       | variable for x-axis      |
| `y`       | variable for y-axis      |
| `data`    | DataFrame                |
| `hue`     | color by category        |
| `style`   | marker style by category |
| `size`    | point size               |
| `palette` | color scheme             |

<br/>
<br/>

### **Sample Example**

```python
# Part - 1
sns.scatterplot(
    x="bill_length_mm", 
    y="flipper_length_mm", 
    data=df, 
    hue="species", 
    style="island"
)

# Part - 2
plt.title("Bill Length vs Flipper Length")

# Part - 3
plt.show()
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## **3. Hist Plot**

### **Dataset Import**

```python
df = sns.load_dataset("penguins")
print(df.head())
```

<br/>
<br/>

### **API Outline**

| Input      | Description                                  |
| ---------- | -------------------------------------------- |
| `x`        | numeric variable                             |
| `data`     | DataFrame                                    |
| `bins`     | number of bins                               |
| `kde`      | include KDE line                             |
| `hue`      | color split by category                      |
| `element`  | style of bars (`'bars'`, `'step'`, `'poly'`) |
| `multiple` | `'layer'`, `'stack'`, `'dodge'`              |

<br/>
<br/>

### **Sample Example**

```python
# Part - 1
sns.histplot(
    x="body_mass_g", 
    data=df, 
    bins=30, 
    kde=True, 
    hue="species", 
    element="step", 
    multiple="stack"
)

# Part - 2
plt.title("Distribution of Body Mass")

# Part - 3
plt.show()
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## **4. KDE Plot**

### **Dataset Import**

```python
df = sns.load_dataset("penguins")
print(df.head())
```

<br/>
<br/>


### **API Outline**

| Input       | Description                                    |
| ----------- | ---------------------------------------------- |
| `x`         | numeric variable                               |
| `data`      | DataFrame                                      |
| `hue`       | category separation                            |
| `shade`     | fill the curve                                 |
| `bw_adjust` | bandwidth adjustment                           |
| `multiple`  | layout option (`'layer'`, `'stack'`, `'fill'`) |

<br/>
<br/>

### **Sample Example**

```python
# Part - 1
sns.kdeplot(
    data=df, 
    x="flipper_length_mm",
    hue="species",
    shade=True,
    bw_adjust=0.5,
)

# Part - 2
plt.title("KDE of Flipper Length")

# Part - 3
plt.show()
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## **5. Box Plot**

### **Dataset Import**

```python
df = sns.load_dataset("penguins")
print(df.head())
```

### **API Outline**

| Input     | Description                    |
| --------- | ------------------------------ |
| `x`       | categorical variable           |
| `y`       | numeric variable               |
| `data`    | DataFrame                      |
| `hue`     | category for color split       |
| `palette` | color palette                  |
| `orient`  | `'v'` or `'h'` for orientation |
| `width`   | box width                      |

### **Sample Example**

```python
# Part - 1
sns.boxplot(
    data=df,
    x="species", 
    y="bill_depth_mm", 
    palette="Set2"
)

# Part - 2
plt.title("Box Plot of Bill Depth by Species")

# Part - 3
plt.show()
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
