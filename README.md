# Ai-Datascience

A comprehensive collection of Jupyter Notebooks focused on AI and Data Science topics.

## Repository Overview

This repository contains educational materials and practical examples for learning AI and Data Science concepts using Python.

## 📊 Language Composition

- **Jupyter Notebook**: 100%

## 📁 Repository Contents

### Notebooks

1. **Untitled1.ipynb** ⭐ _For First-Time Learners_
   - **Purpose**: Learn Python fundamentals through practical examples
   - **Topics Covered**:
     - Functions: How to define and call reusable code blocks
     - Mathematical Operations: Addition, area calculations (rectangle and circle)
     - Conditional Logic: If-else statements for decision-making
     - List Operations: Finding maximum values
     - Number Classification: Even/odd checker and positive/negative classifier
   - **Best For**: Complete beginners to Python programming
   - **Functions Included**:
     - `add_number()` - Sum three numbers
     - `area_rect()` - Calculate rectangle area
     - `area_circle()` - Calculate circle area
     - `find_max()` - Find largest number in a list
     - `find_even_odd()` - Classify numbers as even or odd
     - `find_positive()` - Classify numbers as positive, negative, or zero

2. **numpy.ipynb** 📊 _Intermediate Level_
   - **Purpose**: Master NumPy library for numerical computing and data manipulation
   - **Best For**: Those who understand Python basics and want to work with arrays and data
   - **Topics Covered**:
     - NumPy array creation and operations
     - Array manipulation and reshaping
     - Mathematical operations on arrays
     - Statistical functions (sum, mean, etc.)
     - Integration with Pandas for data handling
     - Working with CSV files

---

## 🚀 Getting Started

To work with the notebooks in this repository:

1. Clone the repository
   ```bash
   git clone https://github.com/rajeshdchikkala/Ai-Datascience.git
   ```

2. Install required dependencies
   ```bash
   pip install numpy pandas jupyter
   ```

3. Open the notebooks using Jupyter Notebook or Google Colab
   ```bash
   jupyter notebook
   ```
   
   Or use Google Colab: https://colab.research.google.com/

4. Follow along with the tutorials and examples

---

## 📚 NumPy (numpy.ipynb) - Complete Guide for Beginners

### What is NumPy?
NumPy is a Python library for numerical computing. It provides powerful tools for working with large arrays and matrices of numerical data.

### 1️⃣ Importing NumPy
```python
import numpy as np
```
**What it does**: Imports the NumPy library and gives it a short name `np` for easy use.

---

### 2️⃣ Creating Arrays

#### Creating a Simple 1D Array
```python
sales = np.array([1000, 2000, 3000, 4000])
print(sales)
# Output: [1000 2000 3000 4000]
```
**What it does**: Creates an array (list of numbers) called `sales`.
**Use Case**: Storing a sequence of sales values

#### Checking Data Type
```python
sales.dtype
# Output: dtype('int64')
```
**What it does**: Shows the data type of array elements. `int64` means 64-bit integers.

#### Arrays with Decimal Numbers
```python
sales = np.array([1000.89, 2000, 3000, 4000])
print(sales)
# Output: [1000.89 2000.   3000.   4000.  ]
```
**What it does**: When you include a decimal number, all numbers become floats (decimals).

---

### 3️⃣ Mathematical Operations on Arrays

#### Subtract from All Elements
```python
sales - 500
# Output: array([ 500.89, 1500.  , 2500.  , 3500.  ])
```
**What it does**: Subtracts 500 from each element in the array.
**Use Case**: Apply discount to all sales figures

#### Multiply All Elements
```python
sales * 2
# Output: array([2001.78, 4000.  , 6000.  , 8000.  ])
```
**What it does**: Multiplies each element by 2.
**Use Case**: Calculate double the sales, or convert currencies

---

### 4️⃣ Creating Arrays with Special Functions

#### Create Array of Zeros
```python
arr_zeroes = np.zeros((2, 3))
print(arr_zeroes)
# Output:
# [[0. 0. 0.]
#  [0. 0. 0.]]
```
**What it does**: Creates a 2×3 array filled with zeros.
**Use Case**: Initialize an empty array before filling with data

#### Create Array of Ones
```python
arr_ones = np.ones((2, 3))
print(arr_ones)
# Output:
# [[1. 1. 1.]
#  [1. 1. 1.]]
```
**What it does**: Creates a 2×3 array filled with ones.
**Use Case**: Create a default array to multiply with other values

---

### 5️⃣ Creating Number Ranges

#### Using arange() - Create a Range with Step
```python
arr_arange = np.arange(0, 10, 2)
print(arr_arange)
# Output: [0 2 4 6 8]
```
**What it does**: Creates numbers from 0 to 10 (not including 10) with step of 2.
- **Start**: 0
- **End**: 10 (not included)
- **Step**: 2

#### Counting Down
```python
arr_arange = np.arange(10, 0, -1)
print(arr_arange)
# Output: [10  9  8  7  6  5  4  3  2  1]
```
**What it does**: Creates numbers from 10 down to 1 with step of -1 (going backwards).

#### Different Steps
```python
arr_arange = np.arange(0, 15, 3)
print(arr_arange)
# Output: [ 0  3  6  9 12]
```
**What it does**: Creates numbers from 0 to 15 with step of 3.

#### Simple Range
```python
arr_arange = np.arange(0, 15)
print(arr_arange)
# Output: [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14]
```
**What it does**: Creates numbers from 0 to 14 (default step of 1).

---

### 6️⃣ Using linspace() - Evenly Spaced Values

`linspace` divides a range into equal parts.

```python
arr_linspace = np.linspace(0, 10, num=5)
print(arr_linspace)
# Output: [ 0.   2.5  5.   7.5 10. ]
```
**What it does**: Creates 5 evenly spaced values from 0 to 10.
- Divides the range into equal intervals

#### With 2 Points
```python
arr_linspace = np.linspace(0, 10, num=2)
print(arr_linspace)
# Output: [ 0. 10.]
```
**What it does**: Creates only start and end points.

#### With 3 Points
```python
arr_linspace = np.linspace(0, 10, num=3)
print(arr_linspace)
# Output: [ 0.  5. 10.]
```
**What it does**: Divides range into 2 equal parts (3 points).

#### With 4 Points
```python
arr_linspace = np.linspace(0, 10, num=4)
print(arr_linspace)
# Output: [ 0.  3.33333333  6.66666667 10. ]
```
**What it does**: Divides range into 3 equal parts (4 points).

**Use Case**: Generate evenly spaced time points or frequency values

---

### 7️⃣ Reshaping Arrays

#### Convert 1D to 2D Array
```python
arra_1d = np.array([1, 2, 3, 4, 5, 6])
arra_2d = np.reshape(arra_1d, (2, 3))
print(arra_2d)
# Output:
# [[1 2 3]
#  [4 5 6]]
```
**What it does**: Reorganizes 6 elements into a 2×3 (2 rows, 3 columns) array.

#### Another Example
```python
arra_1d = np.array([1, 2, 3, 4, 5, 6, 7, 8])
arra_2d = np.reshape(arra_1d, (2, 4))
print(arra_2d)
# Output:
# [[1 2 3 4]
#  [5 6 7 8]]
```
**What it does**: Reorganizes 8 elements into a 2×4 (2 rows, 4 columns) array.

**Use Case**: Organize data into rows and columns for better analysis

---

### 8️⃣ Advanced Array Creation

#### linspace with endpoint=False
```python
arr_linspace = np.linspace(0, 10, num=4, endpoint=False, dtype='int')
print(arr_linspace)
# Output: [0 2 5 7]
```
**What it does**: Creates 4 evenly spaced values from 0 (not including 10), converted to integers.

---

### 9️⃣ Adding Arrays

#### Element-wise Addition
```python
arra_1d = np.array([1, 2, 3])
arra_2d = np.array([1, 2, 3])
arr_sum = np.add(arra_1d, arra_2d)
print(arr_sum)
# Output: [2 4 6]
```
**What it does**: Adds corresponding elements from two arrays.
- Position 0: 1 + 1 = 2
- Position 1: 2 + 2 = 4
- Position 2: 3 + 3 = 6

**Use Case**: Combine sales from different stores, or add measurements

---

### 🔟 Sum - Add All Elements

#### Sum of All Elements in 2D Array
```python
arra_1d = np.array([[1, 2, 3], [4, 5, 6]])
s = np.sum(arra_1d)
print(s)
# Output: 21
```
**What it does**: Adds all elements: 1+2+3+4+5+6 = 21
**Use Case**: Total sales, total expenses, total count

#### Sum of 1D Array
```python
arra_1d = np.array([1, 2, 3])
s = np.sum(arra_1d)
print(s)
# Output: 6
```
**What it does**: Adds all elements: 1+2+3 = 6

---

### 1️⃣1️⃣ Mean - Average of All Elements

#### Mean of 2D Array
```python
arra_1d = np.array([[1, 2, 3], [4, 5, 6]])
s = np.mean(arra_1d)
print(s)
# Output: 3.5
```
**What it does**: Calculates average of all elements.
- Sum = 21, Count = 6
- Average = 21 / 6 = 3.5

**Use Case**: Average score, average temperature, average salary

#### Mean of 1D Array
```python
arra_1d = np.array([1, 2, 3])
s = np.mean(arra_1d)
print(s)
# Output: 2.0
```
**What it does**: Calculates average: (1+2+3)/3 = 2.0

---

### 1️⃣2️⃣ Working with Pandas & CSV Files

#### Import Libraries
```python
import pandas as pd
import numpy as np
import csv
```
**What it does**: Imports necessary libraries for data handling.

#### Create DataFrame
```python
wd = {
    'day': ['1/1/2017', '1/2/2017', '1/3/2017', '1/4/2017'],
    'temperature': [32, 35, 28, 24],
    'windspeed': [6, 7, 2, 7],
    'event': ['Rain', 'Sunny', 'Snow', 'Rain']
}
df = pd.DataFrame(wd)
df
```
**What it does**: Creates a table (DataFrame) with weather data.

| day | temperature | windspeed | event |
|-----|-------------|-----------|-------|
| 1/1/2017 | 32 | 6 | Rain |
| 1/2/2017 | 35 | 7 | Sunny |
| 1/3/2017 | 28 | 2 | Snow |
| 1/4/2017 | 24 | 7 | Rain |

#### Save to CSV File
```python
df.to_csv("weather.csv", index=False)
```
**What it does**: Saves the DataFrame to a CSV file.
- `index=False`: Don't include row numbers in the file

#### Read from CSV File
```python
data = pd.read_csv("weather.csv")
data
```
**What it does**: Reads the CSV file back into a DataFrame.

**Use Case**: Save and load data from files for analysis

---

## 🔑 Key Concepts Summary

| Concept | What It Does | Example |
|---------|-------------|---------|
| **Array** | Collection of numbers | `[1, 2, 3, 4, 5]` |
| **2D Array** | Grid of numbers (rows × columns) | `[[1, 2], [3, 4]]` |
| **arange()** | Create range with specific step | `np.arange(0, 10, 2)` |
| **linspace()** | Divide range into equal parts | `np.linspace(0, 10, 5)` |
| **reshape()** | Change array shape | `np.reshape(arr, (2, 3))` |
| **sum()** | Add all elements | `np.sum([1, 2, 3])` = 6 |
| **mean()** | Calculate average | `np.mean([1, 2, 3])` = 2.0 |
| **add()** | Add two arrays element-wise | `np.add([1, 2], [3, 4])` |
| **DataFrame** | Table for data organization | Pandas table with rows/columns |

---

## 💡 Tips for Learning

1. **Run Each Cell**: Execute code to see results
2. **Modify Values**: Change inputs to understand how output changes
3. **Experiment**: Create your own arrays and test functions
4. **Practice**: Solve similar problems independently
5. **Don't Fear Errors**: Error messages help you learn

---

## 🎯 Learning Path

1. **Start with Untitled1.ipynb** - Learn Python basics
2. **Move to numpy.ipynb** - Master numerical computing
3. **Combine Both** - Create real-world data analysis projects
4. **Next Steps**: Learn Pandas, Matplotlib, and Scikit-learn

---

## 📝 License

[Add your license information here]

## 👤 Author

rajeshdchikkala

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the content.

---

**Happy Learning! 🎓** Start with Untitled1.ipynb and progress to numpy.ipynb!
