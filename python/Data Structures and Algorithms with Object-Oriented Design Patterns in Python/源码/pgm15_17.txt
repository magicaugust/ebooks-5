#
# This file contains the Python code from Program 15.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_17.txt
#
class BucketSorter(Sorter):

    def _sort(self):
        for i in xrange(self._m):
            self._count[i] = 0
        for j in xrange(self._n):
            self._count[self._array[j]] += 1
        j = 0
        for i in xrange(self._m):
            while self._count[i] > 0:
                self._array[j] = i
                j += 1
                self._count[i] -= 1

    # ...
}
