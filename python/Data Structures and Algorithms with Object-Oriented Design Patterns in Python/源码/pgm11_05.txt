#
# This file contains the Python code from Program 11.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_05.txt
#
class BinaryHeap(PriorityQueue):

    def getMin(self):
        if self._count == 0:
            raise ContainerEmpty
        return self._array[1]

    # ...
