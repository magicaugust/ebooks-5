#
# This file contains the Python code from Program 7.28 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_28.txt
#
class SortedListAsArray(OrderedListAsArray, SortedList):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        offset = self.findOffset(obj)
        if offset < 0:
            raise KeyError
        i = offset
        while i < self._count:
            self._array[i] = self._array[i + 1]
            i += 1
        self._array[i] = None
        self._count -= 1

    # ...
