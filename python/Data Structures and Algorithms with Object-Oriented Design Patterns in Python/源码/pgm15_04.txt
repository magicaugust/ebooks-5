#
# This file contains the Python code from Program 15.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_04.txt
#
class BubbleSorter(Sorter):

    def __init__(self):
        super(BubbleSorter, self).__init__()

    def _sort(self):
        i = self._n
        while i > 1:
            for j in xrange(i - 1):
                if self._array[j] > self._array[j + 1]:
                    self.swap(j, j + 1)
            i -= 1
