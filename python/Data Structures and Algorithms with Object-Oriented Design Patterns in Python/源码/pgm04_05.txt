#
# This file contains the Python code from Program 4.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_05.txt
#
class Array(object):

    def __len__(self):
        return len(self._data)

    def setLength(self, value):
        if len(self._data) != value:
            newData = [ None for i in xrange(value) ]
            m = min(len(self._data), value)
            for i in xrange(m):
                newData[i] = self._data[i]
            self._data = newData

    length = property(
        fget = lambda self: self.__len__(),
        fset = lambda self, value: self.setLength(value))

    # ...
