#
# This file contains the Python code from Program 14.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_06.txt
#
def binarySearch(array, target, i, n):
    if n == 0:
        raise KeyError
    if n == 1:
        if array[i] == target:
            return i
        raise KeyError
    else:
        j = i + n / 2
        if array[j] <= target:
            return binarySearch(array, target, j, n - n/2)
        else:
            return binarySearch(array, target, i, n/2)
