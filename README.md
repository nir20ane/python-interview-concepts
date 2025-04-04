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
  * returns a tuple of the index and the element at that index
    
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
* copy(original_list) creates shallow copy
* original_list[:]
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

# Queue - LIFO
* from collections import deque
* queue = deque(arr)
* popleft - O(1) and append - O(1)
* leftmost = arr[0], rightmost = [-1]
* rotate a list left by k, [1, 2, 3, 4, 5] -> [2, 3, 4, 5, 1]
* while i in range(k): queue.append(queue.popleft())

# Double sided queue - insert and remove from both ends
* from collections import deque
* queue = deque(arr)
* popleft - O(1) and append - O(1), pop() - O(1) and appendleft - O(1)
* leftmost = arr[0], rightmost = [-1]
* rotate a list right by k, [1, 2, 3, 4, 5] -> [5, 1, 2, 3, 4]
* while i in range(k): queue.appendleft(queue.pop())

# 2D Lists
* rows - len(grid)
* columns - len(grid[0])
* grid = [[0] * 3] * 2
* A better way to initialize a 2-D list is to use a nested list comprehension:
* grid = [[0 for i in range(3)] for j in range(2)]

# HashMap Basics
* my_dict = {}
* my_dict['a'] = 1 # {'a': 1}
* my_dict = {'a': 1}
* my_dict = {'a': 1, 'b': 2}
* del my_dict['a'] # {}
* my_dict.pop('b') # {}
* my_dict.pop('c') # KeyError: 'c'
* my_dict.pop('c', 'default') # No error, returns 'default'
* collections module provides a class called defaultdict that is a subclass of the built-in dict class
* It allows you to set a default value for a key that doesn't exist in the dictionary
* freq = defaultdict(int), for num in nums: freq[num] += 1
* d = defaultdict(list), for num in nums: d[num].append(num)
* from collections import Counter, counter = Counter(nums)
* counter = Counter(nums1), counter.update(nums2)
* Dict comprehension, eg: squared = {num: num * num for num in nums}
* Dict items(), keys() and values()
* my_set = set()
* my_set.add('b') # {'b'}
* my_set.discard('b') # {}
* my_set.discard('b') # {} (no error)
* Set comprehension: squared = {num * num for num in nums}
* Tuples, int and string can be used as keys in dictionary

# Heap
* Heaps are DS that allows to insert(push) or remove(pop) based on some priority
* by default, heap is min heap - smallest number or alphabet in lexicographical order
* heapq, heapq.heappush(heap, element), heapq.heappop(heap)
* heapify - to convert a list into heap
* Max heap:
  for num in nums:
        heapq.heappush(max_heap, -num) # Negate the number

  while max_heap:
        top = -heapq.heappop(max_heap) # Negate the number back
        print(top)
  
 * Custom heap through tuples:
  for num in nums:
    pair = (abs(num), num)
    heapq.heappush(heap, pair)

  while heap:
    pair = heapq.heappop(heap)
    original_num = pair[1]
    print(original_num) 
    
  * Custom heap - Max Heap - tuple
      for num in nums:
         pair = (-num, num)
         heapq.heappush(heap, pair)

      output = []
      while heap:
         pair = heapq.heappop(heap)
         output.append(pair[1])
      return output
   * nsmallest(int, arr) and nlargest(int, arr) - change order - reverse list [::-1]

# SortedDict
* popitem() method to remove and return the first or last key-value pair in sorted order
* pop() method to remove and return the value associated with a specific key, or the del keyword to delete a key-value pair
* popitem() method will raise a KeyError if the dictionary is empty
* pop() method will raise a KeyError if the key does not exist
* del keyword will also raise a KeyError if the key does not exist
* Time Complexity
    * Insertion - O(logn)
    * Access - O(logn)
    * Deletion - O(logn)
    * Lookup - O(logn)
 
# SortedSet
* from sortedcontainers import SortedSet
* remove() method will raise a KeyError if the element does not exist, while the discard() method will not
* pop() method will remove and return the largest element in the sorted set
* pop(0) method will remove and return the smallest element in the sorted set
* clear() method will remove all elements from the sorted set
* Time Complexity
    * Insertion - O(logn)
    * Deletion - O(logn)
    * Lookup - O(logn)
    * clear - O(n)



