#
# This file contains the Python code from Program 3.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm03_04.txt
#
def Fibonacci(n):
    if n == 0 or n == 1:
        return n
    else:
        return Fibonacci(n - 1) + Fibonacci(n - 2)
