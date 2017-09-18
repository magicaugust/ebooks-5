#
# This file contains the Python code from Program 15.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_14.txt
#
class TwoWayMergeSorter(Sorter):

    def merge(self, left, middle, right):
        i = left
        j = left
        k = middle + 1
        while j <= middle and k <= right:
            if self._array[j] < self._array[k]:
                self._tempArray[i] = self._array[j]
                i += 1
                j += 1
            else:
                self._tempArray[i] = self._array[k]
                i += 1
                k += 1
        while j <= middle:
            self._tempArray[i] = self._array[j]
            i += 1
            j += 1
        for i in xrange(left, k):
            self._array[i] = self._tempArray[i]

    # ...
