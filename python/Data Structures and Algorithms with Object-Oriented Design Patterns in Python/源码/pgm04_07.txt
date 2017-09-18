#
# This file contains the Python code from Program 4.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_07.txt
#
class MultiDimensionalArray(object):

    def getOffset(self, indices):
        if len(indices) != len(self._dimensions):
            raise IndexError
        offset = 0
        for i, dim in enumerate(self._dimensions):
            if indices[i] < 0 or indices[i] >= dim:
                raise IndexError
            offset += self._factors[i] * indices[i]
        return offset

    def __getitem__(self, indices):
        return self._data[self.getOffset(indices)]

    def __setitem__(self, indices, value):
        self._data[self.getOffset(indices)] = value

    # ...
