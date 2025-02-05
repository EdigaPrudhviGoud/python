# Lists in Python

In Python, a **list** is a built-in data structure that allows storing multiple items in a single variable. Lists are **ordered, mutable, and allow duplicate elements**.

```python
my_list = [1, 2, 3, 4, 5]
```

## Common List Methods

| Method | Description | Example |
|--------|-------------|---------|
| `append(x)` | Adds an item `x` to the end of the list. | `my_list.append(6)` |
| `extend(iterable)` | Extends the list by adding elements from an iterable (e.g., another list). | `my_list.extend([7, 8])` |
| `insert(index, x)` | Inserts an item `x` at a specific index. | `my_list.insert(2, 10)` |
| `remove(x)` | Removes the first occurrence of `x`. | `my_list.remove(3)` |
| `pop([index])` | Removes and returns the item at the given index (last by default). | `my_list.pop(2)` |
| `clear()` | Removes all elements from the list. | `my_list.clear()` |
| `index(x, [start, end])` | Returns the index of the first occurrence of `x`. | `my_list.index(4)` |
| `count(x)` | Returns the count of occurrences of `x`. | `my_list.count(2)` |
| `sort([key, reverse])` | Sorts the list in ascending order (default). Use `reverse=True` for descending order. | `my_list.sort(reverse=True)` |
| `reverse()` | Reverses the elements of the list. | `my_list.reverse()` |
| `copy()` | Returns a shallow copy of the list. | `new_list = my_list.copy()` |

## Examples

```python
numbers = [3, 1, 4, 1, 5, 9]

numbers.append(2)   # [3, 1, 4, 1, 5, 9, 2]
numbers.remove(1)   # [3, 4, 1, 5, 9, 2]
numbers.sort()      # [1, 2, 3, 4, 5, 9]
numbers.reverse()   # [9, 5, 4, 3, 2, 1]
```
A tuple in Python is an immutable sequence of values. Once a tuple is created, its values cannot be modified. You can create a tuple by placing values inside parentheses () and separating them with commas.
```python
# Defining a tuple
my_tuple = (1, 2, 3, "apple", "banana")

# Accessing elements of the tuple
print(my_tuple[0])  # Output: 1
print(my_tuple[3])  # Output: "apple"

# Tuple slicing
print(my_tuple[1:4])  # Output: (2, 3, 'apple')

# Nested tuple
nested_tuple = (1, 2, (3, 4))
print(nested_tuple[2])  # Output: (3, 4)
```
Tuple Operations:

1.Concatenation: You can concatenate two tuples using the + operator.
```python
tuple1 = (1, 2)
tuple2 = (3, 4)
result = tuple1 + tuple2
print(result)  # Output: (1, 2, 3, 4)
```
2.Repetition: You can repeat a tuple using the * operator.
```python
my_tuple = (1, 2)
result = my_tuple * 3
print(result)  # Output: (1, 2, 1, 2, 1, 2)
```
3.Membership Test: You can check if an element exists in a tuple using the in keyword.
```python
my_tuple = (1, 2, 3)
print(2 in my_tuple)  # Output: True
print(4 in my_tuple)  # Output: False
```
4.Length: You can get the length of a tuple using len().
```python
my_tuple = (1, 2, 3)
print(len(my_tuple))  # Output: 3
```
Important Points:

    Immutability: Once a tuple is created, its elements cannot be changed, unlike lists.
    Indexing: Tuples are indexed just like lists, starting from 0.
    Allowing Multiple Data Types: Tuples can store values of different data types, including integers, strings, lists, etc.
