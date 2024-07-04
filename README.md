# 0x00. Python - Variable Annotations

### Variable (Type) Annotations

This project  summarized as the following
## Tasks To Complete

### 0. Basic annotations - add

| File       | Description |
|------------|--------------|
| [0-add.py](0-add.py) | Contains a type-annotated function `add` that takes a float `a` and a float `b` as arguments and returns their sum as a float. |

### 1. Basic annotations - concat

| File         | Description |
|--------------|--------------|
| [1-concat.py](1-concat.py) | Contains a type-annotated function `concat` that takes a string `str1` and a string `str2` as arguments and returns a concatenated string. |

### 2. Basic annotations - floor

| File        | Description |
|-------------|--------------|
| [2-floor.py](2-floor.py) | Contains a type-annotated function `floor` which takes a float `n` as argument and returns the floor of the float. |

### 3. Basic annotations - to string

| File         | Description |
|--------------|--------------|
| [3-to_str.py](3-to_str.py) | Contains a type-annotated function `to_str` that takes a float `n` as argument and returns the string representation of the float. |

### 4. Define variables

| File                      | Description |
|---------------------------|--------------|
| [4-define_variables.py](4-define_variables.py) | Contains a script that defines and annotates the following variables with the specified values:<br>- `a`, an integer with a value of 1.<br>- `pi`, a float with a value of 3.14.<br>- `i_understand_annotations`, a boolean with a value of True.<br>- `school`, a string with a value of "Holberton". |

### 5. Complex types - list of floats

| File          | Description |
|---------------|--------------|
| [5-sum_list.py](5-sum_list.py) | Contains a type-annotated function `sum_list` which takes a list `input_list` of floats as argument and returns their sum as a float. |

### 6. Complex types - mixed list

| File               | Description |
|--------------------|--------------|
| [6-sum_mixed_list.py](6-sum_mixed_list.py) | Contains a type-annotated function `sum_mixed_list` which takes a list `mxd_lst` of integers and floats and returns their sum as a float. |

### 7. Complex types - string and int/float to tuple

| File       | Description |
|------------|--------------|
| [7-to_kv.py](7-to_kv.py) | Contains a type-annotated function `to_kv` that takes a string `k` and an int OR float `v` as arguments and returns a tuple. The first element of the tuple is the string `k`. The second element is the square of the int/float `v` and should be annotated as a float. |

### 8. Complex types - functions

| File              | Description |
|-------------------|--------------|
| [8-make_multiplier.py](8-make_multiplier.py) | Contains a type-annotated function `make_multiplier` that takes a float `multiplier` as argument and returns a function that multiplies a float by `multiplier`. |

### 9. Let's duck type an iterable object

| File               | Description |
|--------------------|--------------|
| [9-element_length.py](9-element_length.py) | Contains an annotation of the function's parameters and return values with the appropriate types.<br><br>```python<br>def element_length(lst):<br>    return [(i, len(i)) for i in lst]<br>``` |

### 10. Duck typing - first element of a sequence

| File                         | Description |
|------------------------------|--------------|
| [100-safe_first_element.py](100-safe_first_element.py) | Contains an augmentation of the following code with the correct duck-typed annotations:<br><br>```python<br># The types of the elements of the input are not known<br>def safe_first_element(lst):<br>    if lst:<br>        return lst[0]<br>    else:<br>        return None<br>``` |

### 11. More involved type annotations

| File                      | Description |
|---------------------------|--------------|
| [101-safely_get_value.py](101-safely_get_value.py) | Contains a script that includes the code below with type annotations added to it:<br><br>```python<br>def safely_get_value(dct, key, default = None):<br>    if key in dct:<br>        return dct[key]<br>    else:<br>        return default<br>``` |

### 12. Type Checking

| File                     | Description |
|--------------------------|--------------|
| [102-type_checking.py](102-type_checking.py) | Contains the code below and uses `mypy` to validate it and apply any necessary changes:<br><br>```python<br>def zoom_array(lst: Tuple, factor: int = 2) -> Tuple:<br>    zoomed_in: Tuple = [<br>        item for item in lst<br>        for i in range(factor)<br>    ]<br>    return zoomed_in<br><br>array = [12, 72, 91]<br><br>zoom_2x = zoom_array(array)<br><br>zoom_3x = zoom_array(array, 3.0)<br>``` |

# Details For Tables
1. **Basic annotations - add**
   - **Description**: Contains a type-annotated function `add` that takes a float `a` and a float `b` as arguments and returns their sum as a float.

2. **Basic annotations - concat**
   - **Description**: Contains a type-annotated function `concat` that takes a string `str1` and a string `str2` as arguments and returns a concatenated string.

3. **Basic annotations - floor**
   - **Description**: Contains a type-annotated function `floor` which takes a float `n` as argument and returns the floor of the float.

4. **Basic annotations - to string**
   - **Description**: Contains a type-annotated function `to_str` that takes a float `n` as argument and returns the string representation of the float.

5. **Define variables**
   - **Description**: Contains a script that defines and annotates the following variables with the specified values: `a` (integer, value: 1), `pi` (float, value: 3.14), `i_understand_annotations` (boolean, value: True), and `school` (string, value: “Holberton”).

6. **Complex types - list of floats**
   - **Description**: Contains a type-annotated function `sum_list` which takes a list `input_list` of floats as argument and returns their sum as a float.

7. **Complex types - mixed list**
   - **Description**: Contains a type-annotated function `sum_mixed_list` which takes a list `mxd_lst` of integers and floats and returns their sum as a float.

8. **Complex types - string and int/float to tuple**
   - **Description**: Contains a type-annotated function `to_kv` that takes a string `k` and an int or float `v` as arguments and returns a tuple. The first element of the tuple is the string `k`, and the second element is the square of the int/float `v`, annotated as a float.

9. **Complex types - functions**
   - **Description**: Contains a type-annotated function `make_multiplier` that takes a float `multiplier` as argument and returns a function that multiplies a float by `multiplier`.

10. **Let's duck type an iterable object**
    - **Description**: Contains an annotation of the function `element_length`'s parameters and return values with the appropriate types.

11. **Duck typing - first element of a sequence**
    - **Description**: Contains an augmentation of the function `safe_first_element` with the correct duck-typed annotations.

12. **More involved type annotations**
    - **Description**: Contains a script that includes the function `safely_get_value` with type annotations added to it.

13. **Type Checking**
    - **Description**: Contains the function `zoom_array` and uses `mypy` to validate it and apply any necessary changes.
