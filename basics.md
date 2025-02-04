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
