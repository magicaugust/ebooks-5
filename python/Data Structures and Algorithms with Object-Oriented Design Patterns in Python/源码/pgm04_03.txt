#
# This file contains the Python code from Program 4.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_03.txt
#
class Array(object):

    def getOffset(self, index):
        offset = index - self._baseIndex
        if offset < 0 or offset >= len(self._data):
            raise IndexError
        return offset

    def __getitem__(self, index):
        return self._data[self.getOffset(index)]

    def __setitem__(self, index, value):
        self._data[self.getOffset(index)] = value

    # ...
