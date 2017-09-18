#
# This file contains the Python code from Program 12.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_08.txt
#
class SetAsBitVector(Set):

    def __or__(self, set):
	assert isinstance(set, SetAsBitVector)
	assert self._universeSize == set._universeSize
        result = SetAsBitVector(self._universeSize)
        for i in xrange(len(self._vector)):
            result._vector[i] = self._vector[i] | set._vector[i]
        return result

    def __and__(self, set):
	assert isinstance(set, SetAsBitVector)
	assert self._universeSize == set._universeSize
        result = SetAsBitVector(self._universeSize)
        for i in xrange(len(self._vector)):
            result._vector[i] = self._vector[i] & set._vector[i]
        return result

    def __sub__(self, set):
	assert isinstance(set, SetAsBitVector)
	assert self._universeSize == set._universeSize
        result = SetAsBitVector(self._universeSize)
        for i in xrange(len(self._vector)):
            result._vector[i] = self._vector[i] & ~set._vector[i]
        return result

    # ...
