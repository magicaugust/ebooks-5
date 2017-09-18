#
# This file contains the Python code from Program 12.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_04.txt
#
class SetAsArray(Set):

    def __or__(self, set):
	assert isinstance(set, SetAsArray)
	assert self._universeSize == set.universeSize
        result = SetAsArray(self._universeSize)
        for i in xrange(0, self._universeSize):
            result._array[i] = self._array[i] or set._array[i]
        return result

    def __and__(self, set):
	assert isinstance(set, SetAsArray)
	assert self._universeSize == set.universeSize
        result = SetAsArray(self._universeSize)
        for i in xrange(0, self._universeSize):
            result._array[i] = self._array[i] and set._array[i]
        return result

    def __sub__(self, set):
	assert isinstance(set, SetAsArray)
	assert self._universeSize == set.universeSize
        result = SetAsArray(self._universeSize)
        for i in xrange(0, self._universeSize):
            result._array[i] = self._array[i] \
                and not set._array[i]
        return result

    # ...
