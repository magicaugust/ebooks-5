#
# This file contains the Python code from Program 7.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_06.txt
#
class OrderedListAsArray(OrderedList):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        i = 0
        while i < self._count and self._array[i] is not obj:
            i += 1
        if i == self._count:
            raise KeyError
        while i < self._count - 1:
            self._array[i] = self._array[i + 1]
            i += 1
        self._array[i] = None
        self._count -= 1

    # ...
