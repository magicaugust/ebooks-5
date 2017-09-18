#
# This file contains the Python code from Program 2.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_06.txt
#
def geometricSeriesSum(x, n):
    sum = 0
    i = 0
    while i <= n:
        prod = 1
        j = 0
        while j < i:
            prod *= x
            j += 1
        sum += prod
        i += 1
    return sum
