#
# This file contains the Python code from Program 7.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_04.txt
#
class OrderedListAsArray(OrderedList):

    def insert(self, obj):
        if self._count == len(self._array):
            raise ContainerFull
        self._array[self._count] = obj
        self._count += 1

    # ...
