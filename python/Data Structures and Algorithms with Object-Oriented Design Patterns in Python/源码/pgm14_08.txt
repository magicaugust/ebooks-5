#
# This file contains the Python code from Program 14.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_08.txt
#
def mergeSort(array, i, n):
    if n > 1:
        mergeSort(array, i, n / 2)
        mergeSort(array, i + n / 2, n - n / 2)
        merge(array, i, n / 2, n - n / 2)
