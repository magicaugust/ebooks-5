#
# This file contains the Python code from Program 4.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_04.txt
#
class Array(object):

    def getData(self):
        return self._data

    data = property(
        fget = lambda self: self.getData())

    def getBaseIndex(self):
        return self._baseIndex

    def setBaseIndex(self, baseIndex):
        self._baseIndex = baseIndex

    baseIndex = property(
        fget = lambda self: self.getBaseIndex(),
        fset = lambda self, value: self.setBaseIndex(value))

    # ...
