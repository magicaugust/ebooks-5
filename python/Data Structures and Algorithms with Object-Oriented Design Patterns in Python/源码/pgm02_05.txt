#
# This file contains the Python code from Program 2.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_05.txt
#
def gamma():
    result = 0.
    i = 1
    while i <= 500000:
        result += 1.0/i - math.log((i + 1.0)/i)
        i += 1
    return result
