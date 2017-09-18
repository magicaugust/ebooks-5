#
# This file contains the Python code from Program 2.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_03.txt
#
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
