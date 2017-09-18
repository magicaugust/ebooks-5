#
# This file contains the Python code from Program 11.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_06.txt
#
class BinaryHeap(PriorityQueue):

    def dequeueMin(self):
        if self._count == 0:
            raise ContainerEmpty
        result = self._array[1]
        last = self._array[self._count]
        self._count -= 1
        i = 1
        while 2 * i < self._count + 1:
            child = 2 * i
            if child + 1 < self._count + 1 \
                and self._array[child + 1] < self._array[child]:
                child += 1
            if last <= self._array[child]:
                break
            self._array[i] = self._array[child]
            i = child
        self._array[i] = last
        return result

    # ...
