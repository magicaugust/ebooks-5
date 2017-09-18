#
# This file contains the Python code from Program 6.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_05.txt
#
class StackAsArray(Stack):

    class Iterator(Iterator):

        def __init__(self, stack):
            super(StackAsArray.Iterator, self).__init__(stack)
            self._position = 0

        def next(self):
            if self._position >= self._container._count:
                raise StopIteration
	    obj = self._container._array[self._position]
            self._position = self._position + 1
            return obj

    def __iter__(self):
        return self.Iterator(self)

    #...
