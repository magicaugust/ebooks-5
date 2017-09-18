#
# This file contains the Python code from Program 8.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_19.txt
#
class OpenScatterTable(HashTable):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        offset = self.findInstance(obj)
        if offset < 0:
            raise KeyError
        self._array[offset] = self.Entry(self.DELETED, None)
        self._count -= 1

    # ...
