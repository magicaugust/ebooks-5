#
# This file contains the Python code from Program 12.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_05.txt
#
class SetAsArray(Set):

    def __eq__(self, set):
	assert isinstance(set, SetAsArray)
	assert self._universeSize == set.universeSize
        for i in xrange(0, self._universeSize):
            if self._array[i] != set._array[i]:
                return False
        return True

    def __lt__(self, set):
	assert isinstance(set, SetAsArray)
	assert self._universeSize == set.universeSize
        for i in xrange(0, self._universeSize):
            if self_array[i] and not set._array[i]:
                return False
        return True

    # ...
