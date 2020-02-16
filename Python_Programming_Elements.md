# Python-specific Language Construct

## Lists:
* Python lists can be used to implement array, stack, queue right off-the-shelf. 
* You can iterate both front and backwards of a list easily, even with an optional hop. It never reaches the stop, so you can think of range as [start,stop) with hop. If start > stop, returns empty list.
* Slice a list easily with the colon (:) operator. It creates a new copy of the slice, so be careful about the space complexity.
* Use list comprehension, but not complicated ones.
* Strings are technically list-style, but they are immutable. So iterating and slicing works but not append/pop etc.

## Dictionary:
* The Python dictionary data structure is as universally useful as it gets. It works out-of-box as an excellent hashmap.
* Use defaultdict from collections for saving some interview time initializing values for new keys.
* To create a hashmap of elements of a string or list (some other iterables will work too), use Counter from collections. These are simple techniques to save a few error-prone lines when time is essential. Caution: be careful about traversing a Counter, some functions from usual dict may not work.

## Other basic data structures:
* Linked lists and Binary trees are the most common data structures you would need in an interview. It is straightforward to implement them in Python.
* While loops are useful to loop through a linked list or traverse a tree (e.g. while node.next is not None).
* A graph is most often represented as an adjacency list in terms of Python dictionaries. For undirected graphs, same edge will be counted twice.
* Breadth-first and depth-first search are absolutely simple in Python using a queue and a stack respectively. Check out an excellent roundup.

## Random Python quirks:
* Use float(“inf”) and float(“-inf”) for initializing a far bigger and smaller value 🙋.
* The way python checks for emptiness/None/zero values is not obvious. For example, if not x: will evaluate to True for x being an empty list, None, 0, and some others. While this syntax is recommended, go with explicit syntax (e.g. x != 0:) if you are even slightly uncertain.
* In usual cases, comparing two variables can be done in two ways: a == b or a is b. They serve different purposes (read up string interning for more), hence to avoid confusion, use a == b when comparing the values of variables. However, if x is not None is pretty acceptable way to check if a variable is set to None.

## Reference
* https://medium.com/@ratulsaha/preparing-for-programming-interview-as-a-phd-student-with-python-5f8af8b40d5f
