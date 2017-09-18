#
# This file contains the Python code from Program 11.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_03.txt
#
class BinaryHeap(PriorityQueue):

    def __init__(self, length = 0):
        super(BinaryHeap, self).__init__()
        self._array = Array(length, 1) # Base index is 1.

    def purge(self):
        while self._count > 0:
            self._array[self._count] = None
            self._count -= 1

    # ...
