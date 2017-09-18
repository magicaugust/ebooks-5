#
# This file contains the Python code from Program 6.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_19.txt
#
class DequeAsArray(QueueAsArray, Deque):

    def getTail(self):
        if self._count == 0:
            raise ContainerEmpty
        return self._array[self._tail];

    def dequeueTail(self):
        if self._count == 0:
            raise ContainerEmpty
        result = self._array[self._tail];
        self._array[self._tail] = None
        if self._tail == 0:
            self._tail = len(self._array) - 1
        else:
            self._tail = self._tail - 1
        self._count -= 1
        return result;

    # ...
