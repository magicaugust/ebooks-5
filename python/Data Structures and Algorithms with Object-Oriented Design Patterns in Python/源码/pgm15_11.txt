#
# This file contains the Python code from Program 15.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_11.txt
#
class HeapSorter(Sorter):

    def buildHeap(self):
        i = self._n / 2
        while i > 0:
            self.percolateDown(i, self._n)
            i -= 1

    # ...
