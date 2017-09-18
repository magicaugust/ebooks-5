#
# This file contains the Python code from Program 2.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_04.txt
#
def findMaximum(a, n):
    result = a[0]
    i = 1
    while i < n:
        if a[i] > result:
            result = a[i]
        i += 1
    return result
