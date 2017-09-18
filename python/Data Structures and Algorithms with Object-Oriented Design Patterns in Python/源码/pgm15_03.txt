#
# This file contains the Python code from Program 15.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_03.txt
#
class BinaryInsertionSorter(Sorter):

    def __init__(self):
        super(BinaryInsertionSorter, self).__init__()

    def _sort(self):
        for i in xrange(1, self._n):
            tmp = self._array[i]
            left = 0
            right = i
            while left < right:
                middle = (left + right) / 2
                if tmp >= self._array[middle]:
                    left = middle + 1
                else:
                    right = middle
            j = i
            while j > left:
                self.swap(j - 1, j)
                j -= 1
