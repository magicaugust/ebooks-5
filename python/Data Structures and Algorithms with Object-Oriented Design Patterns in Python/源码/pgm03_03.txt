#
# This file contains the Python code from Program 3.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm03_03.txt
#
def Fibonacci(n):
    previous = -1
    result = 1
    i = 0
    while i <= n:
        sum = result + previous
        previous = result
        result = sum
        i += 1
    return result
