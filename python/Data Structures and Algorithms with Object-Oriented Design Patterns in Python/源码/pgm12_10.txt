#
# This file contains the Python code from Program 12.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_10.txt
#
class MultisetAsArray(Multiset):

    def __init__(self, n):
        super(MultisetAsArray, self).__init__(n)
        self._array = Array(self._universeSize)
        for item in xrange(self._universeSize):
            self._array[item] = 0

    # ...
