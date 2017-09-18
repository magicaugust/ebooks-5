#
# This file contains the Python code from Program 15.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_02.txt
#
class StraightInsertionSorter(Sorter):

    def __init__(self):
        super(StraightInsertionSorter, self).__init__()

    def _sort(self):
        for i in xrange(1, self._n):
            j = i
            while j > 0 and self._array[j - 1] > self._array[j]:
                self.swap(j, j - 1)
                j -= 1
