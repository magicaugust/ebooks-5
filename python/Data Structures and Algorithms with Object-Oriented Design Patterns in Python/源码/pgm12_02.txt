#
# This file contains the Python code from Program 12.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_02.txt
#
class SetAsArray(Set):

    def __init__(self, n):
        super(SetAsArray, self).__init__(n)
        self._array = Array(self._universeSize)
        for item in xrange(0, self._universeSize):
            self._array[item] = False

    # ...
