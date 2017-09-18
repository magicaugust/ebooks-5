#
# This file contains the Python code from Program 8.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_14.txt
#
class ChainedScatterTable(HashTable):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        i = self.h(obj)
        while i != self.NULL and self._array[i]._obj is not obj:
            i = self._array[i]._next
        if i == self.NULL:
            raise KeyError
        while True:
            j = self._array[i]._next
            while j != self.NULL:
                h = self.h(self._array[j]._obj)
                contained = False
                k = self._array[i]._next
                while k != self._array[j]._next \
                        and not contained:
                    if k == h:
                        contained = True
                    k = self._array[k]._next
                if not contained:
                    break
                j = self._array[j]._next
            if j == self.NULL:
                break
            self._array[i]._obj = self._array[j]._obj
            i = j
        self._array[i] = self.Entry(None, self.NULL)
        j = (i + len(self) - 1) % len(self)
        while j != i:
            if self._array[j]._next == i:
                self._array[j]._next = self.NULL
                break
            j = (j + len(self) - 1) % len(self)
        self._count -= 1

    # ...
