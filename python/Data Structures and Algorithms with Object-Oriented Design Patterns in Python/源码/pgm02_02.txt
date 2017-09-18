#
# This file contains the Python code from Program 2.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_02.txt
#
def Horner(a, n, x):
    result = a[n]
    i = n - 1
    while i >= 0:
        result = result * x + a[i]
        i -= 1
    return result
