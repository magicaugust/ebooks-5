#
# This file contains the Python code from Program 15.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_06.txt
#
class QuickSorter(Sorter):

    CUTOFF = 2 # minimum cut-off

    def quicksort(self, left, right):
        if right - left + 1 > self.CUTOFF:
            p = self.selectPivot(left, right)
            self.swap(p, right)
            pivot = self._array[right]
            i = left
            j = right - 1
            while True:
                while i < j and self._array[i] < pivot:
                    i += 1
                while i < j and self._array[j] > pivot:
                    j -= 1
                if i >= j:
                    break
                self.swap(i, j)
                i += 1
                j -= 1
            if self._array[i] > pivot:
                self.swap(i, right)
            if left < i:
                self.quicksort(left, i - 1)
            if right > i:
                self.quicksort(i + 1, right)

    # ...
