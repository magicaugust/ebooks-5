#
# This file contains the Python code from Program 8.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_17.txt
#
class OpenScatterTable(HashTable):

    def c(self, i):
        return i

    def findUnoccupied(self, obj):
        hash = self.h(obj)
        for i in xrange(self._count + 1):
            probe = (hash + self.c(i)) % len(self)
            if self._array[probe]._state != self.OCCUPIED:
                return probe
        raise ContainerFull

    def insert(self, obj):
        if self._count == len(self):
            raise ContainerFull
        offset = self.findUnoccupied(obj)
        self._array[offset] = self.Entry(self.OCCUPIED, obj)
        self._count += 1

    # ...
