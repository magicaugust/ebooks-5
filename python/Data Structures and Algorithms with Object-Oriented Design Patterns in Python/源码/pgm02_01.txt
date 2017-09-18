#
# This file contains the Python code from Program 2.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_01.txt
#
def sum(n):
    result = 0
    i = 1
    while i <= n:
        result += i
        i += 1
    return result
