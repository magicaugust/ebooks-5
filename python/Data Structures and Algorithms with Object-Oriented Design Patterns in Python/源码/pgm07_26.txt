#
# This file contains the Python code from Program 7.26 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_26.txt
#
class SortedListAsArray(OrderedListAsArray, SortedList):

    def findOffset(self, obj):
        left = 0
        right = self._count - 1
        while left <= right:
            middle = (left + right) / 2
            if obj > self._array[middle]:
                left = middle + 1
            elif obj < self._array[middle]:
                right = middle - 1
            else:
                return middle
        return -1

    # ...
