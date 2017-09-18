#
# This file contains the Python code from Program 12.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_12.txt
#
class MultisetAsArray(Multiset):

    def __or__(self, set):
	assert isinstance(set, MultisetAsArray)
	assert self._universeSize == set._universeSize
        result = MultisetAsArray(self._universeSize)
        for i in xrange(self._universeSize):
            result._array[i] = self._array[i] + set._array[i]
        return result

    def __and__(self, set):
	assert isinstance(set, MultisetAsArray)
	assert self._universeSize == set._universeSize
        result = MultisetAsArray(self._universeSize)
        for i in xrange(self._universeSize):
            result._array[i] = min(self._array[i], set._array[i])
        return result

    def __sub__(self, set):
	assert isinstance(set, MultisetAsArray)
	assert self._universeSize == set._universeSize
        result = MultisetAsArray(self._universeSize)
        for i in xrange(self._universeSize):
            if set._array[i] <= self._array[i]:
                result._array[i] = self._array[i] - set._array[i]
        return result

    # ...
