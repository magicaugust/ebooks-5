#
# This file contains the Python code from Program 2.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm02_09.txt
#
def geometricSeriesSum(x, n):
    return (power(x, n + 1) - 1) / (x - 1)
