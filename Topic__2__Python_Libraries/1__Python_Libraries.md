# Python Libraries for AI (Basic)

![Python_Lib_Intro](./images/py-lib-intro.jpg)

## 1. The 4 Basic Libraries

| No. | Library      | Purpose | Installing               |
| --- | ------------ | ------- | ------------------------ |
| 1   | `numpy`      | Arrays  | `pip install numpy`      |
| 2   | `pandas`     | Tables  | `pip install pandas`     |
| 3   | `matplotlib` | Graphs  | `pip install matplotlib` |
| 4   | `seaborn`    | Graphs  | `pip install seaborn`    |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## 2. Installing Libraries

<br/>

> To install library  python
> 
> format : `pip` `install` _______________


<br/>
<br/>
<br/>

```bash
# Type in Terminal

pip install numpy        # Numpy for Arrays
pip install pandas       # Pandas for Tables
pip install matplotlib   # Graphing, Visualization
pip install seaborn      # Graphing, Visualization (Simpler, Easier)


# Jupyter Lab (Main Code editor for AI)
pip install jupyterlab 
```
<br/>

- **`jupyterlab`**: Main code editor for AI 
  
- You can also use " colab "

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## 3. Importing and using Libraries

<br/>
<br/>

### Keywords
| keyword  | Purpose        |
| -------- | -------------- |
| `from`   | Module path    |
| `import` | What to import |
| `as`     | Shorter-name   |

<br/>
<br/>
<br/>

#### Format:

- `import` __________ `as` _____


<br/>
<br/>

#### Example:

- `import` pandas `as` pd

- `import` numpy `as` np

<br/>
<br/>

#### Example:

<br/>

```py
import numpy

x = numpy.ndarray(  [1,2,3] )
#   ^
```
<br/>


```py
import numpy as np

x = np.ndarray( [1,2,3] )
#   ^
```