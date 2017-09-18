#
# This file contains the Python code from Program 15.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_09.txt
#
class StraightSelectionSorter(Sorter):

    def __init__(self):
        super(StraightSelectionSorter, self).__init__()

    def _sort(self):
        i = self._n
        while i > 1:
            max = 0
            for j in xrange(i):
                if self._array[j] > self._array[max]:
                    max = j
            self.swap(i - 1, max)
            i -= 1
