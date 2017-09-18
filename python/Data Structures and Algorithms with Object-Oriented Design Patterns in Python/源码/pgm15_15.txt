#
# This file contains the Python code from Program 15.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_15.txt
#
class TwoWayMergeSorter(Sorter):

    def _sort(self):
        self._tempArray = Array(self._n)
        self.mergesort(0, self._n - 1)
        self._tempArray = None

    def mergesort(self, left, right):
        if left < right:
            middle = (left + right) / 2
            self.mergesort(left, middle)
            self.mergesort(middle + 1, right)
            self.merge(left, middle, right)

    # ...
