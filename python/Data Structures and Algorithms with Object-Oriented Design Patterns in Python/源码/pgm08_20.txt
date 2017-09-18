#
# This file contains the Python code from Program 8.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_20.txt
#
class OpenScatterTableV2(OpenScatterTable):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        i = self.findInstance(obj)
        if i < 0:
            raise KeyError
        while True:
            j = (i + 1) % len(self)
            while self._array[j]._state == self.OCCUPIED:
                h = self.h(self._array[j]._obj)
                if ((h <= i and i < j) or (i < j and j < h) or \
                        (j < h and h <= i)):
                    break
                j = (j + 1) % len(self)
            if self._array[j]._state == self.EMPTY:
                break
            self._array[i] = self._array[j]
            i = j
        self._array[i] = self.Entry(self.EMPTY, None)
        self._count -= 1

    # ...
