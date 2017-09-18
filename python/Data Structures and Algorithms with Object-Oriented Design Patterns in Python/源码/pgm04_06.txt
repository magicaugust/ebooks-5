#
# This file contains the Python code from Program 4.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_06.txt
#
class MultiDimensionalArray(object):

    def __init__(self, *dimensions):
        self._dimensions = Array(len(dimensions))
        self._factors = Array(len(dimensions))
        product = 1
        i = len(dimensions) - 1
        while i >= 0:
            self._dimensions[i] = dimensions[i]
            self._factors[i] = product
            product *= self._dimensions[i]
            i -= 1
        self._data = Array(product)

    # ...
