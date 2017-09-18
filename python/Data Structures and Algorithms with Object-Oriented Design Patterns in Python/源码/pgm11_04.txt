#
# This file contains the Python code from Program 11.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_04.txt
#
class BinaryHeap(PriorityQueue):

    def enqueue(self, obj):
        if self._count == len(self._array):
            raise ContainerFull
        self._count += 1
        i = self._count
        while i > 1 and self._array[i/2] > obj:
            self._array[i] = self._array[i / 2]
            i /= 2
        self._array[i] = obj

    # ...
