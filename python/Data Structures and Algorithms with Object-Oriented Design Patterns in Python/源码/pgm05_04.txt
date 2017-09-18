#
# This file contains the Python code from Program 5.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_04.txt
#
class Container(Object):

    def getCount(self):
        return self._count

    count = property(
        fget = lambda self: self.getCount())

    def getIsEmpty(self):
        return self.count == 0

    isEmpty = property(
        fget = lambda self: self.getIsEmpty())

    def getIsFull(self):
        return False

    isFull = property(
        fget = lambda self: self.getIsFull())

    # ...
