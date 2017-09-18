#
# This file contains the Python code from Program 7.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_08.txt
#
class OrderedListAsArray(OrderedList):

    def findPosition(self, obj):
        i = 0
        while i < self._count and self._array[i] != obj:
            i += 1
        return self.Cursor(self, i)

    def __getitem__(self, offset):
        if offset < 0 or offset >= self._count:
            raise IndexError
        return self._array[offset]

    # ...
