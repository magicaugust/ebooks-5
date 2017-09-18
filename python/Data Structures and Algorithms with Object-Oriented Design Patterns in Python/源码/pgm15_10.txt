#
# This file contains the Python code from Program 15.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_10.txt
#
class HeapSorter(Sorter):

    def __init__(self):
        super(HeapSorter, self).__init__()


    def percolateDown(self, i, length):
        while 2 * i <= length:
            j = 2 * i
            if j < length and self._array[j + 1] \
                    > self._array[j]:
                j = j + 1
            if self._array[i] \
                    >= self._array[j]:
                break
            self.swap(i, j)
            i = j

    # ...
