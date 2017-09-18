#
# This file contains the Python code from Program 7.25 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_25.txt
#
class SortedListAsArray(OrderedListAsArray, SortedList):

    def insert(self, obj):
        if self._count == len(self._array):
            raise ContainerFull
        i = self._count
        while i > 0 and self._array[i - 1] > obj:
            self._array[i] = self._array[i - 1]
            i -= 1
        self._array[i] = obj
        self._count += 1

    # ...
