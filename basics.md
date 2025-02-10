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


In Python, a set is an unordered collection of unique elements. Sets are similar to lists or dictionaries, but with a key difference: they do not allow duplicate elements. Additionally, sets are mutable, meaning that you can add or remove elements after the set is created. However, the elements within a set must be immutable (e.g., numbers, strings, tuples), and a set cannot contain another set.
Creating a Set

You can create a set using curly braces {} or the set() constructor.
```python
# Using curly braces
my_set = {1, 2, 3}

# Using set() constructor
my_set2 = set([1, 2, 3])
```
Common Set Methods

Here are some commonly used methods and operations on Python sets:
1. Adding Elements

    add(element): Adds a single element to the set.
```python
my_set.add(4)
print(my_set)  # Output: {1, 2, 3, 4}
```
2. Removing Elements
i.remove(element): Removes an element from the set. If the element does not exist, it raises a KeyError.
```python
my_set.remove(4)
print(my_set)  # Output: {1, 2, 3}
```
ii.discard(element): Removes an element from the set, but if the element is not found, it does nothing (no error).
```python
my_set.discard(5)  # Does nothing because 5 is not in the set
```
iii.pop(): Removes and returns an arbitrary element from the set. It raises a KeyError if the set is empty.
```python
popped_element = my_set.pop()
print(popped_element)  # Output: 1 (or any arbitrary element)
```
3. Clearing a Set
    clear(): Removes all elements from the set, leaving it empty.
```python
my_set.clear()
print(my_set)  # Output: set()
```
4. Copying a Set
    copy(): Returns a shallow copy of the set.
```python
new_set = my_set.copy()
```
5. Set Operations
i.Union: Combines two sets.
        union(other_set) or the | operator.
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.union(set2)
print(result)  # Output: {1, 2, 3, 4, 5}
```
ii.Intersection: Returns common elements between sets.
    intersection(other_set) or the & operator.
```python
result = set1.intersection(set2)
print(result)  # Output: {3}
```
iii.Difference: Returns elements in the first set that are not in the second.
    difference(other_set) or the - operator.
```python
result = set1.difference(set2)
print(result)  # Output: {1, 2}
```
iv.Symmetric Difference: Returns elements that are in either set, but not in both.
    symmetric_difference(other_set) or the ^ operator.
```python
result = set1.symmetric_difference(set2)
print(result)  # Output: {1, 2, 4, 5}
```
6. Subset and Superset
issubset(other_set): Returns True if the set is a subset of the other set (i.e., all elements of the set are in the other set).
```python
print({1, 2}.issubset({1, 2, 3}))  # Output: True
```
issuperset(other_set): Returns True if the set is a superset of the other set (i.e., it contains all elements of the other set).
```python
print({1, 2, 3}.issuperset({1, 2}))  # Output: True
```
7. Set Length

    len(set): Returns the number of elements in the set.

print(len(my_set))  # Output: 3 (for set {1, 2, 3})

8. Set Comprehension

    Similar to list comprehensions, you can create sets using set comprehension:

even_numbers = {x for x in range(10) if x % 2 == 0}
print(even_numbers)  # Output: {0, 2, 4, 6, 8}

Important Properties of Sets

    Unordered: Sets do not maintain the order of the elements.
    No Duplicates: A set cannot contain duplicate elements. If you try to add a duplicate element, it will be ignored.

Example of Using Sets

# Create a set
fruits = {"apple", "banana", "cherry"}

# Add an element
fruits.add("orange")

# Remove an element
fruits.remove("banana")

# Check if an element exists
if "apple" in fruits:
    print("Apple is in the set")

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1 | set2  # {1, 2, 3, 4, 5}
intersection_set = set1 & set2  # {3}
difference_set = set1 - set2  # {1, 2}

Sets are commonly used for operations where you want to ensure uniqueness and perform mathematical set operations such as union, intersection, and difference.


##A dictionary in Python is a collection of key-value pairs, where each key is unique and is associated with a value. Dictionaries are unordered, and the keys are immutable types (such as strings, numbers, or tuples), while the values can be of any type, including mutable types like lists.
Creating a Dictionary

You can create a dictionary using curly braces {} with key-value pairs separated by colons : or by using the dict() constructor.

# Using curly braces
my_dict = {"name": "John", "age": 25, "city": "New York"}

# Using dict() constructor
my_dict2 = dict(name="John", age=25, city="New York")

Common Dictionary Methods

Here are some commonly used methods and operations for working with dictionaries in Python:
1. Accessing Values

    You can access a value by referencing its key:

name = my_dict["name"]
print(name)  # Output: John

    If the key does not exist, it raises a KeyError.

    You can use the get() method to access a value, which won't raise an error if the key is missing (instead, it returns None or a default value if provided).

age = my_dict.get("age")
print(age)  # Output: 25

# Using default value
country = my_dict.get("country", "USA")
print(country)  # Output: USA

2. Adding or Updating Key-Value Pairs

    You can add a new key-value pair or update an existing key using the assignment operator.

my_dict["email"] = "john@example.com"  # Add new key-value pair
my_dict["age"] = 26  # Update existing key-value pair

3. Removing Elements

    pop(key): Removes the key-value pair with the specified key and returns its value.

removed_value = my_dict.pop("age")
print(removed_value)  # Output: 26
print(my_dict)  # Output: {'name': 'John', 'city': 'New York', 'email': 'john@example.com'}

    popitem(): Removes and returns an arbitrary key-value pair (useful for working with unordered data).

removed_item = my_dict.popitem()
print(removed_item)  # Output: ('email', 'john@example.com')

    del keyword: Deletes a key-value pair based on the key.

del my_dict["city"]
print(my_dict)  # Output: {'name': 'John'}

    clear(): Removes all key-value pairs from the dictionary.

my_dict.clear()
print(my_dict)  # Output: {}

4. Copying a Dictionary

    copy(): Returns a shallow copy of the dictionary.

new_dict = my_dict.copy()

5. Checking Keys and Values

    keys(): Returns a view object containing all the keys in the dictionary.

keys = my_dict.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'city'])

    values(): Returns a view object containing all the values in the dictionary.

values = my_dict.values()
print(values)  # Output: dict_values(['John', 25, 'New York'])

    items(): Returns a view object containing all key-value pairs as tuples.

items = my_dict.items()
print(items)  # Output: dict_items([('name', 'John'), ('age', 25), ('city', 'New York')])

    in operator: Checks if a key exists in the dictionary.

if "name" in my_dict:
    print("Name exists in the dictionary")

6. Dictionary Length

    len(dictionary): Returns the number of key-value pairs in the dictionary.

print(len(my_dict))  # Output: 3 (if there are 3 key-value pairs)

7. Combining Dictionaries

    update(): Updates the dictionary with key-value pairs from another dictionary or iterable. If a key already exists, its value will be updated.

my_dict.update({"age": 30, "country": "USA"})
print(my_dict)  # Output: {'name': 'John', 'age': 30, 'city': 'New York', 'country': 'USA'}

    You can also combine dictionaries using the ** unpacking operator (available in Python 3.5+).

dict1 = {"a": 1, "b": 2}
dict2 = {"c": 3, "d": 4}
combined = {**dict1, **dict2}
print(combined)  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}

8. Dictionary Comprehension

    Similar to list comprehensions, you can create dictionaries using dictionary comprehension:

squared = {x: x ** 2 for x in range(5)}
print(squared)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

Example of Using Dictionaries

# Creating a dictionary
person = {"name": "John", "age": 25, "city": "New York"}

# Accessing values
print(person["name"])  # Output: John
print(person.get("age"))  # Output: 25

# Updating or adding values
person["email"] = "john@example.com"
person["age"] = 26

# Removing elements
person.pop("city")
del person["email"]

# Iterating through keys and values
for key, value in person.items():
    print(f"{key}: {value}")

# Combining dictionaries
dict1 = {"a": 1, "b": 2}
dict2 = {"b": 3, "c": 4}
dict1.update(dict2)
print(dict1)  # Output: {'a': 1, 'b': 3, 'c': 4}

Important Properties of Dictionaries

    Unordered: Dictionaries in Python are unordered collections. The order of keys is not guaranteed (though in Python 3.7+ dictionaries preserve insertion order).
    Unique Keys: A dictionary cannot have duplicate keys. If you try to assign a value to an existing key, it will overwrite the previous value.
    Mutable: Dictionaries are mutable, meaning you can change, add, or remove key-value pairs after creation.

Dictionaries are widely used for fast lookups, counting occurrences of elements, grouping data, and representing JSON-like structures.


for <condition>:
    #instructions
else:
    #instructions

while <condition>:
    #instructions
