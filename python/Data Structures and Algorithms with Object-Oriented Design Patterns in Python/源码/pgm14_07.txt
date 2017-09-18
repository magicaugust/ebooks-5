#
# This file contains the Python code from Program 14.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_07.txt
#
def Fibonacci(n):
    if n == 0 or n == 1:
        return n
    else:
        a = Fibonacci((n + 1) / 2)
        b = Fibonacci((n + 1) / 2 - 1)
        if n % 2 == 0:
            return a * (a + 2 * b)
        else:
            return a * a + b * b
