#
# This file contains the Python code from Program 15.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_19.txt
#
class RadixSorter(Sorter):

    def _sort(self):
        self._tempArray = Array(self._n)
        for i in xrange(self.p):
            for j in xrange(self.R):
                self._count[j] = 0
            for k in xrange(self._n):
                self._count[(self._array[k] \
                    >> (self.r*i)) & (self.R-1)] += 1
                self._tempArray[k] = self._array[k]
            pos = 0
            for j in xrange(self.R):
                tmp = pos
                pos += self._count[j]
                self._count[j] = tmp
            for k in xrange(self._n):
                j = (self._tempArray[k] \
                    >> (self.r*i)) & (self.R-1)
                self._array[self._count[j]] = self._tempArray[k]
                self._count[j] += 1

    # ...
