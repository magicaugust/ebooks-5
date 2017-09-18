#
# This file contains the Python code from Program 8.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_13.txt
#
class ChainedScatterTable(HashTable):

    def insert(self, obj):
        if self._count == len(self):
            raise ContainerFull
        probe = self.h(obj)
        if self._array[probe]._obj is not None:
            while self._array[probe]._next != self.NULL:
                probe = self._array[probe]._next
            tail = probe
            probe = (probe + 1) % len(self)
            while self._array[probe]._obj is not None:
                probe = (probe + 1) % len(self)
            self._array[tail]._next = probe
        self._array[probe] = self.Entry(obj, self.NULL)
        self._count += 1

    def find(self, obj):
        probe = self.h(obj)
        while probe != self.NULL:
            if obj == self._array[probe]._obj:
                return self._array[probe]._obj
            probe = self._array[probe]._next
        return None

    # ...
