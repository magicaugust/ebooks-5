#
# This file contains the Python code from Program 2.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_07.txt
#
def geometricSeriesSum(x, n):
    sum = 0
    i = 0
    while i <= n:
        sum = sum * x + 1
        i += 1
    return sum
