#
# This file contains the Python code from Program 6.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_03.txt
#
class StackAsArray(Stack):

    def push(self, obj):
        if self._count == len(self._array):
            raise ContainerFull
        self._array[self._count] = obj
        self._count += 1

    def pop(self):
        if self._count == 0:
            raise ContainerEmpty
        self._count -= 1
        result = self._array[self._count]
        self._array[self._count] = None
        return result

    def getTop(self):
        if self._count == 0:
            raise ContainerEmpty
        return self._array[self._count - 1]

    #...
