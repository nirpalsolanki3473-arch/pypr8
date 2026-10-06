# 🔢 NumPy Analyzer

A beginner-friendly **NumPy Analyzer** built with Python and Object-Oriented Programming (OOP).

This project provides a menu-driven interface for creating and analyzing NumPy arrays. It demonstrates practical NumPy operations including array creation, indexing, slicing, mathematical operations, combining and splitting arrays, searching, sorting, filtering, and statistical calculations.

---

## 📌 Project Overview

The **NumPy Analyzer** is a command-line application developed using the NumPy library and OOP principles.

The project organizes NumPy functionality inside a `DataAnalytics` class and allows users to interact with arrays through a simple menu.

The application supports:

* 1D, 2D, and 3D array creation
* Array indexing
* Array slicing
* Addition
* Subtraction
* Multiplication
* Division
* Dot product
* Matrix multiplication
* Combining arrays
* Splitting arrays
* Searching values
* Sorting arrays
* Filtering arrays
* Statistical calculations
* Percentile calculation
* Correlation calculation

---

# 🎯 Objectives

The main objectives of this project are:

* Practice NumPy fundamentals.
* Understand multidimensional arrays.
* Apply NumPy mathematical operations.
* Work with array indexing and slicing.
* Understand array shape and dimensions.
* Practice searching, sorting, and filtering.
* Perform statistical calculations.
* Understand NumPy array manipulation.
* Apply Object-Oriented Programming concepts.
* Build a practical menu-driven Python application.

---

# 🛠️ Technologies Used

### Programming Language

* Python

### Library

* NumPy

### Concepts

* Object-Oriented Programming
* Classes and Objects
* Constructor
* Private Methods
* Static Methods
* Class Methods
* Exception Handling
* User Input
* Conditional Statements
* Loops

---

# 📦 Installation

Install NumPy using:

```bash
pip install numpy
```

Check the installed NumPy version:

```python
import numpy as np

print(np.__version__)
```

---

# 🏗️ Class Structure

The main class in the project is:

```python
class DataAnalytics:
```

The class stores the NumPy array in:

```python
self.array
```

The constructor accepts an optional array and converts it into a NumPy array when provided.

---

# 🧩 OOP Concepts Used

## 1. Constructor

The project uses:

```python
def __init__(self, array=None):
```

The constructor initializes the array when an array is provided.

```python
self.array = np.array(array) if array is not None else None
```

---

## 2. Private Method

The project contains a private validation method:

```python
def __validate_array(self):
```

It checks whether an array has been created before performing operations.

If no array exists, it displays:

```text
No array has been created.
```

This demonstrates the use of a **private method** in Python.

---

## 3. Static Method

The project uses:

```python
@staticmethod
def display_title():
```

This method displays the title of the application.

A static method does not require an object instance to be called.

---

## 4. Class Method

The project also demonstrates a class method:

```python
@classmethod
def from_list(cls, values):
```

It creates a `DataAnalytics` object from a list of values.

---

# 📋 Main Menu

When the program starts, the user gets the following menu:

```text
====================================
       Welcome to NumPy Analyzer
====================================

Choose an option:
1. Create a NumPy Array
2. Perform Mathematical Operations
3. Combine or Split Arrays
4. Search, Sort, or Filter Arrays
5. Compute Aggregates and Statistics
6. Exit
```

The menu is controlled using a `while` loop and conditional statements.

---

# 1️⃣ Array Creation

The application supports three types of arrays:

```text
1. 1D Array
2. 2D Array
3. 3D Array
```

## 1D Array

The user enters elements separated by spaces.

Example:

```text
10 20 30 40 50
```

The values are converted into a NumPy array.

---

## 2D Array

The user provides:

* Number of rows
* Number of columns
* Array elements

The project uses `reshape()` to create the requested 2D structure.

Example:

```text
1 2 3
4 5 6
```

---

## 3D Array

The user provides:

* Number of layers
* Number of rows
* Number of columns
* Array elements

The values are reshaped into a 3D NumPy array.

---

# 2️⃣ Indexing and Slicing

After creating an array, the project provides:

```text
1. Indexing
2. Slicing
3. Go Back
```

---

## Indexing

Indexing allows the user to access individual elements.

### 1D

```python
array[index]
```

### 2D

```python
array[row, column]
```

### 3D

```python
array[layer, row, column]
```

The program also handles invalid indexes using exception handling.

---

## Slicing

The project supports slicing for:

* 1D arrays
* 2D arrays
* 3D arrays

For example, a 2D array can be sliced using:

```python
array[row_start:row_end, column_start:column_end]
```

The 3D implementation accepts layer, row, and column ranges.

---

# 3️⃣ Mathematical Operations

The mathematical operations menu contains:

```text
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Dot Product
6. Matrix Multiplication
```

---

## Addition

Two arrays with the same shape can be added:

```python
array1 + array2
```

---

## Subtraction

The project performs element-wise subtraction:

```python
array1 - array2
```

---

## Multiplication

Element-wise multiplication is performed using:

```python
array1 * array2
```

---

## Division

Element-wise division is performed using:

```python
array1 / array2
```

The project checks for zero values in the second array before division.

---

## Dot Product

The project uses:

```python
np.dot()
```

to calculate the dot product between arrays.

The arrays are flattened before calculating the dot product.

---

## Matrix Multiplication

Matrix multiplication is performed using:

```python
np.matmul()
```

The project checks whether the number of columns in the first matrix matches the number of rows in the second matrix before multiplication.

---

# 4️⃣ Combine and Split Arrays

The project provides two operations:

```text
1. Combine Arrays
2. Split Array
```

---

## Combine Arrays

For 2D arrays, the project supports:

### Vertical Stack

```python
np.vstack()
```

### Horizontal Stack

```python
np.hstack()
```

### Concatenate

```python
np.concatenate()
```

These operations combine the original array with a second array.

---

## Split Array

The project uses:

```python
np.array_split()
```

to divide an array into a user-specified number of sections.

---

# 5️⃣ Search, Sort, and Filter

The project provides:

```text
1. Search a value
2. Sort the array
3. Filter values
```

---

## Search

The project uses:

```python
np.where()
```

to find the positions where a specified value occurs.

If the value does not exist, the program displays:

```text
Value not found.
```

---

## Sort

The user can sort the array in:

* Ascending order
* Descending order

The project uses:

```python
np.sort()
```

and reverses the result for descending order.

---

## Filter

The project supports the following filtering conditions:

```text
Greater than
Less than
Greater than or equal
Less than or equal
Equal to
```

Boolean conditions are used to return values that satisfy the selected condition.

---

# 6️⃣ Statistics and Aggregation

The statistics menu provides:

```text
1. Sum
2. Mean
3. Median
4. Standard Deviation
5. Variance
6. Minimum
7. Maximum
8. Percentile
9. Correlation
```

---

## Sum

```python
np.sum()
```

Calculates the total of the array values.

---

## Mean

```python
np.mean()
```

Calculates the average.

---

## Median

```python
np.median()
```

Calculates the middle value.

---

## Standard Deviation

```python
np.std()
```

Measures the spread of values around the mean.

---

## Variance

```python
np.var()
```

Calculates the variance of the values.

---

## Minimum and Maximum

The project uses:

```python
np.min()
np.max()
```

to find the smallest and largest values.

---

## Percentile

The user enters a percentile between `0` and `100`.

The project uses:

```python
np.percentile()
```

to calculate the requested percentile.

---

## Correlation

The project accepts a second array and calculates the correlation using:

```python
np.corrcoef()
```

The arrays must contain the same number of elements.

The program displays the correlation coefficient between the two arrays.

---

# 🔄 Program Flow

```text
Start
  ↓
Display NumPy Analyzer Title
  ↓
Create DataAnalytics Object
  ↓
Main Menu
  │
  ├── Create NumPy Array
  │      ├── 1D
  │      ├── 2D
  │      └── 3D
  │
  ├── Mathematical Operations
  │      ├── Addition
  │      ├── Subtraction
  │      ├── Multiplication
  │      ├── Division
  │      ├── Dot Product
  │      └── Matrix Multiplication
  │
  ├── Combine / Split
  │      ├── Vertical Stack
  │      ├── Horizontal Stack
  │      ├── Concatenate
  │      └── Split
  │
  ├── Search / Sort / Filter
  │      ├── Search
  │      ├── Sort
  │      └── Filter
  │
  ├── Statistics
  │      ├── Sum
  │      ├── Mean
  │      ├── Median
  │      ├── Standard Deviation
  │      ├── Variance
  │      ├── Minimum
  │      ├── Maximum
  │      ├── Percentile
  │      └── Correlation
  │
  └── Exit
```

---

# 🧠 Python and NumPy Concepts Demonstrated

This project demonstrates practical use of:

### Python

* Classes
* Objects
* Constructor
* Private methods
* Static methods
* Class methods
* `while` loops
* `if / elif / else`
* `try / except`
* User input
* Type conversion

### NumPy

* `np.array()`
* `reshape()`
* `flatten()`
* `np.dot()`
* `np.matmul()`
* `np.vstack()`
* `np.hstack()`
* `np.concatenate()`
* `np.array_split()`
* `np.where()`
* `np.sort()`
* `np.sum()`
* `np.mean()`
* `np.median()`
* `np.std()`
* `np.var()`
* `np.min()`
* `np.max()`
* `np.percentile()`
* `np.corrcoef()`

---

# 📁 Project Structure

A simple project structure can be:

```text
numpy-analyzer/
│
├── numpy_analyzer.py
└── README.md
```

If the program is saved as a Jupyter Notebook, it can instead be:

```text
numpy-analyzer/
│
├── NumPy_Analyzer.ipynb
└── README.md
```

---

# ▶️ How to Run

## Step 1 — Install NumPy

Open the terminal and run:

```bash
pip install numpy
```

## Step 2 — Open the Python file

Open the project in VS Code, Jupyter Notebook, or another Python-supported editor.

## Step 3 — Run the program

If the file is named `numpy_analyzer.py`:

```bash
python numpy_analyzer.py
```

The NumPy Analyzer menu will appear in the terminal.

---

# 💻 Example

```text
====================================
       Welcome to NumPy Analyzer
====================================

Choose an option:
1. Create a NumPy Array
2. Perform Mathematical Operations
3. Combine or Split Arrays
4. Search, Sort, or Filter Arrays
5. Compute Aggregates and Statistics
6. Exit

Enter your choice:
```

---

# 📚 Learning Outcomes

After completing this project, the following skills are practiced:

* Creating NumPy arrays
* Working with 1D, 2D, and 3D arrays
* Understanding array dimensions and shapes
* Indexing and slicing
* Mathematical operations
* Matrix operations
* Array combining and splitting
* Searching and filtering
* Sorting
* Statistical analysis
* Correlation
* Object-Oriented Programming
* Exception handling
* Menu-driven application development

---

# 🚀 Possible Future Improvements

The current project can be extended with:

* File-based array loading
* CSV data support
* Array saving and exporting
* More NumPy functions
* Broadcasting operations
* Reshape and transpose options
* Random array generation
* Graphical user interface
* Better input validation
* More advanced statistical operations

These are **future improvements** and are not part of the current implementation.

---

# 👨‍💻 Author

**NIRPALSINH SOLANKI**

GitHub: [@nirpalsolanki3473-arch](https://github.com/nirpalsolanki3473-arch)

---

# ⭐ Project Summary

The **NumPy Analyzer** is a command-line NumPy project that combines important NumPy operations with Object-Oriented Programming.

It provides an interactive way to create arrays, perform mathematical operations, manipulate arrays, search and filter values, and calculate statistical information.

The project is designed as a practical learning project for building a strong foundation in **Python, NumPy, and OOP**.
