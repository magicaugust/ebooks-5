#
# This file contains the Python code from Program 6.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_12.txt
#
class QueueAsArray(Queue):

    def __init__(self, size = 0):
        super(QueueAsArray, self).__init__()
        self._array = Array(size)
        self._head = 0
        self._tail = size - 1

    def purge(self):
        while self._count > 0:
            self._array[self._head] = None
            self._head = self._head + 1
            if self._head == len(self._array):
                self._head = 0
            self._count -= 1

    # ...
