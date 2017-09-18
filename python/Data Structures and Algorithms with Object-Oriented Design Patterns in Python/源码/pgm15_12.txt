#
# This file contains the Python code from Program 15.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_12.txt
#
class HeapSorter(Sorter):

    def _sort(self):
	base = self._array.baseIndex
	self._array.baseIndex = 1
        self.buildHeap()
        i = self._n
        while i >= 2:
            self.swap(i, 1)
            self.percolateDown(1, i - 1)
            i -= 1
	self._array.baseIndex = base

    # ...
