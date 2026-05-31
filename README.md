# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
Add code here
```py
import numpy as np
array=np.array(eval(input()))
print("og array\n",array)
print("sorted array\n",np.sort(array,axis=0))
```

## Output
<img width="470" height="318" alt="image" src="https://github.com/user-attachments/assets/a0c9c755-1721-442e-a252-014984a1979d" />

## Result
Successfully wrote a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program

Add code here
```py
import numpy as np
l1=eval(input())
l2=eval(input())
x=np.array(l1)
y=np.array(l2)
print(np.where(x>y))
print(np.where(x == y))
```

## Output
<img width="1133" height="241" alt="image" src="https://github.com/user-attachments/assets/3f57429b-67e7-4980-8fb0-9e81aa96242f" />

## Result
Successfully wrote a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.


# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program

Add code here
```py
import numpy as np
original_array = np.array([[1, 2, 3],
                           [4, 5, 6],
                           [7, 8, 9]])
new_column = np.array([10, 11, 12])
array_without_column = np.delete(original_array, 1, axis=1)
updated_array = np.insert(array_without_column, 1, new_column, axis=1)
print("Updated array:")
print(updated_array)
```

## Output
<img width="673" height="310" alt="image" src="https://github.com/user-attachments/assets/85557c71-d4a1-4f80-9b44-81dc920644d1" />

## Result
Successfully wrote a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.


# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program
Add code here
```py
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily'],
    'score': [12.5, 9.0, 16.5, np.nan, 9.0],
    'attempts': [1, 3, 2, 3, 2],
    'qualify': ['yes', 'no', 'yes', 'no', 'no']
}

labels = ['a', 'b', 'c', 'd', 'e']

df = pd.DataFrame(exam_data, index=labels)

print(df)
```

## Output
<img width="675" height="492" alt="image" src="https://github.com/user-attachments/assets/365cb9f2-e56e-4010-a29f-77fd0b626178" />

## Result
Successfully wrote a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.


# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program

Add code here
```py
import pandas as pd

student_data1 = {
    'name': ['Alice', 'Bob', 'Charlie'],
    'score': [85, 90, 95],
    'grade': ['B', 'A', 'A']
}
df1 = pd.DataFrame(student_data1)

student_data2 = {
    'name': ['David', 'Eva'],
    'score': [88, 92],
    'grade': ['B+', 'A']
}
df2 = pd.DataFrame(student_data2)

combined_df = pd.concat([df1, df2], axis=0)

print(combined_df)
```

## Output
<img width="402" height="583" alt="image" src="https://github.com/user-attachments/assets/8eb26a11-14f2-493e-a848-45f9e9a18bbf" />

## Result
Successfully wrote a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.
