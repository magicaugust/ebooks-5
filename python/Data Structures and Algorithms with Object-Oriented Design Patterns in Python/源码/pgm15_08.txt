#
# This file contains the Python code from Program 15.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_08.txt
#
class MedianOfThreeQuickSorter(QuickSorter):

    def __init__(self):
        super(MedianOfThreeQuickSorter, self).__init__()

    def selectPivot(self, left, right):
        middle = (left + right) / 2
        if self._array[left] > self._array[middle]:
            self.swap(left, middle)
        if self._array[left] > self._array[right]:
            self.swap(left, right)
        if self._array[middle] > self._array[right]:
            self.swap(middle, right)
        return middle
