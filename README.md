# Sorting
  * .sort() method sorts the elements in ascending order in-place
  * The return value of the .sort() method is None
  * sort(key=None, reverse=False)
  * words.sort(key=get_word_length, reverse=True)
  * def get_word_length(word: str): return len(word)
  * numbers.sort(key=lambda num: abs(num))
  * sorted(numbers, key=lambda num: abs(num), reverse=True)

# Unpacking
# Enumerate()
  * loop over an array and we needed to access both the index and the element at that index
  * eturns a tuple of the index and the element at that index
# Zip()
  * zip() function takes multiple lists as arguments and returns an iterator of tuples
  * Each tuple contains an element from each list
  * dict or list can be directly used in zip(lista, listb)
  * multiple lists of different lengths can be used - default is list with shortest length
  * from itertools import zip_longest for zipping with longest list
  * zip_longtest(lista, listb, listc, fillvalue="NA")

