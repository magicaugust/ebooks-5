#
# This file contains the Python code from Program 8.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_18.txt
#
class OpenScatterTable(HashTable):

    def findMatch(self, obj):
        hash = self.h(obj)
        for i in xrange(len(self._array)):
            probe = (hash + self.c(i)) % len(self)
            if self._array[probe]._state == self.EMPTY:
                break
            if self._array[probe]._state == self.OCCUPIED and \
                    self._array[probe]._obj == obj:
                return probe
        return -1

    def find(self, obj):
        offset = self.findMatch(obj)
        if offset >= 0:
            return self._array[offset]._obj
        else:
            return None

    # ...
