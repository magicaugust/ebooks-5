#
# This file contains the Python code from Program 15.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_07.txt
#
class QuickSorter(Sorter):

    def _sort(self):
        self.quicksort(0, self._n - 1)
        sorter = StraightInsertionSorter()
        sorter.sort(self._array)

    # ...
