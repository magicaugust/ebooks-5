#
# This file contains the Python code from Program 2.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_08.txt
#
def power(x, n):
    if n == 0:
        return 1
    elif n % 2 == 0: # n is even
        return power(x * x, n / 2)
    else: # n is odd
        return x * power(x * x, n / 2)
