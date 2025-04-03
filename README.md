# Sorting
  * sort() method sorts the elements in ascending order in-place
  * The return value of the .sort() method is None
  * sort(key=None, reverse=False)
  * words.sort(key=get_word_length, reverse=True)
  * def get_word_length(word: str): return len(word)
  * numbers.sort(key=lambda num: abs(num))
  * sorted(numbers, key=lambda num: abs(num), reverse=True)

# Unpacking
# enumerate()
  * loop over an array and we needed to access both the index and the element at that index
  * eturns a tuple of the index and the element at that index
    
# zip()
  * zip() function takes multiple lists as arguments and returns an iterator of tuples
  * Each tuple contains an element from each list
  * dict or list can be directly used in zip(lista, listb)
  * multiple lists of different lengths can be used - default is list with shortest length
  * from itertools import zip_longest for zipping with longest list
  * zip_longtest(lista, listb, listc, fillvalue="NA")
    
# min() and max() functions to avoid going below and above certain value

# Resizable Lists
* append() - O(1)
* pop() and pop(index) - O(1)
* insert(index) - O(n)
* remove(element) - O(n)
* insert(index, element) - O(n)
* extend - O(m) - modifies existing list
* in operator - O(n)

# Concatenate list
* using + operator - creates a new list

# List Clone
* copy() creates shallow copy
* [:]
* list(original_list)
* import copy, copy.deepcopy(original_list) - creates deep copy, mainly for 2D lists or other complex DS

# List Comprehension
* for loop inside []
* result = [i + j for i, j in zip(arr1, arr2)]
* result = [i for i in arr if i % 2 == 0]
* [i for i in range(1, n+1, 2)]

# Stack
* using append() and pop() - O(1) and O(1)
* (-1) to access the top element
* eg: reverse a list (hint: use while len(list) > ))


